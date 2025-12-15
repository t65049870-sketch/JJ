1.	Write a Java program to check whether a number is even or odd

Code:-  
package javaprograms;
import java.util.Scanner;
public class EvenOdd {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);
System.out.print("Enter a number: ");
int num = sc.nextInt();
if (num % 2 == 0) {
System.out.println(num + " is even.");
} else {
System.out.println(num + " is odd.");
}
sc.close();
}
}

2.	Write a Java program to check whether a number is prime.
Code :
package javaprograms;
import java.util.Scanner;
public class PrimeCheck {
 public static void main(String[] args) {
 Scanner sc = new Scanner(System.in);
System.out.print("Enter a number: ");
 int num = sc.nextInt();
        int count = 0; 
 for (int i = 1; i <= num; i++) {
 if (num % i == 0) {
 count++; 
 }
 }
 if (count == 2) {
 System.out.println(num + " is a Prime number.");
 } else {
 System.out.println(num + " is NOT a Prime number.");
 }
        sc.close();
 }
}

3.	Write a Java program to generate the Fibonacci series. Up to n terms.

Code :
package javaprograms;
public class FibonacciSeries {
public static void main(String[] args) {

 int n = 10; // number of terms to display
 int first = 0, second = 1;
 System.out.println("Fibonacci Series up to " + n + " terms:");
 for (int i = 1; i <= n; i++) {
 System.out.print(first + " ");
 // calculate the next term
 int next = first + second;
 first = second;
 second = next;
 }
}

}

4.	Write a Java program to calculate the factorial of a number.
Code:
package javaprograms;
public class Factorial {
public static void main(String[] args) {
// TODO Auto-generated method stub
Integer num1=5, fact=6,result=2;
for(num1=1; num1<=fact; num1++) {
 result=num1*result;
}
System.out.println("factorial " +result);
}
}

5.	Write a Java program to reverse a number.
Code:
package javaprograms;
public class ReverseNumber {
public static void main(String[] args) {
// TODO Auto-generated method stub
int num=543, rev, sum=0;
while(num>0) {
rev=num%10; 
sum=(sum*10)+rev;
num=num/10;
}
System.out.println("reverse of number: " +sum);
}
}

Write a Java program to implement a calculator using a switch case.
Code:
package javaprograms;
import java.util.Scanner;
public class Calculator {
public static void main(String[] args) {
double num1, num2, result;
char operator;
Scanner sc = new Scanner(System.in);
System.out.print("Enter first number: ");
num1 = sc.nextDouble();
System.out.print("Enter second number: ");
num2 = sc.nextDouble();
System.out.print("Choose an operator (+, -, *, /, %): ");
operator = sc.next().charAt(0);
switch (operator) {
case '+':
result = num1 + num2;
System.out.println("Result = " + result);
break;
case '-':
result = num1 - num2;
System.out.println("Result = " + result);
break;
case '*':
result = num1 * num2;
System.out.println("Result = " + result);
break;
case '/':
if (num2 != 0) {
result = num1 / num2;
System.out.println("Result = " + result);
} else {
System.out.println("Error! Division by zero is not allowed.");
} break;
case '%':
if (num2 != 0) {
result = num1 % num2;
System.out.println("Result = " + result);
} else {
System.out.println("Error! Division by zero is not allowed.");
} break;
default:
System.out.println("Invalid operator!");
break; }
sc.close();          
}
} 

7.	Write a Java program to print a pattern (e.g., pyramid, diamond).
Code:
package javaprograms;

public class PatternPrinter {
public static void main(String[] args) {
int rows = 5;
// ---------- Pyramid Pattern ----------
System.out.println("Pyramid Pattern:\n");
for (int i = 1; i <= rows; i++) {
for (int j = i; j < rows; j++) {
System.out.print(" ");
}
for (int k = 1; k <= i; k++) {
System.out.print("* ");
}
System.out.println();
}

// ---------- Diamond Pattern ----------
System.out.println("\nDiamond Pattern:\n");

// upper part
for (int i = 1; i <= rows; i++) {
for (int j = i; j < rows; j++) {
System.out.print(" ");
}
for (int k = 1; k <= i; k++) {
System.out.print("* ");
}
System.out.println();
}

// lower part
for (int i = rows - 1; i >= 1; i--) {
for (int j = rows; j > i; j--) {
System.out.print(" ");
}
for (int k = 1; k <= i; k++) {
System.out.print("* ");
}
System.out.println();
}
}
}


