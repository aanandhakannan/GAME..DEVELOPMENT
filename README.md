# EX 7 : THREE DIMENSIONAL TRANSFORMATIONS

NAME : AANANDHA KANNAN S

REG NO : 212224040003

## AIM :
 
 To implement the various transformations on three dimensional odjects using a c coding.

## EQUIPMENT REQUIRED:

●	Hardware: Personal Computer (PC)

●	Software: C Compiler

## ALGORITHM :


   Step 1 : Start.

   Step 2 : Draw an image with default parameters.

   Step 3 : Get the choice from user.

   Step 4 : Get the parameters for transformation.

   Step 5 : Perform the transformation.

   Step 6 : Display the output.

   Step 7 : Stop.

## Program :
```
#include<stdio.h> 
#include<conio.h> 
#include<graphics.h> 
#include<math.h> 
int maxx,maxy,midx,midy; 
void axis() 
{ 
getch(); 
cleardevice(); 
line(midx,0,midx,maxy); 
line(0,midy,maxx,midy); 
} 
void main() 
{ 
int gd,gm,x,y,z,o,x1,x2,y1,y2; 
detectgraph(&gd,&gm); 
initgraph(&gd,&gm," "); 
setfillstyle(0,getmaxcolor()); 
maxx=getmaxx(); 
maxy=getmaxy(); 
midx=maxx/2; 
midy=maxy/2; 
axis(); 
bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
printf("Enter Translation Factor"); 
scanf("%d%d%d",&x,&y,&z); 
axis(); 
printf("after translation"); 
bar3d(midx+(x+50),midy-(y+100),midx+x+60,midy-(y+90),5,1); 
axis(); 
bar3d(midx+50,midy+100,midx+60,midy-90,5,1); 
printf("Enter Scaling Factor"); 
scanf("%d%d%d",&x,&y,&z); 
axis(); 
printf("After Scaling"); 
bar3d(midx+(x*50),midy-(y*100),midx+(x*60),midy-(y*90),5*z,1); 
axis(); 
bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
printf("Enter Rotating Angle"); 
scanf("%d",&o); 
x1=50*cos(o*3.14/180)-100*sin(o*3.14/180); 
y1=50*cos(o*3.14/180)+100*sin(o*3.14/180); 
x2=60*sin(o*3.14/180)-90*cos(o*3.14/180); 
y2=60*sin(o*3.14/180)+90*cos(o*3.14/180); 
axis(); 
printf("After Rotation about Z Axis"); 
bar3d(midx+x1,midy-y1,midx+x2,midy-y2,5,1); 
axis(); 
printf("After Rotation about X Axis"); 
bar3d(midx+50,midy-x1,midx+60,midy-x2,5,1); 
axis(); 
printf("After Rotation about Y Axis"); 
bar3d(midx+x1,midy-100,midx+x2,midy-90,5,1); 
getch(); 
closegraph(); 
}
```

## Output :

![image](https://github.com/user-attachments/assets/f26af567-5c27-4843-b952-e344d14c5277)

![image](https://github.com/user-attachments/assets/10d9c354-873e-4e3c-81b3-1731750e0438)

![image](https://github.com/user-attachments/assets/838fdb27-5b41-43f9-b6aa-59faf765f448)

![image](https://github.com/user-attachments/assets/5a8fc296-403b-4b19-b514-95039407a50a)

![image](https://github.com/user-attachments/assets/43cf1b94-b34c-4570-80d6-a57ed3cb6dbc)

![image](https://github.com/user-attachments/assets/99c586b9-43b9-409d-9235-1fff47058ff0)

![image](https://github.com/user-attachments/assets/26c6b515-f89d-4676-b316-572be754768f)

![image](https://github.com/user-attachments/assets/5e85d931-c428-4a11-8c32-f2c0e341ce25)

## Result :

Thus, the C program for performing three-dimensional transformations — including translation,scaling, and rotation about the X, Y, and Z axes — was successfully implemented and the output was verified through graphical representation.
