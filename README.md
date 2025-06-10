1.public class Eligibility {
public static void checkEligibility(int age) {
if (age >= 18)
System.out.println("Eligible to vote");
else
System.out.println("Not eligible to vote");
}
public static void main(String[] args) {
checkEligibility(17);
}
}
2.1.public class EvenOdd {
public static void checkEvenOdd(int num) {
if (num % 2 == 0)
System.out.println(num + " is Even");
else
System.out.println(num + " is Odd");
}
public static void main(String[] args) {
checkEvenOdd(9);
}
}
2.2.EvenOddTest
import org.junit.Test;
public class EvenOddTest {
@Test
public void testEven() {
EvenOdd.checkEvenOdd(8); // Expect "8 is Even"
}
@Test
public void testOdd() {
EvenOdd.checkEvenOdd(9); // Expect "9 is Odd"
}
}
3.1.public class Calculator {
public static int add(int a, int b) { return a + b; }
public static int subtract(int a, int b) { return a - b; }
public static int multiply(int a, int b) { return a * b; }
public static double divide(int a, int b) {
return (b == 0) ? 0 : (double) a / b;
}
public static void performOperations() {
int a = 10, b = 5;
System.out.println("Add: " + add(a, b));
System.out.println("Subtract: " + subtract(a, b));
System.out.println("Multiply: " + multiply(a, b));
System.out.println("Divide: " + divide(a, b));
}
public static void main(String[] args) {
performOperations();
}
}
3.2.test
import static org.junit.Assert.*;
import org.junit.Test;
public class CalculatorTest {
@Test
public void testAdd() {
assertEquals(15, Calculator.add(10, 5));
}
@Test
public void testSubtract() {
assertEquals(5, Calculator.subtract(10, 5));
}
@Test
public void testMultiply() {
assertEquals(50, Calculator.multiply(10, 5));
}
@Test
public void testDivide() {
assertEquals(2.0, Calculator.divide(10, 5), 0.01);
}
@Test
public void testDivideByZero() {
assertEquals(0.0, Calculator.divide(10, 0), 0.01);
}
}
4.
public class Swap {
public static void swapNumbers(int a, int b) {
System.out.println("Before Swap: a=" + a + " b=" + b);
int temp = a;
a = b;
b = temp;
System.out.println("After Swap: a=" + a + " b=" + b);
}
public static void main(String[] args) {
swapNumbers(10, 20);
}
}
5
public class NumberCheck {
public static void checkNumber(int num) {
if (num > 0)
System.out.println("Positive");
else if (num < 0)
System.out.println("Negative");
else
System.out.println("Zero");
}
public static void main(String[] args) {
checkNumber(-3);
}
}
6.
public class SimpleInterest {
public static double calculateSI(double p, double r, double t) {
return (p * r * t) / 100;
}
public static void main(String[] args) {
double result = calculateSI(1000, 5, 2);
System.out.println("Simple Interest: " + result);
}
}
7.
public class Largest {
public static int findLargest(int a, int b, int c) {
int max = a;
if (b > max) max = b;
if (c > max) max = c;
return max;
}
public static void main(String[] args) {
int result = findLargest(12, 45, 33);
System.out.println("Largest: " + result);
}
}
8.
public class ArrayOperations {
public static void calculateStats(int[] arr) {
int sum = 0, min = arr[0], max = arr[0];
for (int n : arr) {
sum += n;
if (n < min) min = n;
if (n > max) max = n;
}
double avg = (double) sum / arr.length;
System.out.println("Sum: " + sum);
System.out.println("Average: " + avg);
System.out.println("Min: " + min);
System.out.println("Max: " + max);
}
public static void main(String[] args) {
int[] numbers = {5, 12, 7, 3, 18};
calculateStats(numbers);
}
}
Admin@123
cf963257b534462a9d7c5e4ced74b88a
