Server:
```Java
try(DatagramSocket socket = new DatagramSocket(5000))
{
  byte[] buffer = new byte[1024];
  DatagramPacket packet = new DatagramPacket(buffer, buffer.length);
  socket.receive();
  String audioFileName = new String(buffer, 0, packet.getLength());
}
catch()
{}
```

Client:
```Java
try(DatagramSocket socket = new DatagramSocket())
{
  byte[] audioFileName = "Stitch.wav".getBytes();
  DatagramPacket packet = new DatagramPacket(audioFileName, audioFileName.length, InetAddress.getLocalHost(), 5000);
  socket.send(packet);
}
catch(IOException e)
{}
```
