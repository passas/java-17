```Java
try( BufferedWritter bufferedWritter = Files.newBufferedWriter(Path.of("students.csv")))
{
  bufferedWritter.write(header);
  bufferedWritter.newLine();

  for (Student student : students)
    for (var record : student.getEngagemantRecords())
    {
      bufferedWritter.write(record);
      bufferedWritter.newLine();
    }
}
catch(IOException e) {}
```
