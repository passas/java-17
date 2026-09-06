```Java
<T> void processPoint(T v1, T v2, BiConsumer<T,T> consumer)
{
  consumer.apply(v1, v2);
}

BiConsumer<Double, Double> p1 = (lat, long) -> "%.3f,%.3f".formatted(lat, long);

processPoint(p[0], p[1], p1);

```
