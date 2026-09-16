Server:
```Java
try(ServerSocketChannel serverChannel = new ServerSocketChannel.open())
{
  serverChannel.socket().bind(new InetSocketAddress(5000));
  serverChannel.socket.getLocalPort();

  while(true)
  {
    SocketChannel clientChannel = serverChannel.accept();
    clientChannel.socket().getRemoteSocketAddress();

    ByteBuffer buffer = ByteBuffer.allocate(1024);
    SocketChannel channel = clientChannel;
    int readBytes = channel.read(buffer);
    if (readBytes > 0)
    {
      buffer.flip(); // writeable to readable
      channel.write(ByteBuffer.wrap("Echo from server: ".getBytes());
      while (buffer.hasRemaining())
      {
        channel.write(buffer);
      }
      buffer.clear();
    }
    else if (readBytes == -1) // lost connection
    {
      ...
      channel.close();
    }
  }

}
catch(IOException e)
{ ... }
```

Client:
```Java
```
