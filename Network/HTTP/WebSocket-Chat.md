Server:
```Java
import org.java_websocket.WebSocket;
import org.java_websocket.handshake.ClientHandshake;
import org.java_websocket.server.WebSocketServer;

import java.net.InetSocketAddress;
import java.util.ArrayList;
import java.util.HashMap;
import java.util.Map;

public class SimpleWebSocketServer extends WebSocketServer {

    public static final int SERVER_PORT = 8080;

    private static Map<String, String> map = new HashMap<>();

    public SimpleWebSocketServer() {
        super(new InetSocketAddress(SERVER_PORT));
    }

    public static void main(String[] args) {

        var server = new SimpleWebSocketServer();
        server.start();
    }

    @Override
    public void onOpen(WebSocket webSocket, ClientHandshake clientHandshake) {
        var resource = webSocket.getResourceDescriptor();
        String name = resource.split("=")[1];
        map.put(webSocket.getRemoteSocketAddress().toString(),name);
        System.out.println(map.values());
        System.out.println("Connection Opened " + webSocket.getRemoteSocketAddress());
        broadcastAllButSender(webSocket,"%s joined".formatted(name));
    }

    @Override
    public void onClose(WebSocket webSocket, int i, String s, boolean b) {
        System.out.println("Connection Closed " + webSocket.getRemoteSocketAddress());
    }

    @Override
    public void onMessage(WebSocket webSocket, String s) {
        String chatName = map.get(webSocket.getRemoteSocketAddress().toString());
        broadcastAllButSender(webSocket,"%s: %s".formatted(chatName, s));
    }

    private void broadcastAllButSender(WebSocket webSocket, String message) {

        var connections = new ArrayList<>(getConnections());
        connections.remove(webSocket);
        broadcast(message, connections);
    }

    @Override
    public void onError(WebSocket webSocket, Exception e) {
        System.out.println("Error For " + webSocket.getRemoteSocketAddress());
    }

    @Override
    public void onStart() {
        System.out.println("Server listening on Port: " + getPort());
    }
}
```

Client:
```Java
import java.net.URI;
import java.net.URISyntaxException;
import java.net.http.HttpClient;
import java.net.http.WebSocket;
import java.util.Scanner;
import java.util.concurrent.CompletionStage;
import java.util.concurrent.ExecutionException;

public class WebSocketClient {

    public static void main(String[] args) throws URISyntaxException {

        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your name to join chat: ");
        String name = scanner.nextLine();

        HttpClient client = HttpClient.newHttpClient();
        WebSocket webSocket = client.newWebSocketBuilder()
                .buildAsync(new URI("ws://localhost:8080?name=%s"
                                .formatted(name)),
                        new WebSocket.Listener() {
                            @Override
                            public CompletionStage<?> onText(WebSocket webSocket,
                                                             CharSequence data,
                                                             boolean last) {
                                System.out.println(data);
                                return WebSocket.Listener.super.onText(webSocket,
                                        data, last);
                            }
                        }).join();

        while (true) {
            String input = scanner.nextLine();
            if ("bye".equalsIgnoreCase(input)) {
                try {
                    webSocket.sendClose(WebSocket.NORMAL_CLOSURE,
                            "User left normally").get();
                } catch (InterruptedException | ExecutionException e) {
                    throw new RuntimeException(e);
                }
                break;
            } else {
                webSocket.sendText(input, true);
            }
        }
    }
}
```
