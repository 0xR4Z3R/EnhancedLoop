# EnhancedLoop


public class EnhancedLoop{
	
	public static void main(String[] args) {
		
		int[] list ={1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
		int sum = sumListEnhanced(list);
		System.out.println("Sum of elements in list: " + sum);
		
		System.out.println("Original List");
		printList(list);
		System.out.println("--------------");
		System.out.println("Calling addOne");
		addOne(list);
		System.out.println("--------------");
		printList(list);
		System.out.println("Calling addoneError");
		addOneError(list);
		System.out.println("List after call to addOneError. Note elements of list did not change.");
		printList(list);
	}




public static int sumListEnhanced(int[] list)
{
	int total = 0;
	for(int val: list) {
		total += val;
	}
	
	return total;
}

public static void printList(int[] list)
{
	System.out.println("index, value");
	System.out.println("------------ ");
	for(int i=0;i< list.length; i++)
	{
		System.out.println(i+ ", " + list[i]);
	}
}

public static void addOne(int[] list) {
	for(int i=0; i < list.length; i++) {
		list[i]++;
	}
}

public static void addOneError(int[] list)
{	for(int val : list)
	{	val = val + 1;
	}
}



//-----------------------------------------------------------
Testing passing prameter value in differnt method
//----------------------------------------------------------
Output
//------------------------------------------------------------
Sum of elements in list: 55
Original List
index, value
------------ 
0, 1
1, 2
2, 3
3, 4
4, 5
5, 6
6, 7
7, 8
8, 9
9, 10
--------------
Calling addOne
--------------
index, value
------------ 
0, 2
1, 3
2, 4
3, 5
4, 6
5, 7
6, 8
7, 9
8, 10
9, 11
Calling addoneError
List after call to addOneError. Note elements of list did not change.
index, value
------------ 
0, 2
1, 3
2, 4
3, 5
4, 6
5, 7
6, 8
7, 9
8, 10
9, 11



