class Worker {
    
    String name;
    int socialSecurityNumber;
    float wage;
    int workingHours;

    
    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Social Security Number: " + socialSecurityNumber);
    }

    void displaySalary() {
        float salary = wage * workingHours;
        System.out.println("Salary = " + salary);
    }
}


public class WorkerTest {
    public static void main(String[] args) {
        Worker worker1 = new Worker();
        worker1.name = "Ali Veli";
        worker1.socialSecurityNumber = 123456;
        worker1.wage = 15.5f;
        worker1.workingHours = 40;

        System.out.println("=== Worker 1 ===");
        worker1.displayInfo();
        worker1.displaySalary();

        // === Second Worker (Input from keyboard) ===
        Scanner sc = new Scanner(System.in);
        Worker worker2 = new Worker();

        System.out.println("\nEnter worker's name: ");
        worker2.name = sc.nextLine();

        System.out.println("Enter Social Security Number: ");
        worker2.socialSecurityNumber = sc.nextInt();

        System.out.println("Enter wage: ");
        worker2.wage = sc.nextFloat();

        System.out.println("Enter working hours: ");
        worker2.workingHours = sc.nextInt();

        System.out.println("\n=== Worker 2 ===");
        worker2.displayInfo();
        worker2.displaySalary();

        sc.close();
    }
}
