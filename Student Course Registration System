import java.util.*;

class Course {
    String id, name, dept, teacher;
    int seats;

    Course(String id, String name, String dept, String teacher, int seats) {
        this.id = id;
        this.name = name;
        this.dept = dept;
        this.teacher = teacher;
        this.seats = seats;
    }

    void display() {
        System.out.println(id + " | " + name + " | " + dept + " | " + teacher + " | Seats: " + seats);
    }
}

class Student {
    String id, name;

    Student(String id, String name) {
        this.id = id;
        this.name = name;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
        HashMap<String, Course> courses = new HashMap<>();
        HashMap<String, Student> students = new HashMap<>();

        
        courses.put("C1", new Course("C1", "Java", "CS", "Mr. Sharma", 2));
        courses.put("C2", new Course("C2", "DSA", "CS", "Mr. Verma", 3));

        students.put("S1", new Student("S1", "Ritik"));

        while (true) {
            System.out.println("\n1. View Courses  2. Register  3. Drop  4. Exit");
            System.out.print("Choice: ");
            int choice = sc.nextInt();
            sc.nextLine();

            if (choice == 1) {
                for (Course c : courses.values()) {
                    c.display();
                }
            }

            else if (choice == 2) {
                System.out.print("Enter Course ID to Register: ");
                String cid = sc.nextLine();

                Course c = courses.get(cid);

                if (c != null && c.seats > 0) {
                    c.seats--;
                    System.out.println("Registered!");
                } else {
                    System.out.println("Course not found or no seats available.");
                }
            }

            else if (choice == 3) {
                System.out.print("Enter Course ID to Drop: ");
                String cid = sc.nextLine();

                Course c = courses.get(cid);

                if (c != null) {
                    c.seats++;
                    System.out.println("Dropped!");
                } else {
                    System.out.println("Course not found.");
                }
            }

            else if (choice == 4) {
                break;
            }
        }
    }
}
