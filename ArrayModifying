package array.modifying;

import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.ObjectInputStream;
import java.io.ObjectOutputStream;
import java.io.Serializable;
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class ArrayModifying implements Serializable {
	static int n;
	static Scanner sc = new Scanner(System.in);
	static StringBuffer sb = new StringBuffer();
	static List<Integer> list = new ArrayList<Integer>();
	static int[] array = new int[10];
	static int optionValue = 0;
	static int option = 0;

	/** Array Element */
	public static int printInputArray(int n) {
		System.out.println("Array elements are: ");
		for (int i = 0; i < n; i++) {
			list.add(array[i]);
			System.out.print(array[i] + ",");
		}
		return 0;
	}

	/** Options */
	public static int getOption() {
		System.out.println("Modify an array element then press 1");
		System.out.println("Search an element then press 2");
		System.out.println("Exit then press 3");
		sc = new Scanner(System.in);
		optionValue = sc.nextInt();
		return optionValue;
	}

	/** Option 1 */
	public static int modifyingArray() {
		sc = new Scanner(System.in);
		System.out.println("Update single element then press 1");
		System.out.println("Replace all elements then press 2");
		System.out.println("Go back then press 3");
		int optionValue2 = sc.nextInt();
		return optionValue2;
	}

	/** Option A update single element */
	public static int updateSingleValue() {
		System.out.print("Enter the number you want to change");
		int changeNumber = sc.nextInt();
		sb.append(changeNumber);
		System.out.print("Enter the number you entered in replace of this number");
		int changeNumber1 = sc.nextInt();
		sb.append(changeNumber1);
		for (Integer l : list) {
			if (l == changeNumber) {
				l = changeNumber1;
				sb.append(l);
			}
			sb.append(l);
			System.out.print(l + ",");
		}
		return 0;
	}

	/** Option B Replace all */
	public static int replaceAll(List<Integer> list) {
		System.out.println("this is old array");
		System.out.println(list.toString());
		return 0;
	}

	/** Option C Go back */
	public static int goBack() {
		return 0;
	}

	/** Option 2 Exist method */
	public static int searchKeyElement(int keyElement, List<Integer> list) {
		for (int i = 1; i < list.size(); i++) {
			if(list.get(i) == keyElement) {
				System.out.println("Element " + keyElement + " found at " + i + " position");
				break;
			} else {
				System.out.println("Element " + keyElement + " not found");
			}
		}
		return -1;
	}

	/** Option 3 Exist method */
	public static int getExit() {
		System.out.println("You has been exist");
		System.out.println("for Trace then press -1");
		int exist = sc.nextInt();
		return exist;
	}

	/** Option 4 Trace method */
	public static void getTrace() {
		//deserializationBean();
		System.out.println("Your Trace Value  :" + sb.toString());
	}

	/** Option 4 Trace method */
	public static void wantToTrace() {
		System.out.println(" For Trace press -1 ");
		int trace = sc.nextInt();
		if (trace == -1) {
			getTrace();
		} else {
			System.out.println("You are entered wrong number.");
		}
	}

	/** Return to Option 1 */
	public static void returnOption1() {
		modifyingArray();
	}
	
	/** Deserialization Object */
	/*public static void deserializationBean() {
		ArrayModifying am=null;
		try
        {
            FileInputStream fis = new FileInputStream("C:/Users/Gaurav/Desktop/PDF File/array-modifying.txt");
            ObjectInputStream ois = new ObjectInputStream(fis);
            am = (ArrayModifying)ois.readObject();
        }
        catch (Exception e)
        {
           e.printStackTrace(); 
           System.out.println("this is desializable"+am.toString());
        }
	}*/

public static void main(String[] args) {
		 
		 System.out.print("Enter the number of elements you want to store: "); 
		 sb.append("Enter the number of elements you want to store: ");
		 n=sc.nextInt();  
	 
		 System.out.println("Enter the elements of the array: ");
		 sb.append("Enter the elements of the array: ");
		 for(int i=0; i<n; i++){ 
			 sb.append(i);
			 array[i]=sc.nextInt();  
		 }
		 printInputArray(n);
		 System.out.println();
		 
		 option = getOption();
		 
		 if(option==1) {
			 int modifyingArray = modifyingArray();
			 if(modifyingArray==1) {
				 int updateSingleValue = updateSingleValue();
				 if(updateSingleValue==0) {
					 returnOption1();
				 }else {
					 getTrace();
				 }
			 }else if(modifyingArray==2) {
				 int replaceAll = replaceAll(list);
				 if(replaceAll==0) {
					 returnOption1();
				 }else {
					 getTrace(); 
				 }
			 }else if(modifyingArray==3) {
				 int goBack = goBack();
				 if(goBack==0) {
					 returnOption1();
				 }else {
					 getTrace();  
				 }
			 }else {
				 System.out.println("You are entered wrong number."); 
			 }
		 }else if(option==2) {
			 System.out.println("Enter search element");
			 int searchElement = sc.nextInt();
			searchKeyElement(searchElement,list);
			 wantToTrace(); 
		 }else if(option==3) {
			 int exit = getExit();
			 if(exit== -1) {
				 getTrace(); 
			 }else {
				 System.out.println("You are entered wrong number."); 
			 }
		 }else {
			 System.out.println("You are entered wrong number.");
		 }

		/*try
		{
			ArrayModifying am = new ArrayModifying();
			FileOutputStream fos = new FileOutputStream("C:/Users/Gaurav/Desktop/PDF File/array-modifying.txt");
			ObjectOutputStream oos = new ObjectOutputStream(fos);
			oos.writeObject(am);
			oos.flush();
			oos.close();
		}catch(
		Exception e)
		{
			System.out.println(e);
		}*/
	
	}

}
