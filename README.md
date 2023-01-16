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
	largest and minimum or second lagest element in array
	#include <iostream>
#include <climits>
using namespace std;
  */int secondlargest(int n,int arr[]){
      int largest=0;
      int secondlargest=-1;
      for(int i=0;i<n;i++){
          if(arr[i]>arr[largest]){
              largest=i;
          }
      }
      for(int i=0;i<n;i++){
          if(arr[i]!==arr[largest]){
              if(secondlargest==-1)
               secondlargest==i;
               else(arr[i]>arr[secondlargest]){
                   secondlargest=i;
               }
          }
      }
      return secondlargest;
  }*/
  
   int getmin(int arr[],int n){
    int min= INT_MAX;
    for(int i=0;i<n;i++){
        if(arr[i]<min){
            min=arr[i];
            
        }
    }
    return min;
}

int getmax(int arr[],int n){
    int max= INT_MIN;
    for(int i=0;i<n;i++){
        if(arr[i]>max){
            max=arr[i];
            
        }
    }
    return max;
}

int main() {
    int n;
    cin>>n;
    int arr[100];
    for(int i=0;i<n;i++){
        cin>>arr[i];
    } 
    cout<< "maximum value is"<< getmax(arr,n)<<endl;
    cout<<"minimum value is "<< getmin(arr,n)<<endl;
    cout <<"second largest value"<< secondlargest(arr,n)<<endl;(wrong)        

    return 0;
}
	//vector sort
	# include <bits/stdc++.h>
# include <vector>
using namespace std;
int main(){
    vector<pair<int,int>> v;
    int arr[]={1 ,9,6,3,5};
    int arr1[]={7,4,9,5,7};
    
    int n= sizeof(arr) /sizeof (arr[0]);
    for(int i=0;i<n;i++)
        v.push_back(make_pair(arr[i],arr1[i]));
        cout<<"before short"<<endl;
    
    for(int i=0;i<n;i++){
        cout<<v[i].first<<" "<<v[i].second<<endl;
    }
    sort(v.begin(),v.end());
    cout <<"after short"<<endl;
    for(int i=0;i<n;i++){
                cout<<v[i].first<<" "<<v[i].second<<endl;
    }
    
    return 0;
}
erase vector
#include <iostream>
# include <vector>
using namespace std;
int main() {
      vector<int>myvector{1,3,5,7,8};
      vector<int>::iterator it;
      it =myvector.begin();
      myvector.erase(it);
      for(auto it=myvector.begin();it!=myvector.end();++it)
          cout<<*it<<endl;
      

    return 0;
}output  3456
	LINKED LIST INSERT
	#include <iostream>
using namespace std;
class Node{
	public:
	int data;
	Node* next;
	Node(int data){
		this-> data=data;
		this-> next=NULL;
	}
};insert at head////
 void InsertAtHead(Node* &head,int d){
 	Node* temp=new Node(d);
 	temp->next=head;
 	head=temp;
 	
 }insert at tail///
	void InsertAtTail(Node* &tail,int d){
     Node* temp=new Node(d);
     tail->next=temp;
     tail=temp;
 }
 trivers///
 void print(Node* &head){   
     Node* temp=head;
     while(temp!=NULL){
     cout<<temp->data<<" ";
     temp=temp->next;
   }
   cout<<endl;
 }
int main() {
	Node* node1=new Node(10);
	Node* head=node1;
	print(head);
	 InsertAtHead(head,12);
	 print(head);
	 InsertAtHead(head,15);
	 print(head);
	 
	return 0;
}#include <iostream>
using namespace std;
class Node{
	public:
	int data;
	Node* next;
	Node(int data){
		this-> data=data;
		this-> next=NULL;
	}
}; insertat mid first and last;
 void InsertAtHead(Node* &head,int d){
 	Node* temp=new Node(d);
 	temp->next=head;
 	head=temp;
 	
 }
 void InsertAtTail(Node* &tail,int d){
     Node* temp=new Node(d);
     tail->next=temp;
     tail=temp;
 }
 void InsertAtPosition(Node* &tail,Node* &head,int Position,int d){
	///insert at first position//
	if(Position==1){
         InsertAtHead(head,d);
         return;
	}
     Node* temp=head;
    int cnt=1;
     while(cnt<Position-1){
         temp=temp->next;
         cnt++;
     }
	insertat last position//
	if(temp->next==NULL){
         InsertAtTail( tail,d);
         return;
     }
     Node* nodeToInsert=new Node(d);
     nodeToInsert->next=temp->next;
     temp->next=nodeToInsert;
     
 }
 
 void print(Node* &head){
     Node* temp=head;
     while(temp!=NULL){
     cout<<temp->data<<" ";
     temp=temp->next;
   }
   cout<<endl;
 }
int main() {
	Node* node1=new Node(10);
	Node* head=node1;
	Node* tail=node1;
	print(head);
	 InsertAtTail(tail,12);
	 print(head);
	 InsertAtTail(tail,15);
	 print(head);
	 
	 InsertAtPosition(head,3,22);
	 print(head);
	 //inser at tail..
	 InsertAtPosition(tail,head,4,22);
	 print(head);
	 cout<<"head"<<head->data<<endl;
	 cout<<"tail"<<tail->data<<endl;
	return 0;output==
	10 
10 12 
10 12 15 
10 12 15 22 
head10
tail22

} deliction start////
	
