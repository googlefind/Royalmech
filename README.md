<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Java Code Snippets</title>
<style>
    pre {
        background-color: #ffffff;
        padding: 1px;
        border-radius: 1px;
        overflow-x: auto;
    }
</style>
</head>
<body style="background-color: white; color: white;">>

<h1>NAVUSA COPY MADTHA IDVI NIVSA MADI</h1>

<button onclick="copyCode(1)">1</button>
<button onclick="copyCode(2)">2</button>
<button onclick="copyCode(3)">3</button>
<button onclick="copyCode(4)">4</button>
<button onclick="copyCode(5)">5</button>
<button onclick="copyCode(6)">6</button>
<button onclick="copyCode(7)">7</button>
<button onclick="copyCode(8)">8</button>
<button onclick="copyCode(9)">9</button>
<pre id="code1">
package quadratic;
import java.util.Scanner;
public class Quadratic 
{
 public static void main(String[] args) 
 {
 double root1, root2,a,b,c,determinant,r;
 Scanner input = new Scanner(System.in);
 System.out.print("Input a: ");
 a = input.nextDouble();
 System.out.print("Input b: ");
 b = input.nextDouble();
 System.out.print("Input c: ");
 c = input.nextDouble();
 determinant = b * b - 4 * a * c;
r=Math.sqrt(determinant);
 
 if (determinant > 0) 
 {
root1 = (-b+r)/(2*a);
 root2 = (-b-r)/(2*a);
 System.out.format("root1 = %.2f and root2 = %.2f\n", root1, root2);
 }
 else if (determinant == 0) 
{
 root1 = root2 = (-b)/(2*a);
 System.out.format("Roots are equal\n");
 System.out.format("root1 = root2 = %.2f\n;", root1);
 }
 else 
 {
 // roots are complex number and distinct
 double real = -b / (2 * a);
 double imaginary = Math.sqrt(-determinant) / (2 * a);
 System.out.format("Roots are imaginary\n");
 System.out.format("root1 = %.2f+%.2fi\n", real, imaginary);
 System.out.format("\nroot2 = %.2f-%.2fi\n", real, imaginary);
 }
 }
}

</pre>

<pre id="code2">
package multiplyarray;
import java.util.Arrays;
public class Multiplyarray {
 public static void main(String[] args) {
 int a1[] = {2,5,-2,10};
 int a2[] = {3,-5,7,1};
 
 for (int i = 0; i < a1.length; i++) {
 a1[i] = a1[i] * a2[i];
 }
 
 for (int i = 0; i < a1.length; i++) 
{
 System.out.print(a1[i] + " ");
 }
 }
}
</pre>

<pre id="code3">
package shiftop;
public class Shiftop 
{
 public static void main(String args[]) {
 byte x, y;
 x = 10;
 y = -10;
 System.out.println("Bitwise Left Shift: x<<2 = " + (x << 2));
 System.out.println("Bitwise Right Shift: x>>2 = " + (x >> 2));
 System.out.println("Bitwise Zero Fill Right Shift: x>>>2 = " + (x >>> 2));
 System.out.println("Bitwise Zero Fill Right Shift: y>>>2 = " + (y >>> 2));
 }
}
</pre>

<pre id="code4">
import java.util.Scanner;
public class ArraySortingExample {
 public static void main(String[] args) {
 Scanner ed = new Scanner(System.in);
 int[] a = new int[50];
 int i, j, temp;
 System.out.println("Please Enter 5 elements in the Array");
 for (i = 0; i < 5; i++) {
 a[i] = ed.nextInt();
 }
 for (i = 0; i < 5; i++) {
 for (j = i + 1; j < 5; j++) {
 if (a[i] > a[j]) {
temp = a[i];
 a[i] = a[j];
 a[j] = temp;
 }
 }
 }
 System.out.println("Sorted Array in Increasing Order:-");
 for (j = 0; j < 5; j++) {
 System.out.println(a[j]);
 }
 for (i = 0; i < 5; i++) {
 for (j = i + 1; j < 5; j++) {
 if (a[i] < a[j]) {
 temp = a[i];
 a[i] = a[j];
 a[j] = temp;
 }
 }
 }
 System.out.println("Sorted Array in Decreasing Order:-");
for (j = 0; j < 5; j++) {
 System.out.println(a[j]);
 }
}
}
</pre>

