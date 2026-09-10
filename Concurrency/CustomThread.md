```Java
public class CustomThread extends Thread
{
  @Override
  public void run()
  {
    try
    {
      Thread.sleep(500);
      // TimeUnit.SECONDS.sleep(1);
    }
    catch(InterruptedException e)
    {
      e.printStackTrace();
    }
  }
}
```

```Java
CustomThread customThread = new CustomThread();
customThread.start();       // assync               .run() // sync
// .join()
```
