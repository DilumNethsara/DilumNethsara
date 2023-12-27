public class QuickSort{

	public static void swap(int arr[],int a,int b){
		int temp=arr[a];
		arr[a]=arr[b];
		arr[b]=temp;
	}
	
	public static void quick(int arr[],int start,int end){  
		
		if(start>=end){         
			return;
		}
		
		int i=start,j=end; 
		int pivot=arr[end];
		
		while(i<j)
		{
			while(arr[i]<pivot && i<j)
			{
				i++;
			}
			
			while(arr[j]>=pivot && i<j)
			{
				j--;
			}
			
			swap(arr,i,j);
		}
		swap(arr,i,end);
		
		quick(arr,start,i-1);
		quick(arr,i+1,end);
		
		
	}

}










public class SelectionSort{
	
	public static void selectionSorting(int arr[])
	{
		int n=arr.length;
		
		for(int i=0; i<n-1; i++)
		{
			int min=i;
			for(int j=i+1; j<n; j++)
			{
				if(arr[min]>arr[j])
					min=j;
			}
			
			if(min!=i)
			{
				int temp=arr[i];
				arr[i]=arr[min];
				arr[min]=temp;
			}
		}
	}
}






public class InsertionSort {  

    public static void insertionSort(int array[]) {  
        int n = array.length;  
        for (int j = 1; j < n; j++) {  
            int temp = array[j];  
            int i = j-1;  
            while ( (i >= 0) && ( array [i] > temp ) ) {  
                array [i+1] = array [i];  
                i--;  
            }  
            array[i+1] = temp;  
        }  
    } 
}
