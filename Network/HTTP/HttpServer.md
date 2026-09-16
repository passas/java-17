```Java
try
{
  HttpServer server = HttpServer.create( new InetSocketAddress(8080), 0 );

  server.createContext("/", exchange -> {
    String requestMethod = exchange.getRequestMethod();
    String data = new String(exhange.getRequestBody().readAllBytes());

    String response = """
      <html>
        <body>
          <h3>Hello</h3>
        </body>
      </html>
    """;
    var bytes = response.getBytes();
    exchange.sendResponseHeaders(HTTP_OK, bytes.length);
    exchange.getResponseBody().write(bytes);
    exchange.close();
  });

  server.start();
}
catch (IOException e)
{ ... }
```
