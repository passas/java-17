Server:
```Java
ExecutorService pool = Executors.newCachedThreadPool();
try (ServerSocket serverSocket = new ServerSocket(5000))
{
  while (true)
  {
    Socket socket = serverSocket.accept()
    socket.setSoTimeOut(20000);
    pool.submit( () -> handler(socket) );
  }
}
catch(IOException e)
{
  ...
}

void handler(Socket socket)
{
  try (socket;
        BufferedReader input = new BufferedReader( new InputStreamReader( socket.getInputStream() ) );
        PrintWriter output = new PrintWriter( socket.getOutputStream(), true );
  )
  {
    while (true)
    {
      String echo = input.readLine();
      if ("exit".equals(echo))
        break;
    }
  }
  catch(Exception e)
  {...}
}
```
