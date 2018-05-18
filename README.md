1.	Write a program to print factorial of N ( without using any loop)


package Sample;

import java.lang.Math;
import java.util.Scanner; 
//headers MUST be above the first class

//one class needs to have a main() method
public class Example
{
// arguments are passed using the text field below this editor
public static void main(String[] args)
{
Scanner sc=new Scanner(System.in);  	
 int i,fact=1; 
 System.out.println("Enter a number");  
int number=sc.nextInt();      
fact = factorial(number);   
System.out.println("Factorial of "+number+" is: "+fact);    

}

static int factorial(int n){    
 if (n == 0)    
return 1;    
else    
return(n * factorial(n-1));    

}
}


2.	There is an animal class which has the common characteristics of all animals. Dog, Horse, Cat are animals(sub-class). Each can shout, but each shout is different. Use polymorphism to create objects of same and using an animal variable, make each of the animals shout.

package Sample;

public class Example {
    public static void main(String[] args){
        Animal obj1 = new Dog();
        Animal obj2 = new Cat();
        Animal obj3 = new Horse();
        obj1.shout(); //output is bark..
        obj2.shout(); //output is bark..  
         obj3.shout();
    }   
}

class Animal{
    public void shout(){
        System.out.println("Parent animal's shout");
    }       
}

class Dog extends Animal{
    public void shout(){
        System.out.println("bark..");
    }
}

class Cat extends Animal{
    public void shout(){
        System.out.println("Meaw..");
    }
}

class Horse extends Animal{
    public void shout(){
        System.out.println("neigh");
    }
}


3.	Create an abstract class Instrument which is having the abstract function play.  Create three more sub classes from Instrument which is Piano, Flute, Guitar. Override the play method inside all three classes printing a message 
             “Piano is playing  tan tan tan tan  ”  for Piano class
              “Flute is playing  toot toot toot toot”  for Flute class
              “Guitar is playing  tin  tin  tin ”  for Guitar class 
      Create an array of 10 Instruments.
      Assign different type of instrument to Instrument reference.
     Check for the polymorphic behavior of  play method.


Ans: package music;

      public interface Playable {
	
     	public void play();
		
          }
          
 package music.string;
import music.Playable;

public class Veena implements Playable
{

	public static Veena obj;
	public void play() {
		System.out.println("Playing Veena");
		
	}
}

package music.wind;
import music.Playable;

public class Saxophone implements Playable{

	public static Saxophone obj1;
	public void play() {
		System.out.println("playing Saxophone");
		
	}
}

package live;

import music.Playable;
import music.string.Veena;
import music.wind.Saxophone;

public class Test {

	
	public static void main(String args[])
	{
		Playable p=new Veena();	
		Playable p1=new Saxophone();	
		p1.play();
		p.play();
	}
}


6.	Write  a  program  to  assign  the  current  thread  to  t1.  Change  the  name  of  the  thread  to  MyThread.  Display  the  changed  name  of  the  thread.  Also  it  should  display  the  current  time.  Put  the  thread  to  sleep  for  10  seconds  and  display  the  time  again.


package Sample;

import java.text.SimpleDateFormat;
import java.util.Date;


class Multi extends CurrentThread
{
	public void run(){
		System.out.println("thread is running");
}
public String setName(String string) {
	return string;
	
}

public String getName() {
    return "swathi";
}

public void start() {
	System.out.println("thread is running");
	
}
}
public class Example{
	
public static void main(String args[])
{
Multi t1=new Multi();
t1.start();
System.out.println("Name of t1:"+t1.getName());
t1.setName("MyThread");
System.out.println("After changing name of t1:"+t1.setName("Ammu"));
}
} 




