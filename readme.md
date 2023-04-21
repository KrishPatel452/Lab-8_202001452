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


![image](https://user-images.githubusercontent.com/123479469/233023817-b63fa106-04dc-421e-9471-cf67d75805d8.png)

3. Created junit test case for class Boa - BoaTest and for test method stubs, select both isHealthy() and fitsInCage(int).

4. Added unit tests - 

Method annotated with @Before will be run before each test executes.

<pre>
package lab8;

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	
	private Boa jen;
	private Boa ken;

	@Before
	public void setUp() throws Exception {
		//initialization
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}
}
</pre>

![image](https://user-images.githubusercontent.com/123479469/233039973-f0cb5ba9-235f-44ae-a5b1-dabd636ca229.png)

5. Added private fields for jen and ken in the Boa class.

<pre>
private Boa jen;
private Boa ken;
</pre>

We added private fields for jen and ken to the BoaTest class, and initialized them in the setUp method. We also updated the testIsHealthy and testFitsInCage methods to use these Boa objects for testing.

Note that the setUp method will be executed before each test method, so any changes made to the Boa objects during a test will not affect the objects used in other tests.

![image](https://user-images.githubusercontent.com/123479469/233040296-b6ab4813-e28d-43d8-858f-d107a7785059.png)

