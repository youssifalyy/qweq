Doctor class
#include "doctor.h"
#include <sstream>
#include <string>
#include <iostream>
#include <fstream>
#include <cstdlib>
using namespace std;
Doctor :: Doctor(){};
Doctor ::Doctor(string x,int y,string z,int g){
	name=x;
	age=y;
	department=z;
	number_of_patients=g;
};
void Doctor :: setname(string x){
	name=x;
}
void Doctor :: setage(int x){
	age=x;
}void Doctor :: setdepart(string x){
	department=x;
}
void Doctor :: setnumber_of_patient(int x){
	number_of_patients=x;
}
string Doctor :: getname(){
	return name;
}
int Doctor :: getage(){
	return age;
}
string Doctor :: getdepart(){
	return department;
}
int Doctor :: getnumber_of_patient(){
	return number_of_patients;
}
void Doctor :: editpatienthistory(string x){
	patient_history=x;
}
string Doctor :: geteditpatienthistory(){
	return patient_history;
}
void Doctor ::roomsvalidator (){
string x;
string y;
   ofstream myfile3("rooms.txt",ios::app);
	ifstream myfile;
	myfile.open("count.txt");
if (myfile.is_open()){
while(getline (myfile,x)) 
{
 y=x;
}
myfile.close();
}
else
{
cout << "Unable to open file"; 
}
stringstream geek(y);
int count;
geek>>count;
	int z=count+1;
	ofstream myfile2;
	myfile2.open("count.txt");
	myfile2<<z<<endl;
	myfile2.close();
if(z<=10){
	cout<<"you can reserve the room ";
	cout<<z<<endl;
	myfile3<<"you can reserve the room"<<" "<<z<<endl;
}	
	else {
		cout<<"all rooms are busy"<<endl;
	}
}
                                     #include <iostream>
using namespace std;
class Doctor{
	private :
		string name;
		int age;
		string department;
		int number_of_patients;
		string patient_history;
		public :
			Doctor();
			Doctor(string x,int y,string z,int g);
			void setname(string x);
			string getname();
			void setage(int x);
			int getage();         
			void setdepart(string x);
			string getdepart();
         void setnumber_of_patient(int x); 
         int getnumber_of_patient();
         void editpatienthistory(string x);
         string geteditpatienthistory();
         void roomsvalidator ();
         
         Doctor d1;
cout<<"enter the age of doctor"<<endl;
int u;
cin>>u;
d1.setage(u);
cout<<"choose one department of the doc you want (Neurology-Oncology-Emergency-Obstetrics)"<<endl;
string f;
cin>>f;
d1.setdepart(f);
cout<<"enter the name of doc"<<endl;
string a;
cin>>a;
d1.setname(a);
cout<<"enter the number of patients with the doc"<<endl;
int b;
cin>>b;
d1.setnumber_of_patient(b);
cout<<"edit of patient history"<<endl;
string c;
cin>>c;
d1.editpatienthistory(c);
cout<<"name of doc"<<endl;
cout<<d1.getname()<<endl;
cout<<"age of doc"<<endl;
cout<<d1.getage()<<endl;
cout<<"patient's number"<<endl;
cout<<d1.getnumber_of_patient()<<endl;
cout<<"edit patient history"<<endl;
myfile<<"the update of doctor for the patient disease :"<<endl;
myfile<<d1.geteditpatienthistory()<<endl;
cout<<d1.geteditpatienthistory()<<endl;
cout<<"doctor reserve a room for patient who need extra care "<<endl;
d1.roomsvalidator ();
cout<< "     End of the doctor information     "<<endl;
