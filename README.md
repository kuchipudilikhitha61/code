import java.util.*;
public class Main
{
    
    class Node{
        int data;
        Node next;
        Node(int data){
            this.data=data;
            this.next=null;
        }
    }
    Node head=null;
    public void insert(int d){
        Node newnode=new Node(d);
        if(head==null){
            head=newnode;
        }
        else{
            Node temp=head;
            while(temp.next!=null){
                temp=temp.next;
            }
            temp.next=newnode;
        }
    }
    public void display(){
        Node temp=head;
        System.out.println();
        while(temp!=null){
            System.out.print(temp.data+" ");
            temp=temp.next;
        }
    }
    public void insertb(int d){
        Node temp=head;
        Node newnode=new Node(d);
        head=newnode;
        newnode.next=temp;
    }
    public void deletef(){
        Node temp=head;
        head=temp.next;
    } 
	public static void main(String[] args) {
	Main ob=new Main();
	Scanner sc=new Scanner(System.in);
	int a;
	while(true){
	    System.out.println("press 1 to insert at end");
	    System.out.println("press 2 to insert at begining");
	    System.out.println("press 3 to insert at display");
	    System.out.println("press 4 to insert at exit");
	    System.out.println("press 5 to delete the first value");
	    a=sc.nextInt();
	    switch(a){
	        case 1: System.out.println("enter the value to be inserted");
	        a=sc.nextInt();
	        ob.insert(a);
	        break;
	        case 2:
	        System.out.println("enter the value to be inserted");
	        a=sc.nextInt();
	        ob.insertb(a);
	        break;
	        case 3:
	        System.out.println("elements in linked list are:-");
	        ob.display();
	        System.out.println();
	        break;
	        case 4:
	        return;
	        case 5:
	            ob.deletef();
	    }
	}    
	}
}
