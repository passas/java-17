```Java
var currentThread = Thread.currentThread();
currentThread.setPriority(Thread.MAX_PRIORITY); // 1 < 10
void threadState(Thread thread)
{
  thread.getId();
  thread.getName();
  thread.getPriority();
  thread.getState();
  thread.getThreadGroup();
  thread.isAlive();
}
```
