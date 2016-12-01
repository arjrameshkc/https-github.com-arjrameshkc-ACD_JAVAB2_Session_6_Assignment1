# https-github.com-arjrameshkc-ACD_JAVAB2_Session_6_Assignment1
package Session6_Assignment;

class Timer extends Thread {
	    String threadName;
	    Thread t;
	      
	   
	   public Timer(String threadName) {
			super();
			this.threadName = threadName;
			System.out.println("Timer is : " +  threadName );
		}

	   
	   public void run() {
	     
	      try {
	    	  
	         for(int i = 0; i < 3; i++) {
	            System.out.println("Thread periodically: " + threadName + ", " + i); 
	             
				// Let the thread sleep for a while.
	            Thread.sleep(1000);
	         }
	      }catch (InterruptedException e) {
	         System.out.println("Thread " +  threadName + " interrupted.");
	      }
	      
	   }
	   
	   public void start () {
	
	      if (t == null) {
	         t = new Thread (this, threadName);
	         t.start ();
	      }
	   }
	}
  
  package Session6_Assignment;

public class MainTimer {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Timer T1 = new Timer( "Thread-1");
	      T1.start();
	  	}

}
