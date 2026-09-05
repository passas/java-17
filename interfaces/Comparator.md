```Java
public class StudentGPAComparator implements Comparator<Student>
{
    @Override
    public int compare(Student s1, Student s2)
    {
      return s1.getGpa().compareTo(s2.getGpa());
    }
}
```

```Java
Arrays.sort(studentArray, new StudentGPAComparator()); 
Arrays.sort(studentArray, new StudentGPAComparator()).reversed(); 

```
