#include <iostream>
#include <windows.h>

using namespace std;

char Map[10][10] = {"#########",
                    "#  #   !#",
                    "#  # ####",
                    "####?#  #",
                    "#    #  #",
                    "# ####  #",
                    "# #     #",
                    "# #     #",
                    "#@#     #",
                    "#########"};

int gamespeed = 1;
int Level = 1;
bool stopgame = false;
int hp = 100;
int maxhp = 100;

int main(){
    while(stopgame == false && Level == 1)
    {
        system("cls");
        for (int y = 0; y<10; y++)
        {
            cout<< Map[y] <<endl;
        }
        cout<< "HP : " << hp << "/" << maxhp <<endl;
        for(int y = 0; y < 10; y++)
        {
            for(int x = 0; x <10; x++)
            {

                switch(Map [y] [x])
                {

                	case '#':
                		{
                			Map[y][x] = 219;
						}
                case '@':
                    {

                        if(GetAsyncKeyState(VK_UP) !=0)
                        {
                            int y2 = (y-1);

                            switch(Map[y2][x])
                            {

                            case ' ':
                                {
                                    Map[y][x] = ' ';
                                    y -= 1;
                                    Map[y2][x] = '@';
                                }break;
                            case '!':
                                {
                                    Level = 2;
                                }break;
                                case '?':
                                	{
                                	hp -= 20;
                                	Map[y][x] = ' ';
                                    y -= 1;
                                    Map[y2][x] = '@';
									}break;
                            }
                        }

                        if(GetAsyncKeyState(VK_DOWN) != 0)
                        {
                            int y2=(y+1);

                            switch(Map[y2][x])
                            {
                            case ' ':
                                {
                                    Map[y][x] = ' ';
                                    y += 1;
                                    Map[y2][x] = '@';
                                }break;
                                case '?':
                                	{
                                	hp -= 20;
                                	Map[y][x] = ' ';
                                    y += 1;
                                    Map[y2][x] = '@';
									}break;
                            case '!':
                                {
                                    Level = 2;
                                }break;
                            }
                        }
                        if(GetAsyncKeyState(VK_RIGHT) !=0)
                        {
                            int x2 = (x + 1);

                            switch(Map[y][x2])
                            {
                            case ' ':
                                {
                                    Map[y][x] = ' ';
                                    x += 1;
                                    Map[y][x2] = '@';
                                }break;
                                case '?':
                                	{
                                	hp -= 20;
                                	Map[y][x] = ' ';
                                    x += 1;
                                    Map[y][x2] = '@';
									}break;
                            case '!':
                                {
                                    Level = 2;
                                }break;
                            }
                        }
                        if(GetAsyncKeyState(VK_LEFT) !=0)
                        {
                            int x2 = (x - 1);

                            switch(Map[y][x2])
                            {
                            case ' ':
                                {
                                    Map[y][x] = ' ';
                                    x -= 1;
                                    Map[y][x2] = '@';
                                }break;
                                case '?':
                                	{
                                	hp -= 20;
                                	Map[y][x] = ' ';
                                    x -= 1;
                                    Map[y][x2] = '@';
									}break;
                            case '!':
                                {
                                    Level = 2;
                                }break;
                            }
                        }break;
                    }
                }
            }

            Sleep(gamespeed);
        }
        while(stopgame == false && Level == 2)
        {
            system("cls");
            cout<<"Level 2 belum tersedia ya....\n\n";
            system("pause");
            return EXIT_SUCCESS;
        }
    }
return 0;
}

