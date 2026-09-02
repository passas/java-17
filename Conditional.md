If-then:
```Java
if (conditional)
  statement;

if (conditional)
{
  statements;
}

if (conditional)
  statement;
else
  statement;

if (conditional)
  statement;
else if (conditional)
  statement;
else
  statement;
```

Switch:
```Java
switch(expression)
{
  case match:
    statements;
    break;
  case match:      // follow through
  case match:
    statements;
  default:
    break;
}

switch(expression)
{
  case match -> statement;
  case match, match: -> {
    statements;
  }
  default -> statement;
}
```
