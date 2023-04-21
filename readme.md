# Lab-8_202001452

# Unit Testing with JUnit

## Goal:
The goal of this lab is to learn how to use JUnit to write unit tests for Java programs.

# Lab Exercises

1. Created a new Eclipse project - nehalab8 and within that created a package - nehalab8

2. Created a class in the package - class name - Boa and junit test case file - BoaTest

<pre>
package lab8;

public class Boa {
	private String name;
	private int length; // the length of the boa, in feet
	private String favoriteFood;
	
	public Boa (String name, int length, String favoriteFood){
		this.name = name;
		this.length = length;
		this.favoriteFood = favoriteFood;
	}
	// returns true if this boa constrictor is healthy
	public boolean isHealthy(){
		return this.favoriteFood.equals("granola bars");
	}
	
	// returns true if the length of this boa constrictor is
	// less than the given cage length
	public boolean fitsInCage(int cageLength){
		return this.length < cageLength;
	}
  }
</pre>
