convert decimal number to binary
#include <iostream>
#include <math.h>
using namespace std;
int main(){
	int n;
cin>>n;
int ans=0;
int i=0;
while(n!=0){
	int bit=n&1;
	ans=bit*pow(10,i)+ans;
	n=n>>1;//digit/2
	i++;
	
}

cout<<"answeris"<<ans<<endl;	
}
 */ in this question they help u to reverse any number  (123)convert(321)
 or they convert decimal to binary digit like 5=101; for reverse any number 
 we use formula bit = digit (ans= (digit*pow(10,i)+ans) )or for same number
 we use ( ans= ans*10+digit).
it depend on limit of int bit because they stored 32 bitsonly.
  #include <iostream>
#include <math.h>
using namespace std;
int main(){
	int n;
cin>>n;
int ans=0;
int i=0;
while(n!=0){
	int digit=n%10;
	if( digit==1){
		ans=ans+pow(2,i);
	}
	
	n=n/10;//digit/2
	i++;
	
}

cout<<ans<<endl;	
} binary to decimal
 
linked list//
	#include <iostream> 
using namespace std; 
 class Node{
    public:
    int data;
    Node* next;
  Node(int data){
      this -> data = data;
      this -> next = NULL;
  }
    
};

int main() {
     Node*node1=new Node(10);
     cout<<node1->data<<endl;
     cout<<node1->next<<endl;

    return 0;
}
linked list insert and travers
	#include <iostream> 
using namespace std; 
 class Node{
    public:
    int data;
    Node* next;
  Node(int data){
      this -> data = data;
      this -> next = NULL;
  }
    
};
 void insertathead(Node* &head,int d){
     Node*temp= new Node(d);
     temp->next=head;
     head=temp;
 } 
 //travers in linked list
 void print(Node*&head){
     Node*temp=head;
     while(temp!=NULL){
         cout<<temp->data<<" ";
         temp=temp->next;
     } 
     cout<<endl;
 }
      
int main() {
     Node*node1=new Node(10);
     //cout<<node1->data<<endl;
     //cout<<node1->next<<endl;
       Node* head=node1;
       print(head);
       
       insertathead(head,12);
       print(head);

    return 0;
} sum of array in bitwise( example a[5]=1 2 3 4 5.==output 1+2+3+4+5=15 //
	#include <iostream> 
using namespace std;

int main() {
    long n,sum=o;
    cin>>n;
    int arr[n];
    for(i=0;i<n-1;i++){
        cin>>arr[i];
        sum=sum+arr[i];
    } 
    cout<<sum;

    return 0;
 } 
	find first repeating number//in array
	#include <iostream> 
using namespace std;

int main() {
    int n;
    cin>>n;
    int arr[n];
    for (int i=0;i<n;i++){
          cin>>arr[i];
        
    } 
     for(int i=0;i<n;i++)
         for(int j=i+1;j<n;j++)
           if( arr[i]==arr[j]){
               cout<<arr[j]<<endl;
               return 0;
           } else
               cout<<"element not found"<<endl;
           
    return 0;
} output 5 
1 2 3 2 4
element not found
element not found
element not found
element not found
element not found
2
