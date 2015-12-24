# b-i-t-p-v-C-



#include<iostream>
#include<conio.h>
using namespace std;
int main()
{
    //khai bao bien int
    int a,b,c,tam,i,tongsongay;
    cout<<"   __________________________________________________________________"<<endl;
    cout<<"  |CHUONG TRINH NHAP VAO MOT NGAY BAT KY IN RA MAN HINH DO LA THU MAY|"<<endl;
    cout<<"  |__________________________________________________________________|"<<endl;
    cout<<"                 nhom 2 xin tran trong duoc trinh bay"<<endl;
    cout<<"                 ************************************"<<endl;
    cout<<endl;
    //khai bao bien cua ngay
    cout<<"   moi ban nhap vao ngay/thang/nam :"<<endl;
    cout<<endl;
    cout<<"   moi nhap ngay(date): ";
    cin>>a;
    cout<<endl;
    while(a<1||a>31)
    {
                    cout<<"   moi nhap lai ngay(date): ";
                    cin>>a;
    }
    //khai bao bien cua thang
    cout<<"   nhap thang(month): ";
    cin>>b;
    cout<<endl;
    while(b<1||b>12)
    {
                    cout<<"   moi nhap lai thang(month): ";
                    cin>>b;
    }
    //khai bao bien cua nam
    cout<<"   nhap nam(year): ";
    cin>>c;
    cout<<endl;
    while(c<0)
    {
              cout<<"   moi nhap lai nam: ";
              cin>>c;
    }
    tam=0;
    //tinh so ngay cua chi so nam khi nguoi dung nhap vao
    for(i=1;i<c;i++)
    {
                     if((i%4==0&&i%100!=0)||i%400==0)
                     {
                             tam=tam+366;
                     }
                     else
                     {
                         tam=tam+365;
                     }
    }
    /*tu khi có lich cho den nam 1582 nguoi ta thay lich da bi lech 11 ngay nen
    nguoi nguoi ta da bo bot di 11 ngay cho no phu hop voi mua mang va cac dip le
    */
    if(c>=1582)
    {
               tam=tam-11;
    }
    /* liet ke ra cac truong hop neu nhu la nam nhuan thi thang 2 co 29 ngay con neu khong phai thi 28 ngay
    cu nhu vay den het cac thang trong nam
    */
     if(b==1)
    {
            tongsongay=a+tam;
    }
    if(b==2)
    {
            tongsongay=a+tam+31;
    }
    /*neu nhu la nam khong nhuan thi thang hai chi den ngay 28 thoi 
    con neu nhu nguoc lai thi nam do thang hai nguoi dung co the nhap vao toi da la 29
    */
    if(b==2&&a>=29&&c%4!=0)
    {
            cout<<"khong co ngay nay";
            getch();
    }
    if(b==2&&a>=30&&(i%4==0&&i%100!=0)||i%400==0)
    {
            cout<<"khong co ngay nay";
            getch();
    }
    //liet ke cac thang tiep theo
    if(b==3&&c%4!=0)
    {
            tongsongay=a+tam+28;
    }
    if(b==3&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+29;
    }
    if(b==4&&c%4!=0)
    {
            tongsongay=a+tam+90;
    }
    if(b==4&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+91;    
    }
    if(b==5&&c%4!=0)
    {
            tongsongay=a+tam+120;
    }
    if(b==5&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+121;
    }
    if(b==6&&c%4c=0)
    {
            tongsongay=a+tam+151;
    }
    if(b==6&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+152;
    }
    if(b==7&&c%4!=0)
    {
            tongsongay=a+tam+181;
    }
    if(b==7&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+182;
    }
    if(b==8&&c%4!=0)
    {
            tongsongay=a+tam+212;
    }
    if(b==8&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+213;
    }
    if(b==9&&c%4!=0)
    {
            tongsongay=a+tam+243;
    }
    if(b==9&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+244;
    }
    if(b==10&&c%4!=0)
    {
            tongsongay=a+tam+273;
    }
    if(b==10&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+274;
    }
    if(b==11&&c%4!=0)
    {
            tongsongay=a+tam+304;
    }
    if(b==11&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+305;
    }
    if(b==12&&c%4!=0)
    {
            tongsongay=a+tam+334;
    }
    if(b==12&&(i%4==0&&i%100!=0)||i%400==0)
    {
            tongsongay=a+tam+335;
    }
    /*co tong so ngay roi thi chung ta lay tong so ngay do di chia cho 7
     roi chung ta liet ke ra tung truong hop tuong ung voi cac ngay trong tuan
     */
    if(tongsongay%7==1)
    {
                       cout<<"^^ ngay "<<a<<"/"<<b<<"/"<<c;
                       cout<<" ^^la ngay thu 6 ^^";
    }
    if(tongsongay%7==2)
    {
                       cout<<"^^ ngay "<<a<<"/"<<b<<"/"<<c;
                       cout<<" ^^ la ngay thu 7";
    }
    if(tongsongay%7==3)
    {
                       cout<<"^^ ngay "<<a<<"/"<<b<<"/"<<c;
                       cout<<" ^^ la ngay chu nhat";
    }
    if(tongsongay%7==4)
    {
                       cout<<"^^ ngay "<<a<<"/"<<b<<"/"<<c;
                       cout<<" ^^ la ngay thu 2";
    }
    if(tongsongay%7==5)
    {
                       cout<<"^^ ngay "<<a<<"/"<<b<<"/"<<c;
                       cout<<" ^^ la ngay thu 3";
    }
    if(tongsongay%7==6)
    {
                       cout<<"^^ ngay "<<a<<"/"<<b<<"/"<<c;
                       cout<<" ^^ la ngay thu 4";
    }
    if(tongsongay%7==0)
    {
                       cout<<"^^ ngay "<<a<<"/"<<b<<"/"<<c;
                       cout<<" ^^ la ngay thu 5";
    }
    cout<<endl;
    cout<<"   *** cam on ban da su dung chuong trinh cua chung toi ***";
    getch();
}
