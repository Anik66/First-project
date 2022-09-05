# First-project
C++ (project)
#include<iostream>
#include<string>
using namespace std;

class Person{
public:
    string name;
    int age;
    Person(){

    }








};

class StudentInfo:public Person{
protected:
    int studentID;
    int studentSemester;

public:
    void getstdentData(){
    cout<<"---------STUDENT-INFORMATION-----------"<<endl;
    cout<<"Enter the student Name:";
    cin>>name;
    cout<<"Enter your age:";
    cin>>age;
    cout<<"Enter your Student ID:";
    cin>>studentID;
    cout<<"Enter your studentSemester:";
    cin>>studentSemester;



    }

    void student_check(){

   if(studentID > 120 || studentSemester > 12){

     cout<<"Sorry,you are not our institute student"<<endl;
   exit(0);

   }
   else{

    cout<<"Wellcome,to your our hostel"<<endl;
   }







    }

};















class RoomDetail{
    protected:

    int roomnum[10]={11,12,13,14,15,16,17,18,19,20};
   int roomrent[3]={7000,4000,3000};

  public:
 void GetroomData(){
        cout<<"Show the room number list:";
         for(int i=0;i<10;i++){
            cout<<roomnum[i]<<" ";


         }
         cout<<endl;
        cout<<"Show the roomrent list :"<<endl;
        for(int i=0;i<3;i++){
            cout<<"The Room Rent List:"<<roomrent[i]<<endl;
        }



        }


void Allotment(){
    cout<<"Enter your Roomnum:";
    cin>>roomnum[0];
    cout<<endl;
    cout<<"Enter your Roomrent";
    cin>>roomrent[0];


    if(roomnum[0] >20 || 3000>=roomrent[0]>=7000 )
        {
        cout<<"Sorry,we dont have the room"<<endl;
        exit(0);
    }
     else if(roomrent[0]==7000){

        cout<<"1 bedroom with attached bathroom and belcony"<<endl;

    }
    else if(roomrent[0]==4000){
        cout<<"1 bad room "<<endl;
    }
    else if(roomrent[0]==3000){
        cout<<"hallroom"<<endl;
    }
    else{
      cout<<"sorry,we dont have the room"<<endl  ;
    }



cout<<endl<<endl;




}









};

 class Mealdetail{

   private:
    int amount[3]={180,220,250};
    public:
    void Set_mealbill(){
    cout<<"Enter the amount list:"<<endl;
    for(int i=0;i<3;i++){
        cout<<amount[i]<<endl;
    }
    }

    void amount_pay(){
        cout<<"Show the amount list:";
        cin>>amount[3];
        cout<<endl;

    if(amount[0]==180){

        cout<<"breakfast:"<<"2 roti and 1 eggg"<<endl;
        cout<<"Lunch:"<<"2 plate rice and 1 fish curry"<<endl;
        cout<<"Dinner:"<<"2 plate rice and 1 chiken meat and 1 plate daal "<<endl;
    }
    else if(amount[0]==220){
        cout<<"breakfast:"<<"3 parata and 1 eggg and 1 plate vegetables" <<endl;
        cout<<"Lunch:"<<"2 plate rice and 1 fish curry and 1 chiken meat  "<<endl;
        cout<<"Dinner:"<<"morog polao "<<endl;

    }

    else if(amount[0]==250){
        cout<<"breakfast:"<<"vuna khicuri" <<endl;
        cout<<"Lunch:"<<"Thaeri "<<endl;
        cout<<"Dinner:"<<"khacci  "<<endl;

    }
    else{

        cout<<"Sorry,we can not provide food with this amount"<<endl;
    }

cout<<endl<<endl;
    }


 };

class  HostelName:public RoomDetail,public Mealdetail
 {
private:
    string name;

    public:
    void setHData(string Fname){
       name=Fname;



    }
    string getHData(){
        cout<<"Hostel name:";
    return name;

    }

};




int main(){


 cout<<"----------WeLLCOME TO OUR HOSTEL--------"<<endl;
  HostelName obj2;
  obj2.setHData("freiends Hostel");
  cout<<obj2.getHData();
  cout<<endl;
  StudentInfo obj1;
 obj1. getstdentData();
 obj1.student_check();


 obj2.GetroomData();
 obj2.Allotment();
 obj2.Set_mealbill();
 obj2.amount_pay();

cout<<"----------THANK YOU--------"<<endl;









return 0;
}

