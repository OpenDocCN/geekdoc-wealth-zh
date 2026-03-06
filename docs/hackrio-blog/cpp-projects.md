# 2023 年 C++初学者十大 C++项目创意[更新]

> 原文：<https://hackr.io/blog/cpp-projects>

## 介绍

C++是作为 C 的扩展而构建的，它给予程序员对内存和系统资源的高度控制。如果你懂别的编程语言，C++就好学了。即使不然，C++也是一种友好的语言，你可以通过一些动手项目和实践来学习它。

本文列举了 10 个不同级别的 C++项目，有助于你更好地欣赏这门语言。也可以尝试很多其他类似的项目。例如，我们的一个项目是书店库存管理。你也可以试试图书馆管理系统。还是那句话，类似于铁路客票预订系统，可以试试汽车客票预订系统。

想在开始第一个 C++项目之前学习 C++？[从 udemy 开始 C++编程课程](https://click.linksynergy.com/deeplink?id=SeYHzlfZEmI&mid=39197&murl=https://www.udemy.com/course/beginning-c-plus-plus-programming/)强烈推荐开始你的 C++之旅。

## 什么是 C++？

C++是一种基于 OOPs 的编程语言，非常适合构建高性能的应用程序。C++在需要高速度和高精度的应用中得到应用，例如操作系统、游戏应用、图形用户界面(GUI)和嵌入式系统。下面的项目将使用 Visual Studio 中最流行的 c++IDE。你也可以在记事本或 Textpad 这样的文本编辑器上编写程序，然后使用 GCC 这样的编译器编译它们。其他一些流行的 ide 是 Eclipse 和 Code::Blocks。Turbo C++是经过时间考验的 ide 之一，您可以毫无困难地将其用于所有 C++程序。

C++的一些显著特征是:

*   面向对象
*   易于编码和理解
*   丰富的库集
*   高效的内存管理
*   强大而快速

## C++项目将如何帮助你？

练习学习 C++，可以做很多项目，从简单到高级。这些项目中的每一个都会教给你一些新的东西，这样你就熟悉了最重要的主题，这些主题在你构建现实世界的项目时总是会派上用场的。

要处理这些项目，您需要安装一个 IDE。可以从[微软官网](https://visualstudio.microsoft.com/downloads/)下载免费版 Visual Studio。或者你可以从他们的[官网下载 Code::Blocks。](http://www.codeblocks.org/downloads)

## 提升您的 C++技能的热门项目

### 1.登录和注册系统

这是学习 C++文件系统最简单的项目之一。该项目涉及通过询问用户名和密码的用户注册过程。注册成功后，将使用凭据创建一个用户文件。如果用户不存在，登录时将显示错误。您还将学习如何使用 Visual Studio 创建一个简单的项目。

[点击此处查看代码视频。](https://www.youtube.com/watch?v=I_aWPGCaaFA)

### 2.汽车租赁系统

这是一个流行的项目，对于学习键盘事件、日期时间函数和实现 C++登录系统非常有用。该程序为管理员和其他用户提供了单独的菜单。还有基于时间和距离计算票价的方法，包括显示汽车细节、可用性等。

[查看 GitHub 上的源代码。](https://github.com/thegreat1411vrishank/how-to-make-a-car-rental-system-using-c--)

您可以尝试类似音乐商店管理、公交预订或铁路预订系统的其他项目。

### 3.书店库存系统

这是一个简单的项目，系统维护书店的图书库存。如果客户购买了一本书，该书的数量将减少；如果添加了一本书，也会更新该书。注意指针的使用。您可以修改代码，添加一个图书 ID，并根据图书 ID 进行搜索，或者只使用一个参数进行搜索，得到多个结果，等等。

[在这里查看源代码](https://omkarnathsingh.wordpress.com/2016/02/09/c-program-for-book-shop/)。

### 4.学生报告管理系统

通过这个项目，我们可以学到很多关于 C++的输入/输出流和文件管理系统的知识。我们的程序收集学生的详细信息，如姓名、编号、各科分数，并计算他们的分数。这是一个简单的控制台应用程序。请注意，在这个项目中，我们只关注正确的输入，您可以增强它来处理错误的输入。下面是源代码:

```
#include<iostream>
#include<fstream>
#include<iomanip>
using namespace std;

// the class that stores data
class student
{
int rollno;
char name[50];
int eng_marks, math_marks, sci_marks, lang2_marks, cs_marks;
double average;
char grade;

public:
void getdata();
void showdata() const;
void calculate();
int retrollno() const;
}; //class ends here

void student::calculate()
{
average=(eng_marks+math_marks+sci_marks+lang2_marks+cs_marks)/5.0;
if(average>=90)
grade='A';
else if(average>=75)
grade='B';
else if(average>=50)
grade='C';
else
grade='F';
}

void student::getdata()
{
cout<<"\nEnter student's roll number: ";
cin>>rollno;
cout<<"\n\nEnter student name: ";
cin.ignore();
cin.getline(name,50);
cout<<"\nAll marks should be out of 100";
cout<<"\nEnter marks in English: ";
cin>>eng_marks;
cout<<"\nEnter marks in Math:  ";
cin>>math_marks;
cout<<"\nEnter marks in Science:  ";
cin>>sci_marks;
cout<<"\nEnter marks in 2nd language:  ";
cin>>lang2_marks;
cout<<"\nEnter marks in Computer science:  ";
cin>>cs_marks;
calculate();
}
void student::showdata() const
{
cout<<"\nRoll number of student : "<<rollno;
cout<<"\nName of student : "<<name;
cout<<"\nEnglish : "<<eng_marks;
cout<<"\nMaths : "<<math_marks;
cout<<"\nScience : "<<sci_marks;
cout<<"\nLanguage2 : "<<lang2_marks;
cout<<"\nComputer Science :"<<cs_marks;
cout<<"\nAverage Marks :"<<average;
cout<<"\nGrade of student is :"<<grade;
}
int  student::retrollno() const
{
return rollno;
}
//function declaration
void create_student();
void display_sp(int);//display particular record
void display_all(); // display all records
void delete_student(int);//delete particular record
void change_student(int);//edit particular record
//MAIN
int main()
{
char ch;
cout<<setprecision(2); 
do
{
char ch;
int num;
system("cls");
cout<<"\n\n\n\tMENU";
cout<<"\n\n\t1.Create student record";
cout<<"\n\n\t2\. Search student record";
cout<<"\n\n\t3\. Display all students records ";
cout<<"\n\n\t4.Delete student record";
cout<<"\n\n\t5.Modify student record";
cout<<"\n\n\t6.Exit";
cout<<"\n\n\What is your Choice (1/2/3/4/5/6) ";
cin>>ch;
system("cls");
switch(ch)
{
case '1': create_student(); break;
case '2': cout<<"\n\n\tEnter The roll number "; 
cin>>num;
display_sp(num); break;
case '3': display_all(); break;
case '4': cout<<"\n\n\tEnter The roll number: "; 
cin>>num;
delete_student(num);break;
case '5': cout<<"\n\n\tEnter The roll number "; cin>>num;
change_student(num);break;
case '6': cout<<"Exiting, Thank you!";exit(0);
}
}while(ch!='6');
return 0;
}
//write student details to file
void create_student()
{
student stud;
ofstream oFile;
oFile.open("student.dat",ios::binary|ios::app);
stud.getdata();
oFile.write(reinterpret_cast<char *> (&stud), sizeof(student));
oFile.close();
     cout<<"\n\nStudent record Has Been Created ";
cin.ignore();
cin.get();
}
// read file records
void display_all()
{
student stud;
ifstream inFile;
inFile.open("student.dat",ios::binary);
if(!inFile)
{
cout<<"File could not be opened !! Press any Key to exit";
cin.ignore();
cin.get();
return;
}
cout<<"\n\n\n\t\tDISPLAYING ALL RECORDS\n\n";
while(inFile.read(reinterpret_cast<char *> (&stud), sizeof(student)))
{
st.showdata();
cout<<"\n\n====================================\n";
}
inFile.close();
cin.ignore();
cin.get();
}
//read specific record based on roll number
void display_sp(int n)
{
student stud;
ifstream iFile;
iFile.open("student.dat",ios::binary);
if(!iFile)
{
cout<<"File could not be opened... Press any Key to exit";
cin.ignore();
cin.get();
return;
}
bool flag=false;
while(iFile.read(reinterpret_cast<char *> (&stud), sizeof(student)))
{
if(stud.retrollno()==n)
{
  stud.showdata();
flag=true;
}
}
iFile.close();
if(flag==false)
cout<<"\n\nrecord does not exist";
cin.ignore();
cin.get();
}
// modify record for specified roll number
void change_student(int n)
{
bool found=false;
student stud;
fstream fl;
fl.open("student.dat",ios::binary|ios::in|ios::out);
if(!fl)
{
cout<<"File could not be opened. Press any Key to exit...";
cin.ignore();
cin.get();
return;
}
     while(!fl.eof() && found==false)
{
fl.read(reinterpret_cast<char *> (&stud), sizeof(student));
if(stud.retrollno()==n)
{
stud.showdata();
cout<<"\n\Enter new student details:"<<endl;
stud.getdata();
    int pos=(-1)*static_cast<int>(sizeof(stud));
    fl.seekp(pos,ios::cur);
    fl.write(reinterpret_cast<char *> (&stud), sizeof(student));
    cout<<"\n\n\t Record Updated";
    found=true;
}
}
File.close();
if(found==false)
cout<<"\n\n Record Not Found ";
cin.ignore();
cin.get();
}
//delete record with particular roll number
void delete_student(int n)
{
student stud;
ifstream iFile;
iFile.open("student.dat",ios::binary);
if(!iFile)
{
cout<<"File could not be opened... Press any Key to exit...";
cin.ignore();
cin.get();
return;
}
ofstream oFile;
oFile.open("Temp.dat",ios::out);
iFile.seekg(0,ios::beg);
while(iFile.read(reinterpret_cast<char *> (&stud), sizeof(student)))
{
if(stud.retrollno()!=n)
{
oFile.write(reinterpret_cast<char *> (&stud), sizeof(student));
}
}
oFile.close();
iFile.close();
remove("student.dat");
rename("Temp.dat","student.dat");
cout<<"\n\n\tRecord Deleted ..";
cin.ignore();
cin.get();
}
```

### 5.赌场号码猜谜游戏

这是一个令人兴奋的项目，在这里我们将了解用于随机数的库:cstdlib。该计划要求一个投注金额，然后要求用户猜一个数字滚动。如果生成的随机数与用户输入的相匹配，他就赢了，否则钱会被扣除。用户可以继续玩，直到他输掉最初投入的所有金额。下面是源代码:

```
#include <iostream>
#include <string> // Needed to use strings
#include <cstdlib> // Needed to use random numbers
#include <ctime>
using namespace std;
void rules();
int main()
{
    string playerName;
    int balance; // stores player's balance
    int bettingAmount;
    int guess;
    int dice; // stores the random number
    char choice;
    srand(time(0)); // "Seed" the random generator
    cout << "\n\t\t========WELCOME TO CASINO WORLD=======\n\n";
    cout << "\n\nWhat's your Name : ";
    getline(cin, playerName);
    cout << "\n\nEnter the starting balance to play game : $";
    cin >> balance;
    do
    {
        system("cls");
        rules();
        cout << "\n\nYour current balance is $ " << balance << "\n";
// Get player's betting balance
        do
        {
            cout << "Hey, " << playerName<<", enter amount to bet : $";
            cin >> bettingAmount;
            if(bettingAmount > balance)
                cout << "Betting balance can't be more than current balance!\n"
                       <<"\nRe-enter balance\n ";
        }while(bettingAmount > balance);
// Get player's numbers
        do
        {
            cout << "Guess any betting number between 1 & 10 :";
            cin >> guess;
            if(guess <= 0 || guess > 10)
                cout << "\nNumber should be between 1 to 10\n"
                    <<"Re-enter number:\n ";
        }while(guess <= 0 || guess > 10);
        dice = rand()%10 + 1;
        if(dice == guess)
        {
            cout << "\n\nYou are in luck!! You have won Rs." << bettingAmount * 10;
            balance = balance + bettingAmount * 10;
        }
        else
        {
            cout << "Oops, better luck next time !! You lost $ "<< bettingAmount <<"\n";
            balance = balance - bettingAmount;
        }
        cout << "\nThe winning number was : " << dice <<"\n";
        cout << "\n"<<playerName<<", You have balance of $ " << balance << "\n";
        if(balance == 0)
        {
            cout << "You have no money to play ";
            break;
        }
        cout << "\n\n-->Do you want to play again (y/n)? ";
        cin >> choice;
    }while(choice =='Y'|| choice=='y');
    cout << "\n\n\n";
    cout << "\n\nThanks for playing the game. Your balance is $ " << balance << "\n\n";
    return 0;
}
void rules()
{
    system("cls");
    cout << "\t\t======CASINO NUMBER GUESSING RULES!======\n";
    cout << "\t1\. Choose a number between 1 to 10\n";
    cout << "\t2\. Winner gets 10 times of the money bet\n";
    cout << "\t3\. Wrong bet, and you lose the amount you bet\n\n";
}

```

### 6.数独游戏

我们都知道流行的数独游戏，其中我们需要排列数字 1-9，使它们在 9x9 网格的行和列中只出现一次。这个程序使用回溯的概念。在这个程序中，我们已经对初始值进行了硬编码，但是您也可以从用户那里获得相同的输入(尽管这对这个程序来说很麻烦)。需要理解的主要内容是回溯查找没有赋值(为零)的行和列。看看这个程序，执行它，看看结果:

```
#include <iostream>
#include <cstdio>
#include <cstring>
#include <cstdlib>
using namespace std;
#define empty 0
#define N 9
bool isGridSafe(int grid[N][N], int row, int col, int num);
bool isEmptyLocation(int grid[N][N], int &row, int &col);
/* assign values to all the zero (not assigned) values for Sudoku solution
 */
bool SolveSudoku(int grid[N][N])
{
    int row, col;
    if (!isEmptyLocation(grid, row, col))
       return true;
    for (int num = 1; num <= 9; num++)
    {
        if (isGridSafe(grid, row, col, num))
        {
            grid[row][col] = num;
            if (SolveSudoku(grid))
                return true;
            grid[row][col] = empty;
        }
    }
    return false;
}
/* Check for entries that don't have a value. */
bool isEmptyLocation(int grid[N][N], int &row, int &col)
{
    for (row = 0; row < N; row++)
        for (col = 0; col < N; col++)
            if (grid[row][col] == empty)
                return true;
    return false;
}
/* Returns whether the assigned entry n in the particular row matches
   the given number num. */
bool UsedInRow(int grid[N][N], int prow, int number)
{
    for (int col = 0; col < N; col++)
        if (grid[prow][col] == number)
            return true;
    return false;
}
/* Returns true if the number num matches any number in the column */
bool UsedInCol(int grid[N][N], int pcol, int number)
{
    for (int row = 0; row < N; row++)
        if (grid[row][pcol] == number)
            return true;
  else 
     return false;
//Check if the entry used already in the grid box
bool UsedInBox(int grid[N][N], int boxBeginRow, int boxBeginCol, int number)

{
    bool tf = false;
    for (int row = 0; row < 3; row++)
        for (int col = 0; col < 3; col++)
            if (grid[row+boxBeginRow][col+boxBeginCol] == number)
                tf = true;
    return tf;
}
/* Checks if num can be assigned to a given prow,pcol location. */
bool isGridSafe(int grid[N][N], int prow, int pcol, int number)
{
    return !UsedInRow(grid, prow, number) && !UsedInCol(grid, pcol, number) &&
           !UsedInBox(grid, prow - prow % 3 , pcol - pcol % 3, number);
}
/* print result  */
void printResult(int finalgrid[N][N])
{
    for (int row = 0; row < N; row++)
    {
        for (int col = 0; col < N; col++)
            cout<< finalgrid[row][col]<<"  ";
        cout<<endl;
    }
}
/* Main */
int main()
{
    int grid[N][N] = {{0, 0, 0, 0, 0, 0, 0, 0, 0},
                      {0, 0, 0, 0, 0, 3, 0, 8, 5},
                      {0, 0, 1, 0, 2, 0, 0, 0, 0},
                      {0, 0, 0, 5, 0, 7, 0, 0, 0},
                      {0, 0, 4, 0, 0, 0, 1, 0, 0},
                      {0, 9, 0, 0, 0, 0, 0, 0, 0},
                      {5, 0, 0, 0, 0, 0, 0, 7, 3},
                      {0, 0, 2, 0, 1, 0, 0, 0, 0},
                      {0, 0, 0, 0, 4, 0, 0, 0, 9}}; 
if (SolveSudoku(grid) == true)
          printResult(grid);
    else
        cout<<"No solution found"<<endl;
    return 0;
}
```

### 7.信用卡验证器

这是一个简单的项目，使用 Luhn 的算法来验证用户的信用卡。该计划适用于所有流行的信用卡，如 Visa、Amex、MasterCard 等。Luhn 的算法检查基本验证；例如，Visa 卡应该从 4 开始，然后进行复杂的数字计算。这是一个很好的学习计划，因为大多数电子商务交易需要信用卡验证。

你可以[从 GitHub 网站](https://github.com/karancodes/credit-card-validator/blob/master/credit-card-validator.cpp)下载源代码。

### 8.直升机游戏

对于所有 90 后的孩子来说，这是最受欢迎的游戏之一，而且非常容易实现！在这个项目中，我们将使用 SDL 图形。游戏是在不碰到障碍物的情况下向前移动直升机。玩家应该通过按键来控制游戏，按住按键可以移动直升机，松开按键可以让直升机降落。

[在 GitHub 上找到完整的源代码。](https://github.com/karan-khanna/Helicopter-Game/blob/master/HELI_C-1.CPP)

### 9.使用图形绘制和移动形状

在这个图形程序中，你将学习制作一辆汽车，然后用图形让它移动。这是一个用 Turbo C++写的简单程序；然而，同样的程序也可以在其他 ide 上运行，比如 Dev C++。Code:: Blocks 和 Visual Studios。你必须得到 graphics.h 文件，程序才能运行。

查看 YouTube 链接以了解该计划。

### 10.简单的动画从开始到结束比赛一个喝醉的人

这是一个交互式的控制台动画应用程序，你选择的角色(从 a 到 z 的任何字母)将会有趣地从起点移动到终点。如果他在指定的时间内完成了比赛(在我们的例子中是 1000000)，那么我们打印一条特定的消息，否则打印另一条消息。

看到程序的源代码就明白了。

```
#include<iostream>
#include<cmath>
#include<cstdlib>
#include<ctime>
using namespace std;
int main (){
  srand(time(0));
  const int size=60;
  cout << "Enter a letter to begin \n ";
  char x; cin>> x;
  int position = size /2;
  while (true) {
    cout << "|START|" ;
    for (int i=0; i<size;i++) {
      if (i == position) 
        cout << x;
      else cout << " ";}
    cout << "|FINISH|" << endl;
    int move= rand()%3 - 1;
    position = position + move; 
    if (position <1) {cout << "You could not finish the race!" <<endl; break;}
    if (position >size-1) {cout << "Yay! You finished the race" << endl; break;}
    for(int sleep=0; sleep< 1000000 ; ++ sleep);
  }   
  return 0; 
}
```

## 结论

在本文中，我们讨论了一些重要的初级和中级项目。如果您正确地遵循了代码，您应该会得到准确的输出。尽管 Visual Studio 提供了许多特性，但下载需要时间，所以如果您想继续使用其他 IDE，也没关系。这些项目可以在任何 IDE 上运行。请在评论区告诉我们你尝试了哪些项目！

想在开始你的第一个 C++项目之前学习 C++？udemy 的 C++编程入门课程是开启你 C++之旅的绝佳课程。

**人也在读:**