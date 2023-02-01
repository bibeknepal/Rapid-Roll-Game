#include<stdio.h>
#include<dos.h>
#include<conio.h>
#include<graphics.h>
#include<stdlib.h>
	int x1=60,y1=70,x2=150,y2=90;//rod1
	int a1=454,a2=144,a3=564,a4=164;//rod2
	int b1=50,b2=218,b3=160,b4=238;//rod3
	int c1=400,c2=282,c3=510,c4=302;//rod4
	int d1=150,d2=356,d3=260,d4=376;//rod5
	int i=1,x=455,y=270,r=10;//circle
	int a11=30,x11=20,x22=35,y11=25,y22=50,w22=479,z22=464,i1=0;//spikes
	int randomnum,randomnum1,randomnum2,randomnum3,randomnum4;//for storing random numbers
	char ch,key;
	int gd=0,gm;//graphics driver and graphics mode
	int m1=5,m2=5;//movement of ball
	int nx1=210,ny1=160,nx2=370,ny2=190;//select rectangle
	int nx11=210,ny11=210,nx22=370,ny22=240;//select rectangle
void layout()
{
	setcolor(RED);
	setfillstyle(1,RED);
	rectangle(0,0,639,35);//top rectanlge
	floodfill(22,22,RED);
	setfillstyle(9,RED);
	rectangle(0,35,20,479);//left rectangle
	floodfill(1,36,RED);
	rectangle(639,35,619,479);//right rectangle
	floodfill(624,300,RED);
	setcolor(RED);//spikes
	line(x11,x22,y11,y22);
	line(a11,x22,y11,y22);
	line(0,479,639,479);//bottom straight line
	line(x11,w22,y11,z22);
	line(a11,w22,y11,z22);
	for(i1=0;i1<59;i1++)//loop for spikes
	{
		x11=x11+10;
		y11=y11+10;
		a11=a11+10;
		setcolor(RED);
		line(x11,x22,y11,y22);
		line(a11,x22,y11,y22);
		line(x11,w22,y11,z22);
		line(a11,w22,y11,z22);
	}
}
void stxt()//start text
{
	setcolor(YELLOW);
	rectangle(210,200,390,265);
	rectangle(200,190,400,275);
	settextstyle(2,0,25);
	outtextxy(245,210,"READY");
	getch();
	setcolor(BLACK);
	rectangle(210,200,390,265);
	rectangle(200,190,400,275);
	settextstyle(2,0,25);
	outtextxy(245,210,"READY");
}
void replacecircle()
{
	setfillstyle(1,BLACK);
	floodfill(x,y,BLACK);
	setcolor(BLUE);
	circle(x,y,r);
	setfillstyle(1,BLUE);
	floodfill(x,y,BLUE);
}
void ballmovement1()
{
	key=getch();
	if(key==0)
	{
		key=getch();
		if(key==77)//ascii value of right arrow
		{
			x=x+m1;
		}
		if(key==75)//ascii value of left arrow
		{
			x=x-m1;
		}
	}
	if(key==27)//ascii value of esc
	{
		exit(1);
	}
}
void ballmovement2()
{
	key=getch();
	if(key==0)
	{
		key=getch();
		if(key==77)//ascii value of right arrow
		{
			x=x+m2;
		}
		if(key==75)//ascii value of left arrow
		{
			x=x-m2;
		}
	}
	if(key==27)//ascii value of esc
	{
		exit(1);
	}
}
void rod_move()//upward movement of rod
{
	y1--;y2--;
	a2--;a4--;
	b2--;b4--;
	c2--;c4--;
	d2--;d4--;
}
void replaceball()
{
	setcolor(BLACK);//replace start menu
	settextstyle(10,0,5);
	outtextxy(110,50,"RAPID R  LL");
	setfillstyle(1,BLACK);
	circle(393,102,28);
	floodfill(393,102,BLACK);
	circle(393,102,28);
	setfillstyle(0,BLACK);
	circle(379,88,1);
	circle(375,91,2);
	floodfill(379,88,BLACK);
	floodfill(375,91,BLACK);
}
void replacesubmenu()
{
	setcolor(BLACK);
	rectangle(200,200,380,300);
	settextstyle(8,0,2);
	line(200,250,380,250);
	outtextxy(215,155,"SELECT MODE:");
	outtextxy(223,210,"SCORE MODE");
	outtextxy(240,260,"SURVIVAL");
	rectangle(nx11,ny11,nx22,ny22);
}
void replacehalfmenu()
{
	setcolor(BLACK);
	rectangle(200,150,380,350);
	line(200,200,380,200);
	line(200,250,380,250);
	line(200,300,380,300);
	rectangle(200,150,380,350);
	settextstyle(8,0,2);
	outtextxy(260,160,"PLAY");
	outtextxy(224,210,"HIGH SCORE");
	outtextxy(254,260,"ABOUT");
	outtextxy(265,310,"EXIT");
	rectangle(nx1,ny1,nx2,ny2);
}
void main()
{
	int check=1,c=0,highscore,a=0,countscore=1,score=0,de1=7,de2=7,s=0;//d=delay
	char scoredisp[10],times[5],highs[10];//setting score and highscore upto 10 digits
	int q=1,k=1,p=1;
	FILE *fp;
	initgraph(&gd,&gm,"C://TURBOC3/BGI");//path for gd and gm
	up:
	setcolor(YELLOW);//display rapid roll in start menu
	settextstyle(10,0,5);
	outtextxy(110,50,"RAPID R  LL");
	setcolor(BLUE);
	setfillstyle(1,BLUE);
	circle(393,102,28);
	floodfill(393,102,BLUE);
	setcolor(YELLOW);
	circle(393,102,28);
	setcolor(WHITE);
	setfillstyle(1,WHITE);
	circle(379,88,1);
	circle(375,91,2);
	floodfill(379,88,WHITE);
	floodfill(375,91,WHITE);
	setcolor(RED);
	rectangle(200,150,380,350);
	setcolor(WHITE);
	line(200,200,380,200);
	line(200,250,380,250);
	line(200,300,380,300);
	rectangle(200,150,380,350);
	setcolor(YELLOW);
	settextstyle(8,0,2);
	outtextxy(260,160,"PLAY");
	outtextxy(224,210,"HIGH SCORE");
	outtextxy(254,260,"ABOUT");
	outtextxy(265,310,"EXIT");
	setcolor(3);//select rectangle
	rectangle(nx1,ny1,nx2,ny2);
	while(1)
	{
		ch=getch();
		if(ch==0)
		{
		   ch=getch();
		   if (ch==80)//ascii value of down arrow
		   {
			if(ny2<=300)
			{
				setcolor(BLACK);
				rectangle(nx1,ny1,nx2,ny2);
				setcolor(3);
				rectangle(nx1,ny1+50,nx2,ny2+50);
				ny1=ny1+50;
				ny2+=50;
				q=q+1;
			}
		   }
		   if(ch==72)//ascii value of up arrow
		   {
			if(ny1>=210)
			{
				setcolor(BLACK);
				rectangle(nx1,ny1,nx2,ny2);
				setcolor(3);
				rectangle(nx1,ny1-50,nx2,ny2-50);
				ny1=ny1-50;
				ny2-=50;
				q=q-1;
			}
		   }
		}
		if(ch==13)//ascii value of enter
		{
			if(q==1)
			{
				replacehalfmenu();
				setcolor(YELLOW);
				outtextxy(215,155,"SELECT MODE:");
				settextstyle(8,0,2);
				outtextxy(223,210,"SCORE MODE");
				outtextxy(240,260,"SURVIVAL");
				setcolor(WHITE);
				line(200,250,380,250);
				rectangle(200,200,380,300);
				setcolor(3);//select rectangle
				rectangle(nx11,ny11,nx22,ny22);
				while(k==1)
				{
					if (ch==80)//ascii value of down arrow
					{
						if(ny22<=240)
						{
							setcolor(BLACK);
							rectangle(nx11,ny11,nx22,ny22);
							setcolor(3);
							rectangle(nx11,ny11+50,nx22,ny22+50);
							ny11=ny11+50;
							ny22+=50;
							p=p+1;
						}
					}
					if(ch==72)//ascii value of up arrow
					{
						if(ny11>=260)
						{
							setcolor(BLACK);
							rectangle(nx11,ny11,nx22,ny22);
							setcolor(3);
							rectangle(nx11,ny11-50,nx22,ny22-50);
							ny11=ny11-50;
							ny22-=50;
							p=p-1;
						}
					 }
					ch=getch();
					if(ch==8)
					{
						replaceball();
						replacesubmenu();
						goto up;
					}
					if(ch==13)
					{
						if(p==1)
							{
								replaceball();
								replacesubmenu();
								goto scoremode;
							}
						if(p==2)
							{
								replaceball();
								replacesubmenu();
								goto timemode;
							}

					 }
				}
			}
			if(q==2)
			{
				replacehalfmenu();
				fp=fopen("C://TURBOC3/Projects/highscore.txt","r");//opening highscore file in read mode
				fscanf(fp,"%d",&highscore);
				fprintf(fp,"%d",a);
				fclose(fp);
				setcolor(YELLOW);//display highscore
				settextstyle(8,0,5);
				outtextxy(180,140,"HIGHSCORE:");
				settextstyle(8,0,2);
				sprintf(highs,"%d",highscore);
				outtextxy(390,220,highs);

				fp=fopen("C://TURBOC3/Projects/hightime.txt","r");//opening highscore file in read mode
				fscanf(fp,"%d",&highscore);
				fprintf(fp,"%d",a);
				fclose(fp);
				settextstyle(8,0,2);
				outtextxy(210,220,"a. SCORE MODE:");
				outtextxy(210,260,"b. SURVIVAL  :");
				sprintf(highs,"%d",highscore);
				outtextxy(390,260,highs);
				input1:
				key=getch();
				if(key==8)//ascii value of backspace
				{
					setcolor(BLACK);
					replaceball();
					fp=fopen("C://TURBOC3/Projects/highscore.txt","r");//opening highscore file in read mode
					fscanf(fp,"%d",&highscore);
					fprintf(fp,"%d",a);
					fclose(fp);
					settextstyle(8,0,5);
					outtextxy(180,140,"HIGHSCORE:");
					settextstyle(8,0,2);
					sprintf(highs,"%d",highscore);
					outtextxy(390,220,highs);
					outtextxy(210,220,"a. SCORE MODE:");
					outtextxy(210,260,"b. SURVIVAL  :");

					fp=fopen("C://TURBOC3/Projects/hightime.txt","r");//opening highscore file in read mode
					fscanf(fp,"%d",&highscore);
					fprintf(fp,"%d",a);
					fclose(fp);
					sprintf(highs,"%d",highscore);
					outtextxy(390,260,highs);
					goto up;
				}
				else
				{
					goto input1;
				}
			}
			if(q==3)
			{
				replaceball();
				replacehalfmenu();
				setcolor(WHITE);//diplay contents in about
				settextstyle(2,0,8);
				outtextxy(245,10,"RAPID ROLL:");
				settextstyle(2,0,6);
				outtextxy(15,50,"Rapid Roll : Roll the ball is a kind of fall down game with a lot");
				outtextxy(3,70,"of fun and challenges. Your mission is to move the ball between the");
				outtextxy(3,90,"platforms without crashing into neither the top, the bottom nor the");
				outtextxy(3,110,"spikes. This game is developed in C language. As you go, you must");
				outtextxy(3,130,"continue to run in each platform inorder to socre a point. Staying");
				outtextxy(3,150,"too long on a platform also causes you to lose the game because");
				outtextxy(3,170,"lingering causes the platform to push you up into spikes that lies");
				outtextxy(3,190,"in the top.");
				settextstyle(2,0,4);
				outtextxy(400,450,"Copyright 2019 NOOBS.All Rights Reserved.");
				outtextxy(1,450,"Version: 2.0(up to date)");
				input:
				key=getch();
				if (key==8)
				{
					setcolor(BLACK);
					settextstyle(2,0,8);
					outtextxy(245,10,"RAPID ROLL:");
					settextstyle(2,0,6);
					outtextxy(15,50,"Rapid Roll : Roll the ball is a kind of fall down game with a lot");
					outtextxy(3,70,"of fun and challenges. Your mission is to move the ball between the");
					outtextxy(3,90,"platforms without crashing into neither the top, the bottom nor the");
					outtextxy(3,110,"spikes. This game is developed in C language. As you go, you must");
					outtextxy(3,130,"continue to run in each platform inorder to socre a point. Staying");
					outtextxy(3,150,"too long on a platform also causes you to lose the game because");
					outtextxy(3,170,"lingering causes the platform to push you up into spikes that lies");
					outtextxy(3,190,"in the top.");
					settextstyle(2,0,4);
					outtextxy(400,450,"Copyright 2019 NOOBS.All Rights Reserved.");
					outtextxy(1,450,"Version: 2.0(up to date)");
					goto up;
				}
				else
				{
					goto input;
				}
			}
			if(q==4)
			{
			       exit(1);
			}

		}
	}
	scoremode:
	fp=fopen("C://TURBOC3/Projects/highscore.txt","r");//opeing highscore file in read mode
	if(fp==NULL)//creating highscore file if highscore file isn't created
	{
		fp=fopen("C://TURBOC3/Projects/highscore.txt","w");//opening highscore file in write mode
		fprintf(fp,"%d",a);
		fclose(fp);//closing highsocre file
		fp=fopen("C://TURBOC3/Projects/highscore.txt","r");
	}
	fscanf(fp,"%d",&highscore);
	fclose(fp);
	setbkcolor(BLACK);//background color
	layout();
	stxt();
	setcolor(YELLOW);
	settextstyle(8,0,1);
	outtextxy(430,10,"SCORE:");
	outtextxy(78,10,"HIGHSCORE:");
	sprintf(highs,"%d",highscore);//initial highscore
	outtextxy(200,10,highs);
	sprintf(scoredisp,"%d",score);//initial score
	outtextxy(495,10,scoredisp);

	setcolor(BLUE);//initial circle
	circle(x,y,r);
	setfillstyle(1,BLUE);
	floodfill(x,y,BLUE);
     while(i==1)
     {
		setcolor(GREEN);//randoming safe rod
		rectangle(x1+randomnum,y1,x2+randomnum,y2);
		setfillstyle(1,GREEN);
		floodfill(x1+randomnum+1,y1+1,GREEN);
		rectangle(a1-randomnum1,a2,a3-randomnum1,a4);
		setfillstyle(1,GREEN);
		floodfill(a1-randomnum1+1,a2+1,GREEN);
		rectangle(c1-randomnum3,c2,c3-randomnum3,c4);
		setfillstyle(1,GREEN);
		floodfill(c1-randomnum3+1,c2+1,GREEN);

		setcolor(RED);//randoming danger rod
		rectangle(b1+randomnum2,b2,b3+randomnum2,b4);
		setfillstyle(1,RED);
		floodfill(b1+randomnum2+1,b2+1,RED);
		rectangle(d1+randomnum4,d2,d3+randomnum4,d4);
		setfillstyle(1,RED);
		floodfill(d1+randomnum4+1,d2+1,RED);

		setcolor(BLACK);//replacing rods
		line(x1+randomnum,y2,x2+randomnum,y2);
		line(a1-randomnum1,a4,a3-randomnum1,a4);
		line(b1+randomnum2,b4,b3+randomnum2,b4);
		line(c1-randomnum3,c4,c3-randomnum3,c4);
		line(d1+randomnum4,d4,d3+randomnum4,d4);
		if(check==1)
		{
			check=0;
			getch();
		}
	if(kbhit())//condition for ball not exceeding layout
	{
		if(x-r<28)
		{
			x+=m1;
		}
		else if(x+r>613)
		{
			x-=m1;
		}
		else
		{
			ballmovement1();
		}
	}
	else if(!kbhit())
	{
		if((x>x1+randomnum-r && x<x2+randomnum+r && y+r+2==y1) || (x>a1-randomnum1-r && x<a3-randomnum1+r && y+r+2==a2) || (x>c1-randomnum3-r &&x<c3-randomnum3+r && y+r+2==c2) )
		{
			setcolor(RED);//condition for increasing score
			settextstyle(8,0,1);
			outtextxy(495,10,scoredisp);
			if(countscore==1)
			{
				score++;
				if((score+1)%10==0)
				{
					de1-=2;
					m1++;
				}
				countscore=0;
			}
			sprintf(scoredisp,"%d",score);
			setcolor(YELLOW);
			outtextxy(495,10,scoredisp);
			if(y-r==52)
			{
				goto gameover;
			}
			else
			{
				y--;    //ball+rod moving condition
				rod_move();
				delay(de1);
			}
		}
		else if((x+r+2>=b1+randomnum2 && x-r-2<=b3+randomnum2 && y+r+2==b2) || (x+r+2>=d1+randomnum4 && x-r-2<=d3+randomnum4 && y+r+2==d2)|| (x+r+2>=b1+randomnum2 && x-r-2<=b3+randomnum2 && y+r+1>=b2 && y<=b4) || (x+r+2>=d1+randomnum4 && x-r-2<=d3+randomnum4 && y+r+1>=d2 && y<=d4) )
		{
			goto gameover;
		}
		else
		{
			countscore=1;
			if(y+r==z22-2)
			{
				goto gameover;
			}
			else
			{
				y++; //ball and rod moving condition
				replacecircle();
				rod_move();
				delay(de1);
			}
		}
	}
	if(y1<=52)//loop for rod1
	{
		rectangle(x1+randomnum,y1,x2+randomnum,y2);
		setfillstyle(1,BLACK);
		floodfill(x1+randomnum+1,y1+1,BLACK);
		y1=440;
		y2=460;
		randomnum=random(470);
	}
	if(a2<=52)//loop for rod2
	{
		rectangle(a1-randomnum1,a2,a3-randomnum1,a4);
		setfillstyle(1,BLACK);
		floodfill(a1-randomnum1+1,a2+1,BLACK);
		a2=440;
		a4=460;
		randomnum1=random(400);
	}
	if(b2<=52)//loop for rod3
	{
		rectangle(b1+randomnum2,b2,b3+randomnum2,b4);
		setfillstyle(1,BLACK);
		floodfill(b1+randomnum2+1,b2+1,BLACK);
		b2=440;
		b4=460;
		randomnum2=random(450);
	}
	if(c2<=52)//loop for rod4
	{
		rectangle(c1-randomnum3,c2,c3-randomnum3,c4);
		setfillstyle(1,BLACK);
		floodfill(c1-randomnum3+1,c2+1,BLACK);
		c2=440;
		c4=460;
		randomnum3=random(350);
	}
	if(d2<=52)//loop for rod5
	{
		rectangle(d1+randomnum4,d2,d3+randomnum4,d4);
		setfillstyle(1,BLACK);
		floodfill(d1+randomnum4+1,d2+1,BLACK);
		d2=440;
		d4=460;
		randomnum4=random(350);
	}
	replacecircle();
     }
	gameover:
	setcolor(YELLOW);//display gameover
	settextstyle(2,0,10);
	outtextxy(210,205,"GAMEOVER");
	rectangle(185,200,420,255);
	rectangle(175,190,430,265);
	if(score>highscore)//condition for replacing highscore if score is greater than previous highscore
	{
		FILE *fp;
		fp=fopen("C://TURBOC3/Projects/highscore.txt","w");
		fprintf(fp,"%d",score);
		fclose(fp);
	}
	while(1)
	{
		ch=getch();
		if(ch==114)//ascii value of 'r'
		{
			clrscr();//clearing screen and re-declaring the original values
			x1=60;y1=70;x2=150;y2=90;//rod1
			a1=454; a2=144; a3=564; a4=164;//rod2
			b1=50;b2=218;b3=160;b4=238;//rod3
			c1=400;c2=282;c3=510;c4=302;//rod4
			d1=150;d2=356;d3=260;d4=376;//rod5
			i=1;x=455;y=270;r=10;//circle
			a11=30;x11=20;x22=35;y11=25;y22=50;w22=479;z22=464;i1=0;//spikes
			m1=5;m2=5;//movement of ball
			randomnum=0;randomnum1=0;randomnum2=0;randomnum3=0;randomnum4=0;
			nx1=210;ny1=160;nx2=370;ny2=190;
			nx11=210;ny11=210;nx22=370;ny22=240;//select rectangle
			closegraph();
			main();
		}
		else if(ch==27)//ascii value of esc
		{
			exit(1);
		}
	}
	timemode:
	fp=fopen("C://TURBOC3/Projects/hightime.txt","r");//opeing highscore file in read mode
	if(fp==NULL)//creating highscore file if highscore file isn't created
	{
		fp=fopen("C://TURBOC3/Projects/hightime.txt","w");//opening highscore file in write mode
		fprintf(fp,"%d",a);
		fclose(fp);//closeing highsocre file
		fp=fopen("C://TURBOC3/Projects/hightime.txt","r");
	}
	fscanf(fp,"%d",&highscore);
	fclose(fp);
	setbkcolor(BLACK);//background color
	layout();
	stxt();
	setcolor(YELLOW);
	settextstyle(8,0,1);
	outtextxy(398,10,"TIME(in sec):");
	outtextxy(40,10,"HIGHEST SURVIVAL:");
	outtextxy(279,10,"sec");
	sprintf(highs,"%d",highscore);//initial highscore
	outtextxy(245,10,highs);
	sprintf(times,"%d",s);//initial time
	outtextxy(535,10,times);

	setcolor(BLUE);//initial circle
	circle(x,y,r);
	setfillstyle(1,BLUE);
	floodfill(x,y,BLUE);

	while(i==1)
	{
			sprintf(times,"%d",s);
			setcolor(YELLOW);
			outtextxy(535,10,times);
			c++;
			if(c==95)
			{
			setcolor(RED);//condition for increasing time
			sprintf(times,"%d",s);
			settextstyle(8,0,1);
			outtextxy(535,10,times);
				c=0;
				s++;
			if((s+1)%10==0)
				{
					de2--;
					m2++;
				}
			}

		setcolor(GREEN);//randoming safe rod
		rectangle(x1+randomnum,y1,x2+randomnum,y2);
		setfillstyle(1,GREEN);
		floodfill(x1+randomnum+1,y1+1,GREEN);
		rectangle(a1-randomnum1,a2,a3-randomnum1,a4);
		setfillstyle(1,GREEN);
		floodfill(a1-randomnum1+1,a2+1,GREEN);
		rectangle(c1-randomnum3,c2,c3-randomnum3,c4);
		setfillstyle(1,GREEN);
		floodfill(c1-randomnum3+1,c2+1,GREEN);

		setcolor(RED);//randoming danger rod
		rectangle(b1+randomnum2,b2,b3+randomnum2,b4);
		setfillstyle(1,RED);
		floodfill(b1+randomnum2+1,b2+1,RED);
		rectangle(d1+randomnum4,d2,d3+randomnum4,d4);
		setfillstyle(1,RED);
		floodfill(d1+randomnum4+1,d2+1,RED);

		setcolor(BLACK);//replacing rods
		line(x1+randomnum,y2,x2+randomnum,y2);
		line(a1-randomnum1,a4,a3-randomnum1,a4);
		line(b1+randomnum2,b4,b3+randomnum2,b4);
		line(c1-randomnum3,c4,c3-randomnum3,c4);
		line(d1+randomnum4,d4,d3+randomnum4,d4);

	if(kbhit())//condition for ball not exceeding layout
	{
		if(x-r<28)
		{
			x+=m2;
		}
		else if(x+r>613)
		{
			x-=m2;
		}
		else
		{
			ballmovement2();
		}
	}
	else if(!kbhit())
	{
		if((x>x1+randomnum-r && x<x2+randomnum+r && y+r+2==y1) || (x>a1-randomnum1-r && x<a3-randomnum1+r && y+r+2==a2) || (x>c1-randomnum3-r &&x<c3-randomnum3+r && y+r+2==c2) )
		{
			if(y-r==52)
			{
				goto gameover1;
			}
			else
			{

				y--;    //ball+rod moving condition
				rod_move();
				delay(de2);
			}
		}
		else if((x+r+2>=b1+randomnum2 && x-r-2<=b3+randomnum2 && y+r+2==b2) || (x+r+2>=d1+randomnum4 && x-r-2<=d3+randomnum4 && y+r+2==d2)|| (x+r+2>=b1+randomnum2 && x-r-2<=b3+randomnum2 && y+r+1>=b2 && y<=b4) || (x+r+2>=d1+randomnum4 && x-r-2<=d3+randomnum4 && y+r+1>=d2 && y<=d4) )
		{
			goto gameover1;
		}
		else
		{
			if(y+r==z22-2)
			{
				goto gameover1;
			}
			else
			{
				y++; //ball and rod moving condition
				replacecircle();
				rod_move();
				delay(de2);
			}
		}
	}
	if(y1<=52)//loop for rod1
	{
		rectangle(x1+randomnum,y1,x2+randomnum,y2);
		setfillstyle(1,BLACK);
		floodfill(x1+randomnum+1,y1+1,BLACK);
		y1=440;
		y2=460;
		randomnum=random(470);
	}
	if(a2<=52)//loop for rod2
	{
		rectangle(a1-randomnum1,a2,a3-randomnum1,a4);
		setfillstyle(1,BLACK);
		floodfill(a1-randomnum1+1,a2+1,BLACK);
		a2=440;
		a4=460;
		randomnum1=random(400);
	}
	if(b2<=52)//loop for rod3
	{
		rectangle(b1+randomnum2,b2,b3+randomnum2,b4);
		setfillstyle(1,BLACK);
		floodfill(b1+randomnum2+1,b2+1,BLACK);
		b2=440;
		b4=460;
		randomnum2=random(450);
	}
	if(c2<=52)//loop for rod4
	{
		rectangle(c1-randomnum3,c2,c3-randomnum3,c4);
		setfillstyle(1,BLACK);
		floodfill(c1-randomnum3+1,c2+1,BLACK);
		c2=440;
		c4=460;
		randomnum3=random(350);
	}
	if(d2<=52)//loop for rod5
	{
		rectangle(d1+randomnum4,d2,d3+randomnum4,d4);
		setfillstyle(1,BLACK);
		floodfill(d1+randomnum4+1,d2+1,BLACK);
		d2=440;
		d4=460;
		randomnum4=random(350);
	}
	replacecircle();
     }
	gameover1:
	setcolor(YELLOW);//display gameover
	settextstyle(2,0,10);
	outtextxy(210,205,"GAMEOVER");
	rectangle(185,200,420,255);
	rectangle(175,190,430,265);
	if(s>highscore)//condition for replacing highscore if score is greater than previous highscore
	{
		FILE *fp;
		fp=fopen("C://TURBOC3/Projects/hightime.txt","w");
		fprintf(fp,"%d",s);
		fclose(fp);
	}
	while(1)
	{
		ch=getch();
		if(ch==114)//ascii value of 'r'
		{
			clrscr();//clearing screen and re-declaring the original values
			x1=60;y1=70;x2=150;y2=90;//rod1
			a1=454; a2=144; a3=564; a4=164;//rod2
			b1=50;b2=218;b3=160;b4=238;//rod3
			c1=400;c2=282;c3=510;c4=302;//rod4
			d1=150;d2=356;d3=260;d4=376;//rod5
			i=1;x=455;y=270;r=10;//circle
			a11=30;x11=20;x22=35;y11=25;y22=50;w22=479;z22=464;i1=0;//spikes
			m1=5;m2=5;//movement of ball
			randomnum=0;randomnum1=0;randomnum2=0;randomnum3=0;randomnum4=0;
			nx1=210;ny1=160;nx2=370;ny2=190;
			nx11=210;ny11=210;nx22=370;ny22=240;//select rectangle
			closegraph();
			main();
		}
		else if(ch==27)//ascii value of esc
		{
			exit(1);
		}
	}
}