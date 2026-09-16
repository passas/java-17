Server:
```Java
try (ServerSocket serverSocket = new ServerSocket(5000))
{
  try (Socket socket = serverSocket.accept())
  {
    BufferedReader input = new BufferedReader( new InputStreamReader( socket.getInputStream() ) );
    PrintWriter output = new PrintWriter( socket.getOutputStream(), true );
  }
  while (true)
  {
    String echo = input.readLine();
    if ("exit".equals(echo))
      break;
  }
}
catch(IOException e)
{
  ...
}
```

Client:
```Java
try (Socket socket = new Socket("localhost", 5000))
{
  BufferedReader input = new BufferedReader ( new InputStreamReader ( socket.getInputStream() ) );
  PrintWriter output = new PrintWriter( socket.getOutputStream(), true );

  Scanner scanner = new Scanner(System.in);
  String requestString;
  String responseString;

  while (true)
  {
    requestString = scanner.nextLine();
    output.println(requestString);
    if ("exit".equals(requestString)
      break;
  }
}
catch (IOException e)
{
  ...
}
```
