import java.util.Arrays;

class GFG {
	public static void main(String args[])
	{
		int[] arr = { 5, -2, 23, 7, 87, -42, 509 };
		System.out.println("The original array is: ");
		for (int num : arr) {
			System.out.print(num + " ");
		}
		Arrays.sort(arr);
		System.out.println("\nThe sorted array is: ");
		for (int num : arr) {
			System.out.print(num + " ");
		}
	}
}


// Java Program to Sort Array of Integers
// by Default Sorts in an Ascending Order
// using Arrays.sort() Method

// Importing Arrays class from the utility class
import java.util.Arrays;

// Main class
public class GFG {

	// Main driver method
	public static void main(String[] args)
	{
		// Custom input array
		int[] arr = { 13, 7, 6, 45, 21, 9, 101, 102 };

		// Applying sort() method over to above array
		// by passing the array as an argument
		Arrays.sort(arr);

		// Printing the array after sorting
		System.out.println("Modified arr[] : "
						+ Arrays.toString(arr));
	}
}




// Java program to Sort a Subarray in Array
// Using Arrays.sort() method

// Importing Arrays class from java.util package
import java.util.Arrays;

// Main class
public class GFG {

	// Main driver method
	public static void main(String[] args)
	{
		// Custom input array
		// It contains 8 elements as follows
		int[] arr = { 13, 7, 6, 45, 21, 9, 2, 100 };

		// Sort subarray from index 1 to 4, i.e.,
		// only sort subarray {7, 6, 45, 21} and
		// keep other elements as it is.
		Arrays.sort(arr, 1, 5);

		// Printing the updated array which is
		// sorted after 2 index inclusive till 5th index
		System.out.println("Modified arr[] : "
						+ Arrays.toString(arr));
	}
}



// Java program to Sort a Subarray in Descending order
// Using Arrays.sort()

// Importing Collections class and arrays classes
// from java.util package
import java.util.Arrays;
import java.util.Collections;

// Main class
public class GFG {

	// Main driver method
	public static void main(String[] args)
	{
		// Note that we have Integer here instead of
		// int[] as Collections.reverseOrder doesn't
		// work for primitive types.
		Integer[] arr = { 13, 7, 6, 45, 21, 9, 2, 100 };

		// Sorts arr[] in descending order using
		// reverseOrder() method of Collections class
		// in Array.sort() as an argument to it
		Arrays.sort(arr, Collections.reverseOrder());

		// Printing the array as generated above
		System.out.println("Modified arr[] : "
						+ Arrays.toString(arr));
	}
}






// Java program to sort an array of strings
// in ascending and descending alphabetical order
// Using Arrays.sort()

// Importing arrays and Collections class
// from java.util class
import java.util.Arrays;
import java.util.Collections;

// Main class
public class GFG {

	// Main driver method
	public static void main(String[] args)
	{
		// Custom input string
		String arr[] = { "practice.geeksforgeeks.org",
						"www.geeksforgeeks.org",
						"code.geeksforgeeks.org" };

		// Sorts arr[] in ascending order
		Arrays.sort(arr);
		System.out.println("Modified arr[] : "
						+ Arrays.toString(arr));

		// Sorts arr[] in descending order
		Arrays.sort(arr, Collections.reverseOrder());

		// Lastly printing the above array
		System.out.println("Modified arr[] :"
						+ Arrays.toString(arr));
	}
}






// Java program to demonstrate Working of
// Comparator interface

// Importing required classes
import java.io.*;
import java.lang.*;
import java.util.*;

// Class 1
// A class to represent a student.
class Student {
	int rollno;
	String name, address;

	// Constructor
	public Student(int rollno, String name, String address)
	{
		// This keyword refers to current object itself
		this.rollno = rollno;
		this.name = name;
		this.address = address;
	}

	// Used to print student details in main()
	public String toString()
	{
		return this.rollno + " " + this.name + " "
			+ this.address;
	}
}

// Class 2
// Helper class extending Comparator interface
class Sortbyroll implements Comparator<Student> {
	// Used for sorting in ascending order of
	// roll number
	public int compare(Student a, Student b)
	{
		return a.rollno - b.rollno;
	}
}

// Class 3
// Main class
class GFG {

	// Main driver method
	public static void main(String[] args)
	{
		Student[] arr
			= { new Student(111, "bbbb", "london"),
				new Student(131, "aaaa", "nyc"),
				new Student(121, "cccc", "jaipur") };

		System.out.println("Unsorted");

		for (int i = 0; i < arr.length; i++)
			System.out.println(arr[i]);

		// Sorting on basic as per class 1 created
		// (user-defined)
		Arrays.sort(arr, new Sortbyroll());

		System.out.println("\nSorted by rollno");

		for (int i = 0; i < arr.length; i++)
			System.out.println(arr[i]);
	}
}




// This will sort the array in the descending order
/*package whatever //do not write package name here */
import java.util.Arrays;
import java.util.Collections;
public class GFG {
	public static void main(String[] args)
	{
		Integer[] array
			= { 99, 12, -8, 12, 34, 110, 0, 121, 66, -110 };

		Arrays.sort(array, Collections.reverseOrder());
		System.out.println(
			"Array in descending order: "
			+ Arrays.toString(array));
	}
}



