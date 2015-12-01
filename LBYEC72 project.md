#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<float.h>
#include<math.h>

#define BUFFER_SIZE 128
#define MAX_ROWS 24

typedef struct{
  int profacct[MAX_ROWS];
  char profpass[BUFFER_SIZE][MAX_ROWS];
  int studentacct[MAX_ROWS];
  char studentpass[BUFFER_SIZE][MAX_ROWS];
  char name[BUFFER_SIZE][MAX_ROWS];
  char degree[BUFFER_SIZE][MAX_ROWS];
  char address[BUFFER_SIZE][MAX_ROWS];
  char guardian[BUFFER_SIZE][MAX_ROWS];
  char gender[BUFFER_SIZE][MAX_ROWS];
  char school[BUFFER_SIZE][MAX_ROWS];
  char subject[BUFFER_SIZE][MAX_ROWS];
  int contactG[MAX_ROWS];
  float tuition[MAX_ROWS];
  int grade[MAX_ROWS];

} MYLASALLE;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject1;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject2;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject3;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject4;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject5;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject6;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject7;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject8;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject9;

typedef struct{
  int id[MAX_ROWS];
  float grade[MAX_ROWS];

} subject10;

int main(){

  MYLASALLE dlsu;
  subject1 memb;
  subject2 memr;
  subject3 mema;
  subject4 memc;
  subject5 ec71;
  subject6 ec72;
  subject7 ec73;
  subject8 ec74;
  subject9 mren;
  subject10 pro1;
  int nump = 0, nums = 0;
  int choice1, choice2;
  int profacct, studentacct;
  char pass[BUFFER_SIZE];
  int a, b, c;
  int found, temp;
  int sogo[MAX_ROWS];
  int membenrolled[MAX_ROWS]={0}, memrenrolled[MAX_ROWS]={0}, memaenrolled[MAX_ROWS]={0}, memcenrolled[MAX_ROWS]={0}, ec71enrolled[MAX_ROWS]={0}, ec72enrolled[MAX_ROWS]={0}, ec73enrolled[MAX_ROWS]={0}, ec74enrolled[MAX_ROWS]={0}, mrenenrolled[MAX_ROWS]={0}, pro1enrolled[MAX_ROWS]={0};
  int membenrolled1[MAX_ROWS]={0}, memrenrolled1[MAX_ROWS]={0}, memaenrolled1[MAX_ROWS]={0}, memcenrolled1[MAX_ROWS]={0}, ec71enrolled1[MAX_ROWS]={0}, ec72enrolled1[MAX_ROWS]={0}, ec73enrolled1[MAX_ROWS]={0}, ec74enrolled1[MAX_ROWS]={0}, mrenenrolled1[MAX_ROWS]={0}, pro1enrolled1[MAX_ROWS]={0};
  int nmemb=0, nmemr=0, nmema=0, nmemc=0, nec71=0, nec72=0, nec73=0, nec74=0, nmren=0, npro1=0;
  float membt=8500, memrt=8200, memat=7500, memct=8550, ec71t=7950, ec72t=7800, ec73t=8100, ec74t=8450, mrent=9000, pro1t=7200;
  int course, enrolled;

  printf("\n**Welcome to DLSU database**");
  do{
    temp = -24;
    printf("\n*****************************************");
    printf("\n1. Create Account ");
    printf("\n2. Sign In ");
    printf("\n3. Exit ");
    scanf("%d", &choice1);
    printf("\n*****************************************");

    switch(choice1)
      {

      case 1:



	printf("\n\n****************************");
	printf("\n1. Professor ");
	printf("\n2. Student ");
	scanf("%d", &choice2);
	printf("\n****************************");

	if(choice2==1)
	  {
	    nump++;
	    printf("\nEnter id number: ");
	    scanf("%d", &dlsu.profacct[nump-1]);
	    printf("\nEnter password: ");
	    scanf("%s", dlsu.profpass[nump-1]);
	  }

	else if(choice2==2)
	  {
	    nums++;
	    printf("\nEnter name: ");
	    fflush(stdin);
	    fgets(dlsu.name[nums-1], 128, stdin);
	    printf("\nEnter Degree Program: ");
	    scanf("%s", dlsu.degree[nums-1]);
	    printf("\nEnter your Secondary level school: ");
	    scanf("%s", &dlsu.school[nums-1]);
	    printf("\nEnter your present address: ");
	    fflush(stdin);
	    fgets(dlsu.address[nums-1], 128, stdin);
	    printf("\nGender: ");
	    scanf("%s", dlsu.gender[nums-1]);
	    printf("\nEnter Name of Guardian: ");
	    fflush(stdin);
	    fgets(dlsu.guardian[nums-1], 128, stdin);
	    printf("\nEnter contact number of Guardian: ");
	    scanf("%d", &dlsu.contactG[nums-1]);
	    printf("\nEnter id number: ");
	    scanf("%d", &dlsu.studentacct[nums-1]);
	    printf("\nEnter password: ");
	    scanf("%s", dlsu.studentpass[nums-1]);
	  }
	else
	  {
	    printf("INVALID SELECTION");
	  }break;

      case 2:
	printf("\n****************************");
	printf("\n1. Professor ");
	printf("\n2. Student ");
	scanf("%d", &choice2);
	printf("\n****************************");

	if(choice2==1)
	  {
	    printf("\nEnter your id number: ");
	    scanf("%d", &profacct);
	    for(a=0; a<nump; a++)
	      {
		if(dlsu.profacct[a]==profacct){
		  temp = a;
		}
	      }
	    printf("\nEnter Password: ");
	    scanf("%s", &pass);
	    if(strcmp(dlsu.profpass[temp], pass)==0)
	      {
		printf("\nYou are logged in");
		do{
		  printf("\n1. Add grade\n2. Edit Grade\n3. View Student Info\n4. Sign Out\n");
		  scanf("%d", &choice2);
		  switch(choice2)
		    {
		    case 1:
		      printf("\n1.Lbymemb \n2.Lbymemr \n3.Lbymema \n4.Lbymemc \n5.Lbyec71 \n6.Lbyec72 \n7.Lbyec73 \n8.Lbyec74 \n9.Lbymren \n10.Macpro1");
		      printf("Enter subject:");
		      scanf("%d", &choice1);
		      switch(choice1)
			{
			case 1:
			  {

			    printf("\nEnter grade for Lbymemb");
			    for(a=0; a<nmemb; a++)
			      {
				printf("\nID no. %d:", memb.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &memb.grade[a]);

			      }

			    for(a=0; a<nmemb; a++)
			      {
				printf("\n%d:\t%.1f", memb.id[a], memb.grade[a]);
			      }
			  }break;

			case 2:
			  {

			    printf("\nEnter grade for Lbymemr");
			    for(a=0; a<nmemr; a++)
			      {
				printf("\n%d:", memr.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &memr.grade[a]);

			      }
			    for(a=0; a<nmemr; a++)
			      {
				printf("\n%d:\t%.1f", memr.id[a], memr.grade[a]);
			      }
			  }break;


			case 3:
			  {

			    printf("\nEnter grade for Lbymema");
			    for(a=0; a<nmema; a++)
			      {
				printf("\n%d:", mema.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &mema.grade[a]);

			      }
			    for(a=0; a<nmema; a++)
			      {
				printf("\n%d:\t%.1f", mema.id[a], mema.grade[a]);
			      }
			  }break;

			case 4:
			  {

			    printf("\nEnter grade for Lbymemc");
			    for(a=0; a<nmemc; a++)
			      {
				printf("\n%d:", memc.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &memc.grade[a]);

			      }
			    for(a=0; a<nmemc; a++)
			      {
				printf("\n%d:\t%.1f", memc.id[a], memc.grade[a]);
			      }
			  }break;

			case 5:
			  {

			    printf("\nEnter grade for Lbyec71");
			    for(a=0; a<nec71; a++)
			      {
				printf("\n%d:", ec71.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &ec71.grade[a]);

			      }
			    for(a=0; a<nec71; a++)
			      {
				printf("\n%d:\t%.1f", ec71.id[a], ec71.grade[a]);
			      }
			  }break;

			case 6:
			  {

			    printf("\nEnter grade for Lbyec72");
			    for(a=0; a<nec72; a++)
			      {
				printf("\n%d:", ec72.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &ec72.grade[a]);

			      }
			    for(a=0; a<nec72; a++)
			      {
				printf("\n%d:\t%.1f", ec72.id[a], ec72.grade[a]);
			      }
			  }break;

			case 7:
			  {

			    printf("\nEnter grade for Lbyec73");
			    for(a=0; a<nec73; a++)
			      {
				printf("\n%d:", ec73.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &ec73.grade[a]);

			      }
			    for(a=0; a<nec73; a++)
			      {
				printf("\n%d:\t%.1f", ec73.id[a], ec73.grade[a]);
			      }
			  }break;

			case 8:
			  {

			    printf("\nEnter grade for Lbyec74");
			    for(a=0; a<nec74; a++)
			      {
				printf("\n%d:", ec74.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &ec74.grade[a]);

			      }
			    for(a=0; a<nec74; a++)
			      {
				printf("\n%d:\t%.1f", ec74.id[a], ec74.grade[a]);
			      }
			  }break;

			case 9:
			  {

			    printf("\nEnter grade for Lbymren");
			    for(a=0; a<nmren; a++)
			      {
				printf("\n%d:", mren.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &mren.grade[a]);

			      }
			    for(a=0; a<nmren; a++)
			      {
				printf("\n%d:\t%.1f", mren.id[a], mren.grade[a]);
			      }
			  }break;

			case 10:
			  {

			    printf("\nEnter grade for macpro1");
			    for(a=0; a<npro1; a++)
			      {
				printf("\n%d:", pro1.id[a]);
				printf("\nEnter Grade: ");
				scanf("%f", &pro1.grade[a]);

			      }
			    for(a=0; a<npro1; a++)
			      {
				printf("\n%d:\t%.1f", pro1.id[a], pro1.grade[a]);
			      }
			  }break;
			case 77:
			  break;
			default:
			  printf("invalid choice!");
			}break;
		    case 2:
		      printf("\n1.Lbymemb \n2.Lbymemr \n3.Lbymema \n4.Lbymemc \n5.Lbyec71 \n6.Lbyec72 \n7.Lbyec73 \n8.Lbyec74 \n9.Lbymren \n10.Macpro1");
		      printf("\n\nEnter subject:");
		      scanf("%d", &choice1);
		      switch(choice1)
			{
			case 1:
			  {
			    for(a=0; a<nmemb; a++)
			      {
				printf("\n%d. %d:", a+1, memb.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &memb.grade[found-1]);
			    for(a=0; a<nmemb; a++)
			      {
				printf("\n%d:\t%f", memb.id[a], memb.grade[a]);
			      }
			  }break;

			case 2:
			  {
			    for(a=0; a<nmemr; a++)
			      {
				printf("\n%d. %d:", a+1, memr.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &memr.grade[found-1]);
			    for(a=0; a<nmemr; a++)
			      {
				printf("\n%d:\t%.1f", memr.id[a], memr.grade[a]);
			      }
			  }break;

			case 3:
			  {
			    for(a=0; a<nmema; a++)
			      {
				printf("\n%d. %d:", a+1, mema.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &mema.grade[found-1]);
			    for(a=0; a<nmema; a++)
			      {
				printf("\n%d:\t%.1f", mema.id[a], mema.grade[a]);
			      }
			  }break;

			case 4:
			  {
			    for(a=0; a<nmemc; a++)
			      {
				printf("\n%d. %d:", a+1, memc.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &memc.grade[found-1]);
			    for(a=0; a<nmemc; a++)
			      {
				printf("\n%d:\t%.1f", memc.id[a], memc.grade[a]);
			      }
			  }break;

			case 5:
			  {
			    for(a=0; a<nec71; a++)
			      {
				printf("\n%d. %d:", a+1, ec71.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &ec71.grade[found-1]);
			    for(a=0; a<nec71; a++)
			      {
				printf("\n%d:\t%.1f", ec71.id[a], ec71.grade[a]);
			      }
			  }break;

			case 6:
			  {
			    for(a=0; a<nec72; a++)
			      {
				printf("\n%d. %d:", a+1, ec72.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &ec72.grade[found-1]);
			    for(a=0; a<nec72; a++)
			      {
				printf("\n%d:\t%.1f", ec72.id[a], ec72.grade[a]);
			      }
			  }break;

			case 7:
			  {
			    for(a=0; a<nec73; a++)
			      {
				printf("\n%d. %d:", a+1, ec73.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &ec73.grade[found-1]);
			    for(a=0; a<nec73; a++)
			      {
				printf("\n%d:\t%.1f", ec73.id[a], ec73.grade[a]);
			      }
			  }break;

			case 8:
			  {
			    for(a=0; a<nec74; a++)
			      {
				printf("\n%d. %d:", a+1, ec74.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &ec74.grade[found-1]);
			    for(a=0; a<nec74; a++)
			      {
				printf("\n%d:\t%.1f", ec74.id[a], ec74.grade[a]);
			      }
			  }break;

			case 9:
			  {
			    for(a=0; a<nmren; a++)
			      {
				printf("\n%d. %d:", a+1, mren.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &mren.grade[found-1]);
			    for(a=0; a<nmren; a++)
			      {
				printf("\n%d:\t%.1f", mren.id[a], mren.grade[a]);
			      }
			  }break;

			case 10:
			  {
			    for(a=0; a<npro1; a++)
			      {
				printf("\n%d. %d:", a+1, pro1.id[a]);
			      }
			    printf("\nNumber of ID number:");
			    scanf("%d", &found);
			    printf("\nNew Grade:");
			    scanf("%f", &pro1.grade[found-1]);
			    for(a=0; a<npro1; a++)
			      {
				printf("\n%d:\t%.1f", pro1.id[a], pro1.grade[a]);
			      }
			  }break;
			case 77:
			  break;
			default:
			  printf("invalid choice!");
			}break;

		    case 3:
		      printf("\n1.Lbymemb \n2.Lbymemr \n3.Lbymema \n4.Lbymemc \n5.Lbyec71 \n6.Lbyec72 \n7.Lbyec73 \n8.Lbyec74 \n9.Lbymren \n10.Macpro1");
		      printf("\nEnter subject:");
		      scanf("%d", &choice1);
		      switch(choice1){
		      case 1:
			for(a = 0; a<nmemb; a++){
			  printf("\n%d", memb.id[a]);
			  for(b = 0; b<nums; b++){
			    if(memb.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", memb.grade[a]);
			}
			break;
		      case 2:
			for(a = 0; a<nmemr; a++){
			  printf("\n%d", memr.id[a]);
			  for(b = 0; b<nums; b++){
			    if(memr.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", memr.grade[a]);
			}
			break;
		      case 3:
			for(a = 0; a<nmema; a++){
			  printf("\n%d", mema.id[a]);
			  for(b = 0; b<nums; b++){
			    if(mema.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", mema.grade[a]);
			}
			break;
		      case 4:
			for(a = 0; a<nmemc; a++){
			  printf("\n%d", memc.id[a]);
			  for(b = 0; b<nums; b++){
			    if(memc.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", memc.grade[a]);
			}
			break;
		      case 5:
			for(a = 0; a<nec71; a++){
			  printf("\n%d", ec71.id[a]);
			  for(b = 0; b<nums; b++){
			    if(ec71.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", ec71.grade[a]);
			}
			break;
		      case 6:
			for(a = 0; a<nec72; a++){
			  printf("\n%d", ec72.id[a]);
			  for(b = 0; b<nums; b++){
			    if(ec72.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", ec72.grade[a]);
			}
			break;
		      case 7:
			for(a = 0; a<nec73; a++){
			  printf("\n%d", ec73.id[a]);
			  for(b = 0; b<nums; b++){
			    if(ec73.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", ec73.grade[a]);
			}
			break;
		      case 8:
			for(a = 0; a<nec74; a++){
			  printf("\n%d", ec74.id[a]);
			  for(b = 0; b<nums; b++){
			    if(ec74.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", ec74.grade[a]);
			}
			break;
		      case 9:
			for(a = 0; a<nmren; a++){
			  printf("\n%d", mren.id[a]);
			  for(b = 0; b<nums; b++){
			    if(mren.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", mren.grade[a]);
			}
			break;
		      case 10:
			for(a = 0; a<npro1; a++){
			  printf("\n%d", pro1.id[a]);
			  for(b = 0; b<nums; b++){
			    if(pro1.id[a]==dlsu.studentacct[b] ){
			      printf("\n%s", dlsu.name[b]);
			    }

			  }
			  printf("\n%.1f", pro1.grade[a]);
			}
			break;
		      case 77:
			break;
		      default:
			printf("invalid choice!");
		      }
		    }


		}while(choice2!=4);

	      }

	    else
	      {
		printf("\nWrong password / Account name");
	      }break;
	  }

	else if(choice2==2)
	  {
	    printf("\nEnter your id number: ");
	    scanf("%d", &studentacct);
	    for(a=0; a<nums; a++)
	      {
		if(dlsu.studentacct[a]==studentacct){
		  temp = a;
		}
	      }
	    printf("\nEnter Password: ");
	    scanf("%s", &pass);
	    if(strcmp(dlsu.studentpass[temp], pass)==0)
	      {
		printf("\nYou are logged in");
		do{
		  printf("\n1. View Student Data\n2. View Grades\n3. Tuition Fee\n4. View Course Offering\n5. Enroll / Add Course\n6. Drop Course\n7. Sign Out");
		  printf("\n Note: To exit from Enroll, Add Course, Drop Course just enter 77");
		  printf("\nEnter Choice: ");
		  scanf("%d", &choice2);
		  switch(choice2){
		  case 1:
		    printf("\n Student Data");
		    printf("\nName: %s\nAddress: %s\nDegree: %s\nGender: %s\nSecondary Level: %s\nGuardian: %s\nContact Number: %d", dlsu.name[temp], dlsu.address[temp], dlsu.degree[temp], dlsu.gender[temp], dlsu.school[temp], dlsu.guardian[temp], dlsu.contactG[temp] );
		    break;
		  case 2:
		  	printf("\n If grade is 6.00; your prof has not yet entered a grade");
		    printf("\n Grades: ");

		    for(a = 0; a<nmemb; a++){
		      if(memb.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYMEMB\t%.1f", memb.grade[a]);
		      }
		    }

		    for(a = 0; a<nmemr;a++){
		      if(memr.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYMEMR\t%.1f", memr.grade[a]);
		      }
		    }

		    for(a = 0; a<nmema; a++){
		      if(mema.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYMEMA\t%.1f", mema.grade[a]);
		      }
		    }

		    for(a = 0; a<nmemc;a++){
		      if(memc.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYMEMC\t%.1f", memc.grade[a]);
		      }
		    }

		    for(a = 0; a<nec71; a++){
		      if(ec71.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYEC71\t%.1f", ec71.grade[a]);
		      }
		    }

		    for(a = 0; a<nec72;a++){
		      if(ec72.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYEC72\t%.1f", ec72.grade[a]);
		      }
		    }

		    for(a = 0; a<nec73; a++){
		      if(ec73.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYEC73\t%.1f", ec73.grade[a]);
		      }
		    }

		    for(a = 0; a<nec74;a++){
		      if(ec74.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYEC74\t%.1f", ec74.grade[a]);
		      }
		    }

		    for(a = 0; a<nmren; a++){
		      if(mren.id[a]==dlsu.studentacct[temp]){
			printf("\nLBYMREN\t%.1f", mren.grade[a]);
		      }
		    }

		    for(a = 0; a<npro1;a++){
		      if(pro1.id[a]==dlsu.studentacct[temp]){
			printf("\nMACPRO1\t%.1f", pro1.grade[a]);
		      }
		    }
		    break;
		  case 3:
		    printf("\nTuition Fee");
		    printf("\nYour tuition is %.2f", dlsu.tuition[temp]);
		    printf("\n\n");
		    break;
		  case 4:
		    printf("\nCourse Offering");
		    printf("\n3651\tLBYMEMB");
		    printf("\n3652\tLBYMEMR");
		    printf("\n3653\tLBYMEMA");
		    printf("\n3654\tLBYMEMC");
		    printf("\n3655\tLBYEC71");
		    printf("\n3656\tLBYEC72");
		    printf("\n3657\tLBYEC73");
		    printf("\n3658\tLBYEC74");
		    printf("\n3659\tLBYMREN");
		    printf("\n3660\tMACPRO1");
		    break;

		  case 5:

		    do{
		      printf("\nEnter course code:");
		      scanf("%d", &course);
		      switch(course)
			{
			case 3651:

			  for(a = 0, enrolled = 0; a<nmemb; a++){
			    if(memb.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYMEMB");

			  }
			  else{
			  nmemb++;
			  
			  printf("\nYou are now enrolled into LBYMEMB");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+membt;
			  memb.id[nmemb-1]=dlsu.studentacct[temp];
			  membenrolled[temp] = nmemb-1;
			  memb.grade[membenrolled[temp]]=6;
			  }
			  break;
			case 3652:
			  for(a = 0, enrolled = 0; a<nmemr; a++){
			    if(memr.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYMEMR");

			  }
			  else{
			  nmemr++;

			  printf("\nYou are now enrolled into LBYMEMR");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+memrt;
			  memr.id[nmemr-1]=dlsu.studentacct[temp];
			  memrenrolled[temp] = nmemr-1;
			  memr.grade[memrenrolled[temp]]=6;
			  }
			  break;
			  
			case 3653:
			  for(a = 0, enrolled = 0; a<nmema; a++){
			    if(mema.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYMEMR");

			  }
			  else{
			  nmema++;

			  printf("\nYou are now enrolled into LBYMEMA");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+memat;
			  mema.id[nmema-1]=dlsu.studentacct[temp];
			  memaenrolled[temp] = nmema-1;
			  mema.grade[memaenrolled[temp]]=6;
			  }
			  break;
			case 3654:
			  for(a = 0, enrolled = 0; a<nmemc; a++){
			    if(memc.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYMEMC");

			  }
			  else{
			  nmemc++;

			  printf("\nYou are now enrolled into LBYMEMC");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+memct;
			  memc.id[nmemc-1]=dlsu.studentacct[temp];
			  memcenrolled[temp] = nmemc-1;
			  memc.grade[memcenrolled[temp]]=6;
			  }
			  break;

			case 3655:
			  for(a = 0, enrolled = 0; a<nec71; a++){
			    if(ec71.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYEC71");

			  }
			  else{
			  nec71++;
			  
			  printf("\nYou are now enrolled into LBYEC71");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+ec71t;
			  ec71.id[nec71-1]=dlsu.studentacct[temp];
			  ec71enrolled[temp] = nec71-1;
			  ec71.grade[ec71enrolled[temp]]=6;
			  }
			  break;

			case 3656:
			  for(a = 0, enrolled = 0; a<nec72; a++){
			    if(ec72.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYEC72");

			  }
			  else{
			  nec72++;

			  printf("\nYou are now enrolled into LBYEC72");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+ec72t;
			  ec72.id[nec72-1]=dlsu.studentacct[temp];
			  ec72enrolled[temp] = nec72-1;
			  ec72.grade[ec72enrolled[temp]]=6;
			  }
			  break;

			case 3657:
			  for(a = 0, enrolled = 0; a<nec73; a++){
			    if(ec73.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYEC73");

			  }
			  else{
			  nec73++;

			  printf("\nYou are now enrolled into LBYEC73");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+ec73t;
			  ec73.id[nec73-1]=dlsu.studentacct[temp];
			  ec73enrolled[temp] = nec73-1;
			  ec73.grade[ec73enrolled[temp]]=6;
			  }
			  break;

			case 3658:
			  for(a = 0, enrolled = 0; a<nec74; a++){
			    if(ec74.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYEC74");

			  }
			  else{
			  nec74++;

			  printf("\nYou are now enrolled into LBYEC74");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+ec74t;
			  ec74.id[nec74-1]=dlsu.studentacct[temp];
			  ec74enrolled[temp] = nec74-1;
			  ec74.grade[ec74enrolled[temp]]=6;
			  }
			  break;

			case 3659:
			  for(a = 0, enrolled = 0; a<nmren; a++){
			    if(mren.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN LBYMREN");

			  }
			  else{
			  nmren++;

			  printf("\nYou are now enrolled into LBYMREN");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+mrent;
			  mren.id[nmren-1]=dlsu.studentacct[temp];
			  mrenenrolled[temp] = nmren-1;
			  mren.grade[mrenenrolled[temp]]=6;
			  }
			  break;

			case 3660:
			  for(a = 0, enrolled = 0; a<npro1; a++){
			    if(pro1.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			    printf("\nYOU ARE CURRENTLY ENROLLED IN MACPRO1");

			  }
			  else{
			  npro1++;

			  printf("\nYou are now enrolled into MACPRO1");
			  dlsu.tuition[temp]=dlsu.tuition[temp]+pro1t;
			  pro1.id[npro1-1]=dlsu.studentacct[temp];
			  pro1enrolled[temp] = npro1-1;
			  pro1.grade[pro1enrolled[temp]]=6;
			  }
			  break;

			case 77:
			  break;

			default:
			  printf("invalid choice!");

			}

		    }while(course!=77);
		    break;

		  case 6:
		    printf("remove class\n");
		    do{
		      printf("\nEnter course code:");
		      scanf("%d", &course);
		      switch(course)
			{
			case 3651:
				 for(a = 0, enrolled = 0; a<nmemb; a++){
			    if(memb.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  
			  printf("\nYou now dropped LBYMEMB");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-membt;
			  for(a=membenrolled[temp]; a<nmemb; a++)
			    {
			      memb.id[a]=memb.id[a+1];
			    }
			  nmemb--;
		}
		else{
			puts("\n You are not Enrolled to MEMB");
		}
			  break;

			case 3652:
				 for(a = 0, enrolled = 0; a<nmemr; a++){
			    if(memr.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){

			  printf("\nYou now dropped LBYMEMR");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-memrt;
			  for(a=memrenrolled[temp]; a<nmemr; a++)
			    {
			      memr.id[a]=memr.id[a+1];
			    }
			  nmemr--;
		}
		else{
			puts("\n You are not Enrolled to MEMR");
		}	  
			  break;

			case 3653:
				 for(a = 0, enrolled = 0; a<nmema; a++){
			    if(mema.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  printf("\nYou now dropped LBYMEMA");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-memat;
			  for(a=memaenrolled[temp]; a<nmema; a++)
			    {
			      mema.id[a]=mema.id[a+1];
			    }
			  nmema--;
			  }
		else{
			puts("\n You are not Enrolled to MEMA");
		}
			  break;

			case 3654:
				 for(a = 0, enrolled = 0; a<nmemc; a++){
			    if(memc.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  printf("\nYou now dropped LBYMEMC");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-memct;
			  for(a=memcenrolled[temp]; a<nmemc; a++)
			    {
			      memc.id[a]=memc.id[a+1];
			    }
			  nmemc--;
			  }
		else{
			puts("\n You are not Enrolled to MEMC");
		}
			  break;

			case 3655:
				 for(a = 0, enrolled = 0; a<nec71; a++){
			    if(ec71.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  printf("\nYou now dropped LBYEC71");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-ec71t;
			  for(a=ec71enrolled[temp]; a<nec71; a++)
			    {
			      ec71.id[a]=ec71.id[a+1];
			    }
			  nec71--;
			  }
		else{
			puts("\n You are not Enrolled to EC71");
		}
			  break;

			case 3656:
				 for(a = 0, enrolled = 0; a<nec72; a++){
			    if(ec72.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  printf("\nYou now dropped LBYEC72");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-ec72t;
			  for(a=ec72enrolled[temp]; a<nec72; a++)
			    {
			      ec72.id[a]=ec72.id[a+1];
			    }
			  nec72--;
			  }
		else{
			puts("\n You are not Enrolled to EC72");
		}
			  break;

			case 3657:
				 for(a = 0, enrolled = 0; a<nec73; a++){
			    if(ec73.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  printf("\nYou now dropped LBYEC73");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-ec73t;
			  for(a=ec73enrolled[temp]; a<nec73; a++)
			    {
			      ec73.id[a]=ec73.id[a+1];
			    }
			  nec73--;
			  }
		else{
			puts("\n You are not Enrolled to EC73");
		}
			  break;

			case 3658:
				 for(a = 0, enrolled = 0; a<nec74; a++){
			    if(ec74.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  printf("\nYou now dropped LBYEC74");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-ec74t;
			  for(a=ec74enrolled[temp]; a<nec74; a++)
			    {
			      ec74.id[a]=ec74.id[a+1];
			    }
			  nec74--;
			  }
		else{
			puts("\n You are not Enrolled to EC74");
		}
			  break;

			case 3659:
				 for(a = 0, enrolled = 0; a<nmren; a++){
			    if(mren.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  printf("\nYou now dropped LBYMREN");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-mrent;
			  for(a=mrenenrolled[temp]; a<nmren; a++)
			    {
			      mren.id[a]=mren.id[a+1];
			    }
			  nmren--;
			  }
		else{
			puts("\n You are not Enrolled to MREN");
		}
			  break;

			case 3660:
				 for(a = 0, enrolled = 0; a<npro1; a++){
			    if(pro1.id[a]==dlsu.studentacct[temp]){
			      enrolled = 1;
			    }
			  }
			  if(enrolled==1){
			  printf("\nYou now dropped MACPRO1");
			  dlsu.tuition[temp]=dlsu.tuition[temp]-pro1t;
			  for(a=pro1enrolled[temp]; a<npro1; a++)
			    {
			      pro1.id[a]=pro1.id[a+1];
			    }
			  npro1--;
			  }
		else{
			puts("\n You are not Enrolled to MACPRO1");
		}
			  break;

			case 77:
			  break;

			default:
			  printf("\ninvalid choice!");

			}

		    }while(course!=77);
		    break;

		  }

		}while(choice2!=7);

	      }

	    else
	      {
		printf("\nWrong password / Account name");
	      }break;

	  }



      }
  }while(choice1!=3);
}


