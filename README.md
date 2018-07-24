#include<iostream>
#include<stdlib.h>

using namespace std;
void SelectionSort (int arr[], int n)
{
	int i, j;
	for (i = 0; i < n; ++i)
	{

		for (j = i+1; j < n; ++j)
		{
			// Comparing consecutive data and switching values if value at i > j.
			if (arr[i] > arr[j])
			{
				arr[i] = arr[i]+arr[j];
				arr[j] = arr[i]-arr[j];
				arr[i] = arr[i]-arr[j];
			}	
		}
		// Value at i will be minimum of all the values above this index.
	}	
}	
 
int insertionSort(int dizi [],int n){
  int min,temp;
  for (int i =0;i<n;i++){
    min=i;
  }
  while (dizi[min]<dizi[min-1]){
    temp = dizi[min];
    dizi[min]=dizi[min-1];
    dizi[min-1]=temp;
    min--;
  }

}
       
 void swap(int *xp, int *yp)
{
    int temp = *xp;
    *xp = *yp;
    *yp = temp;
}
 
// A function to implement bubble sort
void bubbleSort(int arr[], int n)
{
   int i, j;
   for (i = 0; i < n-1; i++)      
 
       // Last i elements are already in place   
       for (j = 0; j < n-i-1; j++) 
           if (arr[j] > arr[j+1])
              swap(&arr[j], &arr[j+1]);
}

     int main() {
    
        int max,x;
        
        cout<<"Enter the size of elements";
       cin>>max;
        
        cout<<"Selection of function  \n 1- Selection Sort \n 2-insertion Sort \n 3-BubleSort";
       cin>>x; 
         int arr[max];
         for (int i = 0; i < max; i++){
            arr[i] = rand() % 1000;
            }

       if (x==1){
           
            cout<<"\nHere are the numbers before selection Sort"<<endl;
            for (int j = 0; j < max; j++){
           
                 cout<<" "<<arr[j];
              }
           SelectionSort(arr,max);
            cout<<"\n After SelectionSort";
            for (int k = 0; k<max; k++){
               cout<<" "<<arr[k];
              }
      }
      else if(x==2){
      
         for (int i = 0; i < max; i++){
            arr[i] = rand()%1000;
            }
            cout<<"Here are the numbers before insertion Sort"<<endl;
            for (int j = 0; j < max; j++){
            
                 cout<<" "<<arr[j];
              }
            insertionSort(arr,max);
            cout<<"\n\n\nAfter the insertion sort";
            for (int k = 0; k<max; k++){
               cout<<" "<<arr[k];
              }
              return 0;
       }
       else if(x==3){

            for (int i = 0; i < max; i++){
            arr[i] = rand()%1000;
            }
            cout<<"Here are the numbers before Buble Sort "<<endl;
            for (int j = 0; j < max; j++){
            
                 cout<<" "<<arr[j];
              }
             int n = sizeof( arr ) / sizeof( *arr );
           bubbleSort(arr, n);
           
              cout<<"\n\nBuble sort";
      
             for (int k = 0; k<max; k++){
               cout<<" "<<arr[k];
              }
        return 0;
       }
     
   }
