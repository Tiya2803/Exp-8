# Experiment 8
# Aim:
To study and implement C++ 2D Array - Matrices

# Theory:
A 2D array in C++ can be defined as a data structure that deals with two-dimensional grid formats such as matrices wherein every single element is well identified by two indices: one for rows and another one for columns. It is similar to an array composed of other arrays.
A two-dimensional array could be declared using the syntax type arrayName[rows][columns]; For instance, int matrix[3][4]; indicates three rows by four columns. All its members occupy successive positions in memory meaning they are laid out linearly following row-major order scheme hence it makes it different from accessing them through single index only but rather via two indexes.They may be initialized while being declared. For static arrays they require listing down values enclosed in nested braces whereas dynamic arrays size calculation occurs at run-time stage hence this involves dynamic allocation using new’s keyword and deallocation using delete’s keyword in C++.Elements can be accessed using their respective row and column indexes. The iteration uses mostly a two-fold loop: the outer one is run for rows while the inner one does columns. It enables you to treat or manipulate one element of an entire array.

# Code:

a.
```
#include<iostream>
using namespace std;
int main()
{
    //matrix input and display
    int a[2][2];
    int i,j;
    for (i=0 ;i<2; i++)
    {
        for (j=0 ;j<2; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }

    for (i=0 ;i<2; i++)
    {
        for (j=0 ;j<2; j++)
        {
            cout<<a[i][j]<<" ";
        }
        cout<<endl;
    }

}
```
b.
```
#include<iostream>
using namespace std;
int main()
{

    int a[2][2];
    int b[2][2];
    int s[2][2];
    int i,j,r = 0,c=0;
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;

    cout<<"Matrix 2: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>b[i][j];
        }
    }
    cout<<endl;

    
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            s[i][j] = a[i][j] + b[i][j];
        }
    }

    cout<<"Sum: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<s[i][j]<<" ";
        }
        cout<<endl;
    }
        cout<<endl;
}
```
c.
```
#include<iostream>
using namespace std;
int main()
{
    int i,j,k,r = 0,c=0,s = 0;
    int a[r][c];
    int b[r][c];
    int p[r][c];
    
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;

    cout<<"Matrix 2: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>b[i][j];
        }
    }
    cout<<endl;

    
for (int i = 0; i < r; ++i) 
{
        for (int j = 0; j < r; ++j) 
        {
            p[i][j] = 0;
            for (int k = 0; k <c; ++k) 
            {
                p[i][j] += a[i][k] * b[k][j];
            }
        }
}

    cout<<"Product: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<p[i][j]<<" ";
        }
        cout<<endl;
    }
        cout<<endl;
}
```
d.
```
#include<iostream>
using namespace std;
int main()
{
    int i,j,k,r = 0,c=0;
    int a[r][c];
    int da = 0;
    
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;


    for (int i = 0; i < r; i++) 
    {
        da = da + a[i][i];
    }

cout<<"Diagonal Sum: "<<da<<endl;


}
```
e.
```
#include<iostream>
using namespace std;
int main()
{

    int a[2][2];
    int i,j,r = 0,c=0;
    bool eqr = true;
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;


    for (int j = 0; j < c; j++) 
    {
        if (a[0][j] != a[1][j]) 
        {
            eqr = false;
            break;
        }
    }
    cout<<"Row equality: "<<eqr;
}
```

# Output:

a.<br>![image](https://github.com/user-attachments/assets/d8bbaba5-1dd6-4882-8bdd-7ec223c37739)<br>
b.<br>![image](https://github.com/user-attachments/assets/ea824748-678f-4288-a1b7-88c6b4ba4986)<br>
c.<br>![image](https://github.com/user-attachments/assets/91441923-68d3-46a9-b440-0011fb05ac1f)<br>
d.<br>![image](https://github.com/user-attachments/assets/71361983-c8f4-4306-b2f3-ca591f200da0)<br>
e.<br>![image](https://github.com/user-attachments/assets/ac0a1c76-2239-4ea3-9057-6614841e01be)<br>



# Conclusion:

→ We learnt the use case of 2D arrays in C++.

→ We learnt how to perform basic operations on a 2-D array in C++.


