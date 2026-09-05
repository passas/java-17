https://docs.oracle.com/javase/8/docs/api/java/util/Formatter.html

```Java
String.format(...);
```

```Java
private final static JSON_FORMAT = """
  "properties": {%s}
""";

...

public String toMap()
{
  return """
         "p1": "{%s}", "p2": {%d}
          """.formatted(this.getP1(), this.getP2());
}

...

JSON_FORMAT.formatted(this.toMap());
``
