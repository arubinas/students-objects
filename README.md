import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        ArrayList<Student> students = new ArrayList<>();
        students.add(new Student(3, "John", "123 Street A"));
        students.add(new Student(1, "Alice", "456 Street B"));
        students.add(new Student(2, "Bob", "789 Street C"));
        students.add(new Student(5, "Charlie", "101 Street D"));
        students.add(new Student(4, "Dave", "202 Street E"));
        students.add(new Student(8, "Eve", "303 Street F"));
        students.add(new Student(7, "Frank", "404 Street G"));
        students.add(new Student(6, "Grace", "505 Street H"));
        students.add(new Student(10, "Heidi", "606 Street I"));
        students.add(new Student(9, "Ivan", "707 Street J"));

        System.out.println("Original list:");
        for (Student student : students) {
            System.out.println(student);
        }

        // Sort by name
        SelectionSort.selectionSort(students, new NameComparator());
        System.out.println("\nSorted by name:");
        for (Student student : students) {
            System.out.println(student);
        }

        // Sort by rollno
        SelectionSort.selectionSort(students, new RollnoComparator());
        System.out.println("\nSorted by roll number:");
        for (Student student : students) {
            System.out.println(student);
        }
    }
}