8.Write a Java program to find the sum and average of elements in an array.
Code:
package javaprograms;
import java.util.*;
import java.util.Arrays;
public class SumAndAverage {
public static void main(String[] args) {
    int arr[] = new int[5];
    double sum=0, average=0.0;
    Scanner sc = new Scanner(System.in);
    System.out.print("Enter the array elemant: ");
    for(int i=0;i<arr.length;i++) {
    	arr[i]=sc.nextInt();
    	sum=sum+arr[i];
    }
    average=(sum/arr.length);
    System.out.println("Sum of array elements = " + sum);
    System.out.println("Average of array elements = " + average);
}
}

9.	Write a Java program to find the second largest element in an array.
Code:
package javaprograms;
import java.util.*;
import java.util.Arrays;
public class SecondLargestElement {
    public static void main(String[] args) {
    	    int arr[] = new int[5];
    	    double sum=0, average=0.0;
    	    Scanner sc = new Scanner(System.in);
        System.out.print("Enter the array element: ");
        for(int i=0; i<arr.length; i++) {
        	arr[i]=sc.nextInt();
        }
        Arrays.sort(arr);
        System.out.println("my array elemant are " + Arrays.toString(arr));
        System.out.println("The second largest element = " +arr[arr.length-2]);
        sc.close();
}
}

10.Write a Java program to sort an array using Bubble Sort.
Code:
package javaprograms;
import java.io.*;
public class BubbleSort {
public static void main(String[] args) throws IOException {
int arr[] = new int[5];
int temp;
BufferedReader br= new BufferedReader(new InputStreamReader(System.in));
System.out.println("Enter the array element:");
for (int i=0;i<arr.length;i++) {
arr[i]=Integer.parseInt(br.readLine());
}	
for (int i = 0; i < arr.length - 1; i++) {
 for (int j = 0; j < arr.length - i - 1; j++) {
 if (arr[j] > arr[j + 1]) {
 temp = arr[j];
 arr[j] = arr[j + 1];
 arr[j + 1] = temp;
}
}
 }
System.out.println("Sorted array:");
for (int i=0;i<arr.length;i++) {
System.out.println(arr[i] + "");
}
}
}

11.Write a Java program to search an element in an array using Linear Search.
Code:
package javaprograms;
import java.util.Scanner;
public class SearchElement {
public static void main(String[] args) {
int arr[] = new int[5];
int Search, i;
Scanner sc = new Scanner(System.in);
System.out.print("Enter the array elements: ");
for (i = 0; i < arr.length; i++) {
arr[i] = sc.nextInt();
}
System.out.println("Enter the element you want to search: ");
Search = sc.nextInt();
for (i = 0; i < arr.length; i++) {
if (arr[i] == Search) {
System.out.println("The number found at " + (i + 1) + " position");
break; 
}
}
if (i == arr.length) {
System.out.println("Number not present in array");}}}

12.Write a Java program to implement a class and create objects.
Code:
package javaprograms;
public class MethodOverloading {
// Method with one parameter
void display(int a) {
System.out.println("Method with one integer parameter: " + a);
}
// Method with two parameters
void display(int a, int b) {
System.out.println("Method with two integer parameters: " + a + " and " + b);
}
// Method with different parameter type
void display(String message) {
System.out.println("Method with one String parameter: " + message);
}
public static void main(String[] args) {
MethodOverloading obj = new MethodOverloading();
// Calling different overloaded methods
obj.display(10);
obj.display(10, 20);
obj.display("Hello from overloaded method!");
}
}

13. Write a Java program to demonstrate constructor overloading.
Code:
package javaprograms;

public class CarExample {
String model;
int year;
// Default Constructor
public CarExample() {
model = "";
year = 0;
}
// Constructor with one parameter
public CarExample(String model) {
this.model = model;
this.year = 2020;
}
// Constructor with two parameters
public CarExample(String model, int year) {
this.model = model;
this.year = year;
}
// Display method
public void display() {
System.out.println("Model: " + model + " | Year: " + year);
}
// Main method
public static void main(String[] args) {
CarExample obj1 = new CarExample();
CarExample obj2 = new CarExample("Tata Safari");
CarExample obj3 = new CarExample("Tata Harrier", 2024);
obj1.display();
obj2.display();
obj3.display();
}
}


