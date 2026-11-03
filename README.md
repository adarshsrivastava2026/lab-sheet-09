# lab-sheet-09
code
# FOUNDATION OF JAVA LAB SHEET – 9
## Topic: Collections

---

### Q1. Student List

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> students = new ArrayList<>();

        students.add("Aman");
        students.add("Rahul");
        students.add("Priya");
        students.add("Neha");
        students.add("Rohit");
        students.add("Anjali");
        students.add("Karan");
        students.add("Simran");
        students.add("Vikas");
        students.add("Pooja");

        System.out.println("Student Names:");
        for (String name : students) {
            System.out.println(name);
        }

        System.out.println("Total Students: " + students.size());
    }
}
```

**Output:**
```text
Student Names:
Aman
Rahul
Priya
Neha
Rohit
Anjali
Karan
Simran
Vikas
Pooja
Total Students: 10
```

---

### Q2. Marks List

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> marks = new ArrayList<>();

        marks.add(85);
        marks.add(90);
        marks.add(75);
        marks.add(88);
        marks.add(95);

        System.out.println("First Mark: " + marks.get(0));
        System.out.println("Middle Mark: " + marks.get(2));
        System.out.println("Last Mark: " + marks.get(4));
    }
}
```

**Output:**
```text
First Mark: 85
Middle Mark: 75
Last Mark: 95
```

---

### Q3. Update Student Name

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> students = new ArrayList<>();

        students.add("Aman");
        students.add("Rahul");
        students.add("Priya");
        students.add("Neha");
        students.add("Rohit");

        students.set(1, "Aditya");
        students.remove(3);

        System.out.println("Updated Student List: " + students);
    }
}
```

**Output:**
```text
Updated Student List: [Aman, Aditya, Priya, Rohit]
```

---

### Q4. Unique Departments

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        HashSet<String> departments = new HashSet<>();

        departments.add("Computer Science");
        departments.add("IT");
        departments.add("Mechanical");
        departments.add("Computer Science");
        departments.add("Civil");
        departments.add("IT");

        System.out.println("Unique Departments:");

        for (String department : departments) {
            System.out.println(department);
        }
    }
}
```

**Output (order may vary):**
```text
Unique Departments:
Computer Science
IT
Mechanical
Civil
```

---

### Q5. Sorted Roll Numbers

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        TreeSet<Integer> rollNumbers = new TreeSet<>();

        rollNumbers.add(108);
        rollNumbers.add(103);
        rollNumbers.add(110);
        rollNumbers.add(101);
        rollNumbers.add(106);
        rollNumbers.add(105);
        rollNumbers.add(109);
        rollNumbers.add(102);
        rollNumbers.add(107);
        rollNumbers.add(104);

        System.out.println("Sorted Roll Numbers: " + rollNumbers);
    }
}
```

**Output:**
```text
Sorted Roll Numbers: [101, 102, 103, 104, 105, 106, 107, 108, 109, 110]
```

---

### Q6. ArrayList Searching

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> courses = new ArrayList<>();

        courses.add("Java");
        courses.add("Python");
        courses.add("C++");
        courses.add("Web Development");

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter course name: ");
        String course = sc.nextLine();

        if (courses.contains(course)) {
            System.out.println("Course is available.");
        } else {
            System.out.println("Course is not available.");
        }

        sc.close();
    }
}
```

**Output:**
```text
Enter course name: Java
Course is available.
```

---

### Q7. Collections Utility Methods

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<>();

        numbers.add(40);
        numbers.add(10);
        numbers.add(30);
        numbers.add(20);
        numbers.add(10);

        System.out.println("Original List: " + numbers);

        Collections.sort(numbers);
        System.out.println("Sorted List: " + numbers);

        Collections.reverse(numbers);
        System.out.println("Reversed List: " + numbers);

        System.out.println("Maximum: " + Collections.max(numbers));
        System.out.println("Minimum: " + Collections.min(numbers));
        System.out.println("Frequency of 10: " +
                           Collections.frequency(numbers, 10));
    }
}
```

**Output:**
```text
Original List: [40, 10, 30, 20, 10]
Sorted List: [10, 10, 20, 30, 40]
Reversed List: [40, 30, 20, 10, 10]
Maximum: 40
Minimum: 10
Frequency of 10: 2
```

---

### Q8. LinkedList Student Queue

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        LinkedList<String> students = new LinkedList<>();

        students.addFirst("Aman");
        students.addLast("Rahul");
        students.addLast("Priya");
        students.addFirst("Neha");

        System.out.println("Queue: " + students);

        students.removeFirst();
        System.out.println("After removeFirst(): " + students);

        students.removeLast();
        System.out.println("After removeLast(): " + students);
    }
}
```

**Output:**
```text
Queue: [Neha, Aman, Rahul, Priya]
After removeFirst(): [Aman, Rahul, Priya]
After removeLast(): [Aman, Rahul]
```

---

