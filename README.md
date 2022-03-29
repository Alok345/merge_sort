# merge_sort
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int arr[]={10,12,11,5,13,6,8,9};
    int arr_size=sizeof(arr) / sizeof(arr[0]);
    printf("given array is \n");
    printarray(arr,arr_size);
    mergeSort(arr,0,arr_size-1);
    printf("\nsorted array is \n");
    printarray(arr,arr_size);
return 0;
}
void merge(int arr[],int l,int m,int r){
    int i,j,k;
    int n1=m-l+1;
    int n2=r-m;
    int L[n1],R[n2];
    for( i=0;i<n1;i++){
        L[i]=arr[l+i];
    }
    for( j=0;j<n2;j++){
        R[j]=arr[m+j];
    }
    i=0;
    j=0;
    k=l;
    for(k=l;k<r;k++){
        if(L[i]<=R[j]){
            A[k]=L[i];
            i++
        }
        else{
            A[k]=R[j];
            j++;
        }
    }
}
void mergeSort(int arr[],int l,int r){
    if(l<r){
        int m=(l+r)/2;
        mergeSort(arr,l,m);
        mergeSort(arr,m+1,r);
        merge(arr,l,m,r);
    }
}
void printarray(int A[],int size){
    int i;
    for( i=0;i<size;i++){
        printf("\t%d \t",A[i]);
    }
    printf("\n");
}