14. Write a Java program to demonstrate Single Inheritance.
Code:
package javaprograms;
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
class vehicle{
int tyre,ecap;
    String color;
    public void getvehicleDetails() throws IOException{
    	BufferedReader br=new BufferedReader (new InputStreamReader(System.in));
    	System.out.println("Enter No. of tyre , engine capacity , color");
    	tyre=Integer.parseInt(br.readLine());
    	ecap=Integer.parseInt(br.readLine());
    	color=br.readLine();
    }
    public void putvehicleDetails() {
    	System.out.println("no. of tyres: "+tyre);
    	System.out.println("Engine capacity: "+ecap);
    	System.out.println("Color: "+color);
    }}
class Car1 extends vehicle{
 String comp,ctype,fuel;
 public void getCarDetails() throws IOException{
 BufferedReader br=new BufferedReader (new InputStreamReader(System.in));
 System.out.println("Enter the comp , ctype, fuel");
 comp=br.readLine();
 ctype=br.readLine();
 fuel=br.readLine();
 }
 public void putCarDetails() {
    	System.out.println("Enter company name: "+comp);
    	System.out.println("enter car type: "+ctype);
    	System.out.println("Enter fuel: "+fuel);
    }
}
public class InheritanceExample1 {
public static void main(String[] args) throws IOException{
     Car1 obj=new Car1();
     obj.getvehicleDetails();
     obj.putvehicleDetails();
     obj.getCarDetails();
     obj.putCarDetails();
}
}

15.Write a Java program to implement method overloading.
Code:
package javaprograms;
public class MethodOverloading {
// Method with one parameter
void display(int a) {
System.out.println("Method with one integer parameter: " + a);
}
// Method with two parameters
void display(int a, int b) {
System.out.println("Method with two integer parameters: " + a + " and " + b);
}
// Method with different parameter type
void display(String message) {
System.out.println("Method with one String parameter: " + message);
}
public static void main(String[] args) {
MethodOverloading obj = new MethodOverloading();
// Calling different overloaded methods
obj.display(10);
obj.display(10, 20);
obj.display("Hello from overloaded method!");
}
}

16. Write a Java program to demonstrate use of interfaces.
Code:
package javaprograms;
interface Animal{
void activity();
void run();
void eat();
void sleep();
}
class cat implements Animal{
public void activity () {
System.out.println("Activity of the animal");}
public void run() {
System.out.println("Animals can run");
}
public void eat() {
System.out.println("Animals can eat");
}
public void sleep() {
System.out.println("Animals can sleep");
} 	}
public class InterfacesMultiInherit { 	
public static void main(String[] args) {
cat c = new cat();
c.activity();
c.eat();
 c.run();
c.sleep();
}
}

17. Write a Java program to demonstrate use of packages.
Code 1:
package javaprograms;

public class MessagePrinter {
public void printMessage() {
System.out.println("Hello from the package!!");
}
}

Code 2:
package javaprograms;
public class MainClass {
public static void main(String[] args) {
MessagePrinter printer = new MessagePrinter();
printer.printMessage();
}
}

18. Write a Java program to handle ArithmeticException.
Code:
package javaprograms;
import java.util.Scanner;
public class Arithmetic {
public static void main(String[] args) {
double num1, num2, result;
char operator;
Scanner sc = new Scanner(System.in);
System.out.print("Enter first number: ");
num1 = sc.nextDouble();
System.out.print("Enter second number: ");
num2 = sc.nextDouble();
System.out.print("Choose an operator (+, -, *, /, %): ");
operator = sc.next().charAt(0);
switch (operator) {
case '+':
result = num1 + num2;
System.out.println("Result = " + result);
break;
case '-':
result = num1 - num2;
System.out.println("Result = " + result);
break;
case '*':
result = num1 * num2;
System.out.println("Result = " + result);
break;
case '/':
if (num2 != 0) {
result = num1 / num2;
System.out.println("Result = " + result);
} else {
System.out.println("Error! Division by zero is not allowed.");
}
break;
case '%':
if (num2 != 0) {
result = num1 % num2;
System.out.println("Result = " + result);
} else {
System.out.println("Error! Division by zero is not allowed.");
}
break;
default:
System.out.println("Invalid operator!");
break;
}
sc.close();
}
}