### Q9. ListIterator Modification

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        List<String> students = new ArrayList<>();

        students.add("Aman");
        students.add("Rahul");
        students.add("Priya");

        ListIterator<String> iterator = students.listIterator();

        while (iterator.hasNext()) {
            String name = iterator.next();

            if (name.equals("Rahul")) {
                iterator.set("Aditya");
                iterator.add("Neha");
            }
        }

        System.out.println("Updated List: " + students);
    }
}
```

**Output:**
```text
Updated List: [Aman, Aditya, Neha, Priya]
```

---

### Q10. List vs Set Experiment

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> list = new ArrayList<>();
        HashSet<Integer> set = new HashSet<>();

        int[] values = {10, 20, 10, 30, 20, 40, 50};

        for (int value : values) {
            list.add(value);
            set.add(value);
        }

        System.out.println("ArrayList: " + list);
        System.out.println("HashSet: " + set);
    }
}
```

**Output (HashSet order may vary):**
```text
ArrayList: [10, 20, 10, 30, 20, 40, 50]
HashSet: [50, 20, 40, 10, 30]
```

**Difference:**
- ArrayList allows duplicate elements and maintains insertion order.
- HashSet does not allow duplicate elements and does not guarantee order.

---

### Q11. Sorted Student IDs

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        TreeSet<Integer> ids = new TreeSet<>();

        ids.add(105);
        ids.add(101);
        ids.add(103);
        ids.add(102);
        ids.add(105);
        ids.add(104);

        System.out.println("Student IDs: " + ids);
        System.out.println("First ID: " + ids.first());
        System.out.println("Last ID: " + ids.last());
        System.out.println("Higher than 103: " + ids.higher(103));
        System.out.println("Lower than 103: " + ids.lower(103));
    }
}
```

**Output:**
```text
Student IDs: [101, 102, 103, 104, 105]
First ID: 101
Last ID: 105
Higher than 103: 104
Lower than 103: 102
```

---

### Q12. Hospital Patient List

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> patients = new ArrayList<>();
        HashSet<String> patientIDs = new HashSet<>();

        patients.add("Aman");
        patients.add("Rahul");
        patients.add("Priya");

        patientIDs.add("P101");
        patientIDs.add("P102");
        patientIDs.add("P103");

        System.out.println("Patient Records:");
        for (int i = 0; i < patients.size(); i++) {
            System.out.println(patients.get(i) + " - " +
                               new TreeSet<>(patientIDs).toArray()[i]);
        }

        patients.remove("Rahul");
        patientIDs.remove("P102");

        System.out.println("\nAfter Removing Rahul:");
        System.out.println("Patients: " + patients);
        System.out.println("Patient IDs: " + patientIDs);

        System.out.println("\nSearch Aman: " + patients.contains("Aman"));
        System.out.println("Search P101: " + patientIDs.contains("P101"));
    }
}
```

**Output (HashSet order may vary):**
```text
Patient Records:
Aman - P101
Rahul - P102
Priya - P103

After Removing Rahul:
Patients: [Aman, Priya]
Patient IDs: [P101, P103]

Search Aman: true
Search P101: true
```

---

### Q13. ListIterator Report

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        ArrayList<String> courses = new ArrayList<>();

        courses.add("Java");
        courses.add("Python");
        courses.add("C++");
        courses.add("HTML");
        courses.add("CSS");

        ListIterator<String> iterator = courses.listIterator();

        System.out.println("Forward Traversal:");
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }

        System.out.println("Next Index: " + iterator.nextIndex());
        System.out.println("Previous Index: " + iterator.previousIndex());

        System.out.println("\nBackward Traversal:");
        while (iterator.hasPrevious()) {
            System.out.println(iterator.previous());
        }
    }
}
```

**Output:**
```text
Forward Traversal:
Java
Python
C++
HTML
CSS
Next Index: 5
Previous Index: 4

Backward Traversal:
CSS
HTML
C++
Python
Java
```

---

### Q14. ArrayList vs LinkedList Lab

**Program:**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {

        // ArrayList
        ArrayList<String> arrayList = new ArrayList<>();

        arrayList.add("Java");
        arrayList.add("Python");
        arrayList.add("C++");

        arrayList.add(1, "HTML");
        arrayList.remove("Python");

        System.out.println("ArrayList: " + arrayList);
        System.out.println("ArrayList get(1): " + arrayList.get(1));
        System.out.println("ArrayList size: " + arrayList.size());

        System.out.println("ArrayList Iteration:");
        for (String item : arrayList) {
            System.out.println(item);
        }

        // LinkedList
        LinkedList<String> linkedList = new LinkedList<>();

        linkedList.add("Java");
        linkedList.add("Python");
        linkedList.add("C++");

        linkedList.add(1, "HTML");
        linkedList.remove("Python");

        System.out.println("\nLinkedList: " + linkedList);
        System.out.println("LinkedList get(1): " + linkedList.get(1));
        System.out.println("LinkedList size: " + linkedList.size());

        System.out.println("LinkedList Iteration:");
        for (String item : linkedList) {
            System.out.println(item);
        }
    }
}
```

**Output:**
```text
ArrayList: [Java, HTML, C++]
ArrayList get(1): HTML
ArrayList size: 3
ArrayList Iteration:
Java
HTML
C++

LinkedList: [Java, HTML, C++]
LinkedList get(1): HTML
LinkedList size: 3
LinkedList Iteration:
Java
HTML
C++
```

