```Java
try
{
  URL url = new URL ("http://example.com");
  HttpURLConnection connection = (HttpURLCOnnection) url.openConnection();
  connection.setRequestMethod("GET");
  connection.setRequestProperty("User-Agent", "Chrome");
  connection.setRequestProperty("Accept", "application/json, text/html");
  connection.setReadTimeOut(30_000);

  int responseCode = connection.getResponseCode();  // connect
  connection.getInputStream();                      // connect
}  
catch (IOException e)
{ ... }
```