19. .Write a Java program to create and use a custom exception.
Code:
package javaprograms;
class InvalidAgeException extends Exception{
InvalidAgeException(String s){
super(s);
}
}
public class UserException {
static void validate(int age)throws InvalidAgeException{
if(age<18)
throw new InvalidAgeException("sorry you cant vote your age is below 18");
else
System.out.println("congrats you are above 18, you are eligible for vote");
}
public static void main(String args[]){
try{
validate(16);
}catch(Exception m){
System.out.println("Exception occured: "+m);
}
}}

20. Write a Java program to read from and write to a text file.
Code:
package javaprograms;
import java.io.*;
public class CharReadExample {
public static void main(String[] args) {
try {
FileReader reader = new FileReader("D:\\java\\javaprograms\\src\\javaprograms\\input.txt");
int ch;
while ((ch = reader.read()) != -1) {
System.out.print((char) ch);
}
reader.close();
FileWriter writer = new FileWriter("D:\\java\\javaprograms\\src\\javaprograms\\input.txt");
writer.write("additional contents into the file");
writer.close();
} catch (IOException e) {
System.out.println("An error occured while reading the file");
}

}
}

21. Write a Java program to copy content from one file to another.
Code: 
package javaprograms;
import java.io.*;
public class copyChar {
public static void main(String[] args) throws IOException {
FileReader reader = new FileReader("D:\\java\\javaprograms\\src\\javaprograms\\input.txt");
 FileWriter writer = new FileWriter("D:\\java\\javaprograms\\src\\javaprograms\\output.txt");
int ch;
while((ch = reader.read()) != -1) {
writer.write(ch);
}
System.out.println("File contents are copied");
 reader.close();
 writer.close();
}
}

22. Write a Java program to create a basic AWT form.
Code:
package javaprograms;
import javax.swing.*;
public class MyFrame {
public static void main(String[] args) {
JFrame frameObj = new JFrame("java swing fame");
JTextField textObject = new JTextField("vishal thakur");
textObject.setBounds(200,100,200,50);
frameObj.add(textObject);
frameObj.setSize(500,500);
frameObj.setLayout(null);
frameObj.setVisible(true);
}
}

23. Write a Java program to implement a simple calculator using AWT/Swing.
Code:
package javaprograms;
import java.awt.event.*;
import javax.swing.*;
public class Swing_Calcultor {
public static void main(String[] args) {
JFrame f = new JFrame("burrron example");
final JTextField tf1 = new JTextField ("enetr the first value");
final JTextField tf2 = new JTextField ("enetr the second value");
final JTextField tf3 = new JTextField ("result");
JButton plus = new JButton("+");
JButton minus = new JButton("-");
JButton multiply = new JButton("*");
JButton divide = new JButton("/");
f.setLayout(new java.awt.GridLayout(7,1));
plus.addActionListener(new ActionListener() {
 	 String res;
 	 public void actionPerformed(ActionEvent e) {
 	 int first=Integer.parseInt(tf1.getText());
 	 int second=Integer.parseInt(tf2.getText());
 	 res = String.valueOf(first+second);
 	 tf3.setText(res);
 	 }
});
minus.addActionListener(new ActionListener() {
 	 String res;
 	 public void actionPerformed(ActionEvent e) {
 	 int first=Integer.parseInt(tf1.getText());
 	 int second=Integer.parseInt(tf2.getText());
 	 res = String.valueOf(first-second);
 	 tf3.setText(res);
 	 }
});
multiply.addActionListener(new ActionListener() {
 	 String res;
 	 public void actionPerformed(ActionEvent e) {
 	 int first=Integer.parseInt(tf1.getText());
 	 int second=Integer.parseInt(tf2.getText());
 	 res = String.valueOf(first*second);
 	 tf3.setText(res);
 	 }
});
divide.addActionListener(new ActionListener() {
 	 String res;
 	 public void actionPerformed(ActionEvent e) {
 	 int first=Integer.parseInt(tf1.getText());
 	 int second=Integer.parseInt(tf2.getText());
 	 res = String.valueOf(first/second);
 	 tf3.setText(res);
 	 }
});
f.add(plus);
f.add(minus);
f.add(multiply);
f.add(divide);
f.add(tf1);
f.add(tf2); 	
f.add(tf3);
f.setSize(400,400);
f.setVisible(true);
f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
}
}