<pre id="code5">
package studentinfo;
import java.util.Scanner;
class Student {
 private String usn;
 private String name;
 private String branch;
 private String phone;
 private String percentage;
 public void read() {
 Scanner sc = new Scanner(System.in);
 usn = sc.nextLine();
 name = sc.nextLine();
 branch = sc.nextLine();
 phone = sc.nextLine();
 percentage = sc.nextLine();
 }
 public void display() {
 System.out.println(usn + "\t" + name + "\t" + branch + "\t" + phone + "\t" + percentage);
 }
}
public class Studentinfo {
 public static void main(String[] args) {
 System.out.println("Enter the total number of students");
 Scanner sc = new Scanner(System.in);
 int n = sc.nextInt();
 // Create n objects
 Student[] st = new Student[n];
 for (int i = 0; i < st.length; i++) {
 st[i] = new Student(); }
 for (int i = 0; i < n; i++) { System.out.println("Enter USN, Name, Branch, percentage of marks and Phone no. for student " + (i + 1));
st[i].read();
}
 // Display the student information
 System.out.println("USN\tName\tBranch\tPercentage\tPhone");
 for (int i = 0; i < n; i++) {
 st[i].display();
 }
}
}

</pre>

<pre id="code6">
package mco;
class ABC {
 int a, b;
 ABC(int x, int y) {
 a = x;
 b = y;
 System.out.println(" First version of constructor is called");
 System.out.println("values of a and b are\t" + a + " " + b);
 }
 ABC(int x) {
 a = x;
 b = 10;
 System.out.println(" Second version of constructor is called");
 System.out.println("values of a and b are\t" + a + " " + b);
 }
 void meth() {
 System.out.println(" First version of method is called");
 }
 void meth(int x) {
 System.out.println(" Second version of method is called");
 }
}
public class Mco {
 public static void main(String[] args) {
 ABC ob1 = new ABC(20, 20);
 ABC ob2 = new ABC(20);
 ob1.meth();
 ob1.meth(40);
 }
}
</pre>

<pre id="code7">
package dynamicdsp;
abstract class Figure {
 double d1;
 double d2;
Figure(double a, double b) {
 d1 = a;
 d2 = b;
 }
 abstract double area();
}
class Rectangle extends Figure {
 Rectangle(double a, double b) {
 super(a, b);
 }
 double area() {
 System.out.println("Inside Area for Rectangle.");
 return d1 * d2;
 }
}
class Triangle extends Figure {
 Triangle(double a, double b) {
 super(a, b);
 }
 double area() {
 System.out.println("Inside Area for Triangle.");
 return 0.5 * d1 * d2;
 }
}
public class Dynamicdsp {
 public static void main(String[] args) {
 Rectangle r = new Rectangle(5, 10);
 Triangle t = new Triangle(5, 10);
Figure f; //reference only(no object is created)
 f = r;
 System.out.println("Area is " + f.area());
 f = t;
 System.out.println("Area is " + f.area());
 }
}
</pre>

<pre id="code8">
package P1;
public class A {
 protected int a;
 void displayA(){
 System.out.println("class A");
}
 }
public class B extends A{
 public void displayB(){
 a=10;
 System.out.println("Class B:"+" The value of a is "+a);
 }
}
public class C {
 void displayC(){
 System.out.println("Class C");
 }
}
package P2;
import P1.*;
public class D extends A {
 public void displayD(){
 a=100;
 System.out.println("Class D: "+"The value of a is "+a);
} 
}
public class E {
 private void displayE(){
 System.out.println("Class E");
 }
}
package packagesdemo;
import P1.*;
import P2.*;
public class Packagesdemo {
 public static void main(String[] args) {
 B b=new B();
 C c=new C();
 D d=new D();
 E e=new E();
 
 b.displayB(); //public method, protected data member
//error c.displayC(); //default method
 d.displayD(); //public method,protected data member
//error e.displayE(); //private method
}
}

</pre>
<pre id="code9">

import java.util.Scanner;
public class excdemo {
 public static void main(String args[]){
int a,b,result;
Scanner s=new Scanner(System.in);
System.out.println("Enter the value of A and B");
a=s.nextInt();
b=s.nextInt();
try{
  result=a/b;
  int c[]={1};
 c[40]=99;
 } catch(ArithmeticException e){
  System.out.println("Divide by 0:" +e);
 } catch(ArrayIndexOutOfBoundsException e){
System.out.println("Array index out of bound:" +e);
}
System.out.println("After try/catch block:" );
}
}


<button onclick="copyCode(1)">Copy Code 1</button>
<button onclick="copyCode(2)">Copy Code 2</button>
<button onclick="copyCode(3)">Copy Code 3</button>
<button onclick="copyCode(4)">Copy Code 4</button>
<button onclick="copyCode(5)">Copy Code 5</button>
<button onclick="copyCode(6)">Copy Code 6</button>
<button onclick="copyCode(7)">Copy Code 7</button>
<button onclick="copyCode(8)">Copy Code 8</button>
<button onclick="copyCode(9)">Copy Code 9</button>

<script>
function copyCode(id) {
    var code = document.getElementById('code' + id);
    var range = document.createRange();
    range.selectNode(code);
    window.getSelection().removeAllRanges();
    window.getSelection().addRange(range);
    document.execCommand("copy");
    window.getSelection().removeAllRanges();
    alert("Code " + id + " copied to clipboard!");
}
</script> 
<p style="color: red;">created by mr___d</p>
