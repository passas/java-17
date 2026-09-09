```Java
(int) (Math.random() * (upper - lower)) + lower
```

```Java
Random r = new Random();
r.nextInt(lower, upper);        // [lower,  upper[
r.nextInt(lower, upper + 1);    // [lower,  upper]
```

```Java
long nanoTime = System.nanoTime();
Random sr = new Random(nanoTime);
```
