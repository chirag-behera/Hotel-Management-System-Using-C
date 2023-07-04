# Hotel-Management-System-Using-C
#include <stdio.h> 
#include <string.h>
#include <stdlib.h>
void begin(); 
void show_details();
void complaints_suggestions();
void book_room();
struct
{ 
   char name[20];
   char address[50];
   char email_id[30];
   char nationality[25];
   int roomno;
   char *roomtype;
   int billprice;
   char *program;
} person;
int main()
{
 person.roomno = 0;
   person.billprice = 0;
   person.program = "notchosen";
   printf("WELCOME TO PARADISE HOTEL\n");
   printf("Please enter your details before moving to the mainpage!\n");
   printf("please enter your name:");
   gets(person.name);
   printf("enter your address:");
   gets(person.address);
   printf("enter your nationality:");
   gets(person.nationality);
   printf("enter your email_id:");
   gets(person.email_id);
   system("cls");
   begin();
   return 0;
}
void begin(void)
{
   int decide;
   printf("\n HOW CAN WE HELP YOU?\n\n");
   printf("\n1.Book a room\n2.complaints or suggestions\n3.check out\n4.about us\n");
   scanf("%d", &decide);
   switch (decide)
   {
     case 1:
     book_room();
     break;
     case 2:
     complaints_suggestions();
     printf("Thank you for your valuable suggestions!\n");
     begin();
     break;
     case 3:
     printf("Visit again!");
     printf("Thank you for trusting our service.\n");
     break;
     case 4:
     printf("THE PARADISE:\n");
     printf("A beautiful cosmopolitan destination for a picturesque natural scenario and a blend of Nature");
     printf(" is the memorable experience you could enjoy only at THE PARADISE.");
     printf("Clean and Comfortable room, Hot and Cold Water facilities, beautiful garden, family environment, local food are our salient 
     features to give you taste of our Culture.");
     printf("Satisfying you totally with our unique culture is our primary motto.\n");
     begin();
     break;
   }
}
void book_room(void)
{
   system("cls");
   if (person.roomno == 0)
   {
     int type_of_rooms;
     char ch, c;
     printf("\nWhat type of room do u want to book?\n");
     printf("\n1.Basic Room Rs 1000\n2.Medium room Rs 2000\n3.DELUXE ROOM Rs 3000\n4.I don't want to choose anything\n");
     scanf("%d", &type_of_rooms);
     fflush(stdin);
     if (type_of_rooms == 1)
     {
       printf("\nDo you accept this room?(y/n)\n");
       scanf("%c", &c);
       if (c == 'y')
     {
       system("cls");
       printf("\nYou choose basic room. Enjoy your stay\n");
       printf("your room no is 121");
       person.roomno = 121;
       person.roomtype = "basic";
       person.billprice += 1000;
       begin();
   }
   else
   begin();
 }
 if (type_of_rooms == 2)
 {
   printf("\nDo you accept this room?(y/n)\n");
   scanf("%c", &c);
   if (c == 'y')
   {
     system("cls");
     printf("\nYou choose medium room. Enjoy your stay\n");
     printf("your room no is 212");
     person.billprice += 2000;
     person.roomno = 212;
     person.roomtype = "medium";
     begin();
   }
   else
   begin();
 }
 if (type_of_rooms == 3)
 {
   printf("\nDo u accept this room?(y/n)\n");
   scanf("%c", &c);
   if (c == 'y')
   {
     system("cls");
     printf("\nYou choose deluxe room. Enjoy your stay\n");
     printf("your room no is 312");
     person.billprice += 3000;
     person.roomtype = "deluxe";
     person.roomno = 312;
     begin();
   }
   else
   begin();
 }
 if (type_of_rooms == 4)
 begin();
 }
 else
 printf("you have already booked a room");
}
void complaints_suggestions(void)
{
 system("cls");
 char complain[500];
 printf("please enter your complaints or suggestions\n");
 gets(complain);
 scanf("%c",&complain);
}
