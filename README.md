# matrix
#include<iostream.h>
#include<conio.h>
class matrix
{
  int r,c,a[10][10],b[10][10],n[10][10],sum[10][10],i,j;
  public :
   void get();
   void add();
   void display();
   void mul();
   void sub();
   void div();
   void tpos();
   };
 void matrix::get()
 {
    cout<<"Enter number of rows (between 1 to 10) : "<<endl;
    cin>>r;
    cout<<"Enter number of columns (between 1 to 10) : "<<endl;
    cin>>c;
}
void matrix:: display()
{
  cout<<endl<<"Enter Element Of 1st Matrix :"<<endl;
  for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	cout<<"Enter Element A "<<i+1<<j+1<<":";
	cin>>a[i][j];
	}
	}
	cout<<endl<<"Enter Element Of 2nd Matrix :"<<endl;
	 for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	cout<<"Enter Element B "<<i+1<<j+1<<":";
	cin>>b[i][j];
	}
	}
	cout<<"Element Of 1st Matrix :"<<endl;
		 for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	cout<<a[i][j]<<" ";
	}
	cout<<endl;
	}
	cout<<"Element Of 2nd Matrix :"<<endl;
		 for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	cout<<b[i][j]<<" ";
	}
	cout<<endl;
	}

	}
void matrix::add()
{
    for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	sum[i][j]=a[i][j]+b[i][j];
	}
	}
	cout<<endl<<"Sum of Two Matrix is :"<<endl;
	for(i=0;i<r;i++)
	{
	  for(j=0;j<c;j++)
	  {
	     cout<<sum[i][j]<<" ";

	     }
	      cout<<endl;
	     }
	     }
	     void matrix::sub()
	     {
	      for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	sum[i][j]=a[i][j]-b[i][j];
	}
	}
	cout<<endl<<"Substraction of Two Matrix is :"<<endl;
	for(i=0;i<r;i++)
	{
	  for(j=0;j<c;j++)
	  {
	     cout<<sum[i][j]<<" ";

	     }
	      cout<<endl;
	     }
	     }
  void matrix::mul()
  {
   for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	sum[i][j]=a[i][j]*b[i][j];
	}
	}
	cout<<endl<<"Multiplication of Two Matrix is :"<<endl;
	for(i=0;i<r;i++)
	{
	  for(j=0;j<c;j++)
	  {
	     cout<<sum[i][j]<<" ";

	     }
	      cout<<endl;
	     }


  }
  void matrix::div()
  {
   for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	sum[i][j]=a[i][j]/b[i][j];
	}
	}
	cout<<endl<<"Division of Two Matrix is :"<<endl;
	for(i=0;i<r;i++)
	{
	  for(j=0;j<c;j++)
	  {
	     cout<<sum[i][j]<<" ";

	     }
	      cout<<endl;
	     }



  }
  void matrix::tpos()
  {
   for(i=0;i<r;i++)
  {
     for(j=0;j<c;j++)
     {
	n[j][i]=a[i][j];
	}
	}
	cout<<endl<<"Transpose of Matrix is :"<<endl;
	for(i=0;i<r;i++)
	{
	  for(j=0;j<c;j++)
	  {
	     cout<<n[i][j]<<" ";

	     }
	      cout<<endl;
	     }

  }
	     void main()
	     {   int ch;
		clrscr();
		matrix x;
		x.get();
		while(ch!=100)
		{
cout<<endl<<"Enter your choise 1.Display 2.Addition 3.Substraction 4.Multiplication 5.Division 6.Transpose "<<endl;
	  cin>>ch;
	  switch(ch)
	  {
	   case 1: x.display();break;
	   case 2: x.add(); break;
	   case 3: x.sub(); break;
	   case 4: x.mul(); break;
	   case 5: x.div(); break;
	   case 6: x.tpos(); break;
	   case 7: exit(0);
	   default:
	       cout<<"Your Choise Is Wrong";
	       }
	       }
		getch();
		}
