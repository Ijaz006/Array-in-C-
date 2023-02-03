# Array-in-C++
//
//  main.cpp
//  array s1
//
//  Created by Ijaz Tufail on 26/09/2022.
//




#include <iostream>
#include <cstdlib>
using namespace std;
class Array{
private:
    int *ptr1,*ptr2,*temp;
    
   
    int  arr[5];
    int  array[5];
    int arrray[5];
    int count;
    int count1;
    int at_same_position_same_elements;
    int   Same_Numbers;
    
public:
  
    
   Array( ){
       Same_Numbers=0;
        ptr1=NULL;
        ptr2=NULL;
        count=0;
        at_same_position_same_elements=0;
    }
    
        
    
    void add( ){
        ptr1=arr;
        cout<<" enter data in arr Array"<<endl;
        for( int i=0;i<6;i++){
            cin>>*ptr1;
            ptr1++;
            //count1++;
            
        }
        ptr2=array;
        cout<<" enter data in array Array"<<endl;
        for( int i=0;i<6;i++){
            cin>>*ptr2;
            ptr2++;
            count++;

        }
        
    }
    void print( ){
        ptr2=array;
        ptr1=arr;
        for( int i=0;i<6;i++){
            cout<<*ptr1<<" \t";
            ptr1++;
            
        }
        cout<<endl;
        
        for( int i=0;i<6;i++){
            cout<<*ptr2<<"\t";
            ptr2++;

        }
    }
        void check( ){
            ptr1=arr;
            ptr2=array;
//            if( arr==NULL or array==NULL){
//                cout<<"cant campare"<<endl;
//            }
            for( int i=0;i<6;i++){
                if(*ptr1==*ptr2){
                    at_same_position_same_elements++;
                    ptr1++;
                    ptr2++;
                }
                ptr1++;
                ptr2++;
                
                
            }
            cout<<" at_same_position_same_elements  "<<          at_same_position_same_elements<<endl;
        }
    void same ( ){
        ptr1=arr;
     
        for(int i=0;i<6;i++ ){
            ptr2=array;
            for( int j=0;j<6;j++){
                
                if(*ptr1==*ptr2){
                    Same_Numbers++;
                    ptr2++;
                }
                ptr2++;
            }
            ptr1++;
        }
        cout<<" same elements "<< Same_Numbers<<endl;
    }
    void sort( ){
        ptr1=arr;
     
        for (int i = 0; i <=6; i++) {

               for (int j = i + 1; j <=6; j++) {

                   if (*(ptr1 + i) < *(ptr1 + j)) {

                      int  t = *(ptr1 + i);

                       *(ptr1 + i) = *(ptr1 + j);

                       *(ptr1 + j) = t;

                   }

               }

           }
        cout<<endl;
        ptr2=array;
        
        for (int i = 0; i <= 6; i++) {

               for (int j = i + 1; j <= 6; j++) {

                   if (*(ptr2 + i) < *(ptr2 + j)) {

                      int  t = *(ptr2 + i);

                       *(ptr2 + i) = *(ptr2 + j);

                       *(ptr2 + j) = t;

                   }

               }

           }

           
        }
    void same_mov_to_third_array( ){
        ptr1=arr;
        temp=arrray;
        for(int i=0;i<6;i++ ){
            ptr2=array;
            for( int j=0;j<6;j++){
                
                if(*(ptr1+i)==*(ptr2)){
                    *temp=*ptr2;
                    ptr2++;
                    count1++;
                    temp++;
                }
                ptr2++;
            }
            ptr1++;
        }
        cout<<endl;
        temp=arrray;
        for ( int i=0;i<count1;i++){
            cout<<*temp<<" \t ";
            temp++;
        }
    }
    
        
    
    
    
        
};


int main( ){
    Array l1;
    l1.add();
    
   // l1.check();
   // l1.same();
    l1.sort();
    l1.print();
    l1.same_mov_to_third_array();
    
  
    

    
    
}
