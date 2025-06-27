1.1)  



&nbsp;                                                                                                  

public class Person {                                        

&nbsp;   

&nbsp;   private String name;                                                                         

&nbsp;   private int age;



&nbsp;    

&nbsp;   public Person(String name) {

&nbsp;       this.name = name;

&nbsp;       this.age = 18;

&nbsp;   }



&nbsp;  

&nbsp;   public Person(String name, int age) {

&nbsp;       this.name = name;

&nbsp;       this.age = age;

&nbsp;   }



&nbsp;   

&nbsp;   public void displayDetails() {

&nbsp;       System.out.println("Name: " + name);

&nbsp;       System.out.println("Age: " + age);

&nbsp;   }



&nbsp;  

&nbsp;   public static void main(String\[] args) {

&nbsp;       

&nbsp;       Person p1 = new Person("Vijay");

&nbsp;       p1.displayDetails();



&nbsp;       System.out.println(); // Just for spacing



&nbsp;     

&nbsp;       Person p2 = new Person("Ajith", 25);

&nbsp;       p2.displayDetails();

&nbsp;   }

}           **output:**



            **Name: vijay**

            **Age: 18**



            **Name: Ajith**

            **Age: 25**  







**1.2) Answer;**                              







public class Product {

&nbsp;   int pid;

&nbsp;   double price;

&nbsp;   int quantity;



&nbsp;   

&nbsp;   public Product(int pid, double price, int quantity) {

&nbsp;       this.pid = pid;

&nbsp;       this.price = price;

&nbsp;       this.quantity = quantity;

&nbsp;   }

}





import java.util.Scanner;



public class ProductMain {



&nbsp;   public static void main(String\[] args) {

&nbsp;       Scanner sc = new Scanner(System.in);

&nbsp;       Product\[] products = new Product\[5];



&nbsp;      

&nbsp;       for (int i = 0; i < 5; i++) {

&nbsp;           System.out.println("Enter Product ID, Price and Quantity for product " + (i + 1) + ":");

&nbsp;           int pid = sc.nextInt();

&nbsp;           double price = sc.nextDouble();

&nbsp;           int quantity = sc.nextInt();

&nbsp;           products\[i] = new Product(pid, price, quantity);

&nbsp;       }



&nbsp;       

&nbsp;       double maxPrice = products\[0].price;

&nbsp;       int maxPid = products\[0].pid;



&nbsp;       for (int i = 1; i < products.length; i++) {

&nbsp;           if (products\[i].price > maxPrice) {

&nbsp;               maxPrice = products\[i].price;

&nbsp;               maxPid = products\[i].pid;

&nbsp;           }

&nbsp;       }



&nbsp;       System.out.println("Product ID with the highest price: " + maxPid);



&nbsp;       

&nbsp;       double totalAmount = calculateTotalAmount(products);

&nbsp;       System.out.println("Total amount spent on all products: " + totalAmount);

&nbsp;   }



&nbsp;   

&nbsp;   public static double calculateTotalAmount(Product\[] products) {

&nbsp;       double total = 0;

&nbsp;       for (Product p : products) {

&nbsp;           total += p.price \* p.quantity;

&nbsp;       }

&nbsp;       return total;

&nbsp;   }

}

      **Output:**



      **Enter Product ID, Price and Quantity for product 1:**

      **101 50 2**



      **Enter Product ID, Price and Quantity for product 2:**

      **102 75 1**



      **Enter Product ID, Price and Quantity for product 3:**

      **103 60 3**



      **Enter Product ID, Price and Quantity for product 4:**

      **104 85 1**



      **Enter Product ID, Price and Quantity for product 5:**

      **105 55 2**



**Product ID with the highest price: 104**

**Total amount spent on all products: 505.0**



**1.3)  Answer:**





public class Account {

&nbsp;   private double balance;



&nbsp;    (default balance 0)

&nbsp;   public Account() {

&nbsp;       balance = 0.0;

&nbsp;   }



&nbsp;   

&nbsp;   public Account(double initialBalance) {

&nbsp;       balance = initialBalance;

&nbsp;   }



&nbsp;   

&nbsp;   public void deposit(double amount) {

&nbsp;       if (amount > 0) {

&nbsp;           balance += amount;

&nbsp;           System.out.println("Deposited: " + amount);

&nbsp;       } else {

&nbsp;           System.out.println("Deposit amount must be positive.");

&nbsp;       }

&nbsp;   }



&nbsp;   

&nbsp;   public void withdraw(double amount) {

&nbsp;       if (amount > 0 \&\& amount <= balance) {

&nbsp;           balance -= amount;

&nbsp;           System.out.println("Withdrawn: " + amount);

&nbsp;       } else {

&nbsp;           System.out.println("Insufficient balance or invalid amount.");

&nbsp;       }

&nbsp;   }



&nbsp;     public void displayBalance() {

&nbsp;       System.out.println("Current Balance: " + balance);

&nbsp;   }

}









public class AccountMain {

&nbsp;   public static void main(String\[] args) {

&nbsp;       

&nbsp;       Account acc1 = new Account();



&nbsp;       acc1.deposit(1000);

&nbsp;       acc1.withdraw(300);

&nbsp;       acc1.displayBalance();



&nbsp;       System.out.println();



&nbsp;       

&nbsp;       Account acc2 = new Account(5000);

&nbsp;       acc2.withdraw(1000);

&nbsp;       acc2.deposit(1500);

&nbsp;       acc2.displayBalance();

&nbsp;   }

}

   **output:**



   **Deposited: 1000.0**

**Withdrawn: 300.0**

**Current Balance: 700.0**



**Withdrawn: 1000.0**

**Deposited: 1500.0**

**Current Balance: 5500.0**





**1.4) Answer;**



public class Person {

&nbsp;   String name;

&nbsp;   int age;



&nbsp;   

&nbsp;   public Person(String name, int age) {

&nbsp;       this.name = name;

&nbsp;       this.age = age;

&nbsp;   }

}



public class Employee extends Person {

&nbsp;   int employeeID;

&nbsp;   double salary;



&nbsp;   

&nbsp;   public Employee(String name, int age, int employeeID, double salary) {

&nbsp;       super(name, age); // Call to parent constructor

&nbsp;       this.employeeID = employeeID;

&nbsp;       this.salary = salary;

&nbsp;   }



&nbsp;   

&nbsp;   public void displayDetails() {

&nbsp;       System.out.println("Employee ID: " + employeeID);

&nbsp;       System.out.println("Name       : " + name);

&nbsp;       System.out.println("Age        : " + age);

&nbsp;       System.out.println("Salary     : " + salary);

&nbsp;   }

}



public class EmployeeMain {

&nbsp;   public static void main(String\[] args) {

&nbsp;       

&nbsp;       Employee emp = new Employee("John Doe", 30, 1001, 50000.00);



&nbsp;       

&nbsp;       emp.displayDetails();

&nbsp;   }

}



   **output:**



**Employee ID: 1001**

**Name       : John Doe**

**Age        : 30**

**Salary     : 50000.0**

   



