24. Write a Java program to design Login Screen using Swing.
Code:
package javaprograms;

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class LoginSwing extends JFrame implements ActionListener {
// Components
JLabel labelUsername, labelPassword, labelTitle;
JTextField textUsername;
JPasswordField textPassword;
JButton buttonLogin, buttonReset;

public LoginSwing() {
// Frame settings
setTitle("Login Screen");
setSize(400, 300);
setLayout(null); // Using absolute positioning
setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
setLocationRelativeTo(null); // Center the frame

// Title Label
labelTitle = new JLabel("User Login");
labelTitle.setFont(new Font("Arial", Font.BOLD, 20));
labelTitle.setBounds(140, 20, 200, 30);
add(labelTitle);

// Username Label and Field
labelUsername = new JLabel("Username:");
labelUsername.setBounds(50, 80, 100, 25);
add(labelUsername);

textUsername = new JTextField();
textUsername.setBounds(150, 80, 180, 25);
add(textUsername);

// Password Label and Field
labelPassword = new JLabel("Password:");
labelPassword.setBounds(50, 120, 100, 25);
add(labelPassword);

textPassword = new JPasswordField();
textPassword.setBounds(150, 120, 180, 25);
add(textPassword);

// Buttons
buttonLogin = new JButton("Login");
buttonLogin.setBounds(100, 180, 80, 30);
buttonLogin.addActionListener(this);
add(buttonLogin);

buttonReset = new JButton("Reset");
buttonReset.setBounds(200, 180, 80, 30);
buttonReset.addActionListener(this);
add(buttonReset);

// Make frame visible
setVisible(true);
}

@Override
public void actionPerformed(ActionEvent e) {
if (e.getSource() == buttonLogin) {
String username = textUsername.getText();
String password = new String(textPassword.getPassword());

if (username.equals("admin") && password.equals("12345")) {
JOptionPane.showMessageDialog(this, "Login Successful!");
} else {
JOptionPane.showMessageDialog(this, "Invalid Username or Password!");
}
}

if (e.getSource() == buttonReset) {
textUsername.setText("");
textPassword.setText("");
}
}

public static void main(String[] args) {
new LoginSwing();

25. write a java program to create a Candidate information screen.
Code:
package javaprograms;
import java.awt.*;
import javax.swing.*;
public class SwingCan extends JFrame {
JLabel l1,l2,l3,l4,l5,l6;
JCheckBox check1,check2,check3;
JTextField t1,t2,t3,t4;
JButton b1,b2;
JRadioButton radio1,radio2;
JPanel j1,j2,j3,j4;
Container Contentpane;
ButtonGroup bg;
public SwingCan()
{
setLayout(new GridLayout(4,1));
setSize(300,500);
setVisible(true);
setTitle("Candidate Information");
j1=new JPanel();
j2=new JPanel();
j3=new JPanel();
j4=new JPanel();
bg=new ButtonGroup();
l1=new JLabel("First Name");
l2=new JLabel("Last Name");
l3=new JLabel("Address");
l4=new JLabel("Mobile No");
l5=new JLabel("Gender");
l6=new JLabel("Your Interest");
b1=new JButton("Submit");
b2=new JButton("Reset");
t1=new JTextField(20);
t2=new JTextField(20);
t3=new JTextField(20);
t4=new JTextField(20);
radio1= new JRadioButton("Male");
radio2= new JRadioButton("Female");
bg.add(radio1);
bg.add(radio2);
check1= new JCheckBox("Computer");
check2= new JCheckBox("Sports");
check3= new JCheckBox("Music");
j1.add(l1);
j1.add(t1);
j1.add(l2);
j1.add(t2);
j1.add(l3);
j1.add(t3);
j1.add(l4);
j1.add(t4);
add(j1);
j2.add(l5);
j2.add(radio1);
j2.add(radio2);
add(j2);
j3.add(l6);
j3.add(check1);
j3.add(check2);
j3.add(check3);
add(j3);
j4.add(b1);
j4.add(b2);
add(j4);
}
public static void main(String args[]) {
new SwingCan();
}}

26.write a java program to create a Student information screen.
Code:
package javaprograms;
import java.awt.*;
import javax.swing.*;
public class student_info_swing extends JFrame {
JLabel l1, l2, l3, l4, l5, l6;
JCheckBox check1, check2, check3;
JTextField t1, t2, t3, t4;
JButton b1, b2;
JRadioButton radio1, radio2;
Container contentPane;
ButtonGroup bg;
JPanel j1, j2, j3, j4;
public student_info_swing() {
setLayout(new GridLayout(4,1));
setSize(400, 400);
setTitle("Candidate Info");
setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
j1 = new JPanel();
j2 = new JPanel();
j3 = new JPanel();
j4 = new JPanel();
l1 = new JLabel("First Name:");
l2 = new JLabel("Last Name:");
l3 = new JLabel("Mobile Number:");
l4 = new JLabel("Address:");
l5 = new JLabel("Gender:");
l6 = new JLabel("Your Interests:");
t1 = new JTextField(10);
t2 = new JTextField(10);
t3 = new JTextField(10);
t4 = new JTextField(10);
radio1 = new JRadioButton("Male");
radio2 = new JRadioButton("Female");
bg = new ButtonGroup();
bg.add(radio1);
bg.add(radio2);
check1 = new JCheckBox("Computer");
check2 = new JCheckBox("Sports");
check3 = new JCheckBox("Music");
b1 = new JButton("Submit");
b2 = new JButton("Reset");
j1.add(l1);
j1.add(t1);
j1.add(l2);
j1.add(t2);
j1.add(l3);
j1.add(t3);
j1.add(l4);
j1.add(t4);
j2.add(l5);
j2.add(radio1);
j2.add(radio2);
j3.add(l6);
j3.add(check1);
j3.add(check2);
j3.add(check3);
j4.add(b1);
j4.add(b2);
add(j1);
add(j2);
add(j3);
add(j4);
setVisible(true);
}
public static void main(String[] args) {
new student_info_swing();
}
}

27.Write a JDBC program to Store details of Employees(Empno,Empname,salary,dept). Code:
package javaprograms;
import java.sql.*;
import java.io.*;
import java.util.*;
public class JDBCStudent {
public static void main(String[] args)throws SQLException,ClassNotFoundException {
Class.forName("com.mysql.cj.jdbc.Driver");
System.out.println("JDBC not registerd");
System.out.println("jdbc registered");
String url = "jdbc:mysql://root@localhost:3306/crud";
String insertQuery = "INSERT INTO Employee (Empno, Empname, Salary, Dept) VALUES (?, ?, ?, ?)";
try (
Connection conn = DriverManager.getConnection(url);
PreparedStatement pstmt = conn.prepareStatement(insertQuery);
Scanner sc = new Scanner(System.in)
) {
System.out.print("Enter Employee Number: ");
int empno = sc.nextInt();
sc.nextLine(); // consume newline
System.out.print("Enter Employee Name: ");
String empname = sc.nextLine();
System.out.print("Enter Salary: ");
double salary = sc.nextDouble();
sc.nextLine(); // consume newline
System.out.print("Enter Department: ");
String dept = sc.nextLine();
// Set parameters
pstmt.setInt(1, empno);
pstmt.setString(2, empname);
pstmt.setDouble(3, salary);
pstmt.setString(4, dept);
// Execute update
int rowsInserted = pstmt.executeUpdate();
if (rowsInserted > 0) {
System.out.println("Employee details inserted successfully!");
}
} catch (Exception e) {
 e.printStackTrace();
}}
}

28.Write a JDBC program to display details of students on Screen.
Code:
package javaprograms;

import java.sql.*;

public class JDBCStudentScreen {
public static void main(String[] args) throws SQLException, ClassNotFoundException {
Class.forName("com.mysql.cj.jdbc.Driver");
System.out.println("JDBC Registered");
String url = "jdbc:mysql://localhost:3306/crud";
String user = "root";
String password = "";
String selectQuery = "SELECT id, name, age, course, marks FROM students";

try (
Connection conn = DriverManager.getConnection(url, user, password);
Statement stmt = conn.createStatement();
ResultSet rs = stmt.executeQuery(selectQuery)
) {
System.out.println("Student Details:");
while (rs.next()) {
int rollNo = rs.getInt("id");
String name = rs.getString("name");
int age = rs.getInt("age");
String course = rs.getString("course");
double marks = rs.getDouble("marks");
System.out.println("Roll No: " + rollNo);
System.out.println("Name: " + name);
System.out.println("Age: " + age);
System.out.println("Course: " + course);
System.out.println("Marks: " + marks);
System.out.println("--------------------");
}
} catch (Exception e) {
e.printStackTrace();
}
}
}

29.Create Simple AWT window with Label and button on button click display message.
Code:
package javaprograms;
import java.awt.*;
import java.awt.event.*;
public class click_button extends Frame implements ActionListener {
Label label;
Button button;
click_button() {
setTitle("Simple AWT Example");
setLayout(new FlowLayout());
label = new Label("Click the button to see a message");
button = new Button("Click Me");
add(label);
add(button);
button.addActionListener(this);
setSize(300, 150);
setVisible(true); 
addWindowListener(new WindowAdapter() {
public void windowClosing(WindowEvent e) {
dispose();
}
});
} 
public void actionPerformed(ActionEvent e) {
label.setText("Button Clicked! Hello from AWT!");
} 
public static void main(String[] args) {
new click_button();
}
}

30.Create menubar with menuItem and menuItemList.
Code:
package javaprograms;
import java.awt.*;
import java.awt.event.*;
public class menu_frame extends Frame implements ActionListener {
MenuBar menuBar;
Menu fileMenu, editMenu, helpMenu;
MenuItem newItem, openItem, saveItem, exitItem;
MenuItem cutItem, copyItem, pasteItem;
MenuItem aboutItem;
Label label;
menu_frame() {
// Frame settings
setTitle("AWT MenuBar Example");
setSize(500, 300);
setLayout(new FlowLayout());
// Label
label = new Label("Choose a menu item...");
add(label); 
// Create MenuBar
menuBar = new MenuBar(); 
// Menus
fileMenu = new Menu("File");
editMenu = new Menu("Edit");
helpMenu = new Menu("Help"); 
// File MenuItems
newItem = new MenuItem("New");
openItem = new MenuItem("Open");
saveItem = new MenuItem("Save");
exitItem = new MenuItem("Exit"); 
// Add File items
fileMenu.add(newItem);
fileMenu.add(openItem);
fileMenu.add(saveItem);
fileMenu.addSeparator();
fileMenu.add(exitItem); 
// Edit MenuItems
cutItem = new MenuItem("Cut");
copyItem = new MenuItem("Copy");
pasteItem = new MenuItem("Paste"); 
// Add Edit items
editMenu.add(cutItem);
editMenu.add(copyItem);
editMenu.add(pasteItem); 
// Help MenuItems
 aboutItem = new MenuItem("About");
helpMenu.add(aboutItem); 
// Add Menus to MenuBar
menuBar.add(fileMenu);
menuBar.add(editMenu);
menuBar.add(helpMenu); 
// Attach MenuBar to Frame BEFORE making it visible
setMenuBar(menuBar); 
// Add ActionListeners
newItem.addActionListener(this);
openItem.addActionListener(this);
saveItem.addActionListener(this);
exitItem.addActionListener(this);
cutItem.addActionListener(this);
copyItem.addActionListener(this);
pasteItem.addActionListener(this);
aboutItem.addActionListener(this); 
// Handle window close
addWindowListener(new WindowAdapter() {
public void windowClosing(WindowEvent e) {
System.exit(0);
}
});
// Make frame visible after adding everything
setVisible(true);
} 
public void actionPerformed(ActionEvent e) {
String command = e.getActionCommand();
if (command.equals("Exit")) {
System.exit(0);
} else {
label.setText("You clicked: " + command);
}
} 
public static void main(String[] args) {
new menu_frame();
}
}

31. Create a Java Program using swings to display popup menu.
import javax.swing.*;
import java.awt.event.*;
public class PopupMenuExample {
      public static void main(String[] args) {

        // Create JFrame
        JFrame frame = new JFrame("Popup Menu Example");

        // Create Popup Menu
        JPopupMenu popupMenu = new JPopupMenu();

        // Create Menu Items
        JMenuItem cut = new JMenuItem("Cut");
        JMenuItem copy = new JMenuItem("Copy");
        JMenuItem paste = new JMenuItem("Paste");

        // Add menu items to popup menu
        popupMenu.add(cut);
        popupMenu.add(copy);
        popupMenu.add(paste);

        // Add Mouse Listener to show popup menu on right click
        frame.addMouseListener(new MouseAdapter() {
            public void mousePressed(MouseEvent e) {
                if (e.isPopupTrigger()) {
                    popupMenu.show(e.getComponent(), e.getX(), e.getY());
                }
            }

            public void mouseReleased(MouseEvent e) {
                if (e.isPopupTrigger()) {
                    popupMenu.show(e.getComponent(), e.getX(), e.getY());
                }
            }
        });

        // Frame settings
        frame.setSize(400, 300);
        frame.setLayout(null);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }
}