**Comparison Table:**

| ArrayList | LinkedList |
|---|---|
| Uses a dynamic array | Uses a doubly linked list |
| Faster random access | Slower random access |
| Insertion/deletion in the middle may require shifting | Insertion/deletion can be efficient when the position is already reached |
| Uses less memory generally | Uses more memory because of links |
| Best for frequent searching and accessing | Useful for frequent insertions and deletions |

---

### Q15. Mini Student Collection Management System

**Program:**
```java
import java.util.*;

class Student {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public String toString() {
        return "ID: " + id + ", Name: " + name;
    }
}

public class Main {
    public static void main(String[] args) {

        ArrayList<Student> students = new ArrayList<>();
        HashSet<Integer> uniqueIDs = new HashSet<>();
        TreeSet<Integer> sortedIDs = new TreeSet<>();

        Scanner sc = new Scanner(System.in);
        int choice;

        do {
            System.out.println("\n--- Student Management System ---");
            System.out.println("1. Add Student");
            System.out.println("2. Remove Student");
            System.out.println("3. Search Student");
            System.out.println("4. Display Students");
            System.out.println("5. Count Students");
            System.out.println("6. Forward Traversal");
            System.out.println("7. Backward Traversal");
            System.out.println("8. Display Unique IDs");
            System.out.println("9. Display Sorted IDs");
            System.out.println("0. Exit");

            System.out.print("Enter your choice: ");
            choice = sc.nextInt();

            switch (choice) {

                case 1:
                    System.out.print("Enter Student ID: ");
                    int id = sc.nextInt();
                    sc.nextLine();

                    if (uniqueIDs.contains(id)) {
                        System.out.println("Student ID already exists.");
                    } else {
                        System.out.print("Enter Student Name: ");
                        String name = sc.nextLine();

                        students.add(new Student(id, name));
                        uniqueIDs.add(id);
                        sortedIDs.add(id);

                        System.out.println("Student added successfully.");
                    }
                    break;

                case 2:
                    System.out.print("Enter ID to remove: ");
                    int removeID = sc.nextInt();

                    boolean removed = false;

                    Iterator<Student> removeIterator = students.iterator();

                    while (removeIterator.hasNext()) {
                        Student s = removeIterator.next();

                        if (s.id == removeID) {
                            removeIterator.remove();
                            uniqueIDs.remove(removeID);
                            sortedIDs.remove(removeID);
                            removed = true;
                            break;
                        }
                    }

                    if (removed) {
                        System.out.println("Student removed.");
                    } else {
                        System.out.println("Student not found.");
                    }
                    break;

                case 3:
                    System.out.print("Enter ID to search: ");
                    int searchID = sc.nextInt();

                    boolean found = false;

                    for (Student s : students) {
                        if (s.id == searchID) {
                            System.out.println("Student Found: " + s);
                            found = true;
                            break;
                        }
                    }

                    if (!found) {
                        System.out.println("Student not found.");
                    }
                    break;

                case 4:
                    System.out.println("Student Records:");
                    for (Student s : students) {
                        System.out.println(s);
                    }
                    break;

                case 5:
                    System.out.println("Total Students: " + students.size());
                    break;

                case 6:
                    System.out.println("Forward Traversal:");
                    ListIterator<Student> forward = students.listIterator();

                    while (forward.hasNext()) {
                        System.out.println(forward.next());
                    }
                    break;

                case 7:
                    System.out.println("Backward Traversal:");
                    ListIterator<Student> backward =
                        students.listIterator(students.size());

                    while (backward.hasPrevious()) {
                        System.out.println(backward.previous());
                    }
                    break;

                case 8:
                    System.out.println("Unique Student IDs: " + uniqueIDs);
                    break;

                case 9:
                    System.out.println("Sorted Student IDs: " + sortedIDs);
                    break;

                case 0:
                    System.out.println("Program Ended.");
                    break;

                default:
                    System.out.println("Invalid Choice.");
            }

        } while (choice != 0);

        sc.close();
    }
}
```

**Sample Output:**
```text
--- Student Management System ---
1. Add Student
2. Remove Student
3. Search Student
4. Display Students
5. Count Students
6. Forward Traversal
7. Backward Traversal
8. Display Unique IDs
9. Display Sorted IDs
0. Exit

Enter your choice: 1
Enter Student ID: 101
Enter Student Name: Aman
Student added successfully.

Enter your choice: 1
Enter Student ID: 103
Enter Student Name: Rahul
Student added successfully.

Enter your choice: 1
Enter Student ID: 102
Enter Student Name: Priya
Student added successfully.

Enter your choice: 4
Student Records:
ID: 101, Name: Aman
ID: 103, Name: Rahul
ID: 102, Name: Priya

Enter your choice: 8
Unique Student IDs: [101, 102, 103]

Enter your choice: 9
Sorted Student IDs: [101, 102, 103]

Enter your choice: 5
Total Students: 3

Enter your choice: 0
Program Ended.
```


