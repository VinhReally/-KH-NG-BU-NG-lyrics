#include <iostream>
#include <string>
#include <thread>
#include <chrono>
#include <windows.h>
#include <mmsystem.h>
using namespace std;
void td(string t, int s = 50)
{
	for (char d : t)
	{
		cout << d << flush;
		this_thread::sleep_for(chrono::milliseconds(s));
	}
}
void te(string t, int s = 50)
{
	for (char d : t)
	{
		cout << d << flush;
		this_thread::sleep_for(chrono::milliseconds(s));
	}
	cout << endl;
}
void c(WORD color)
{
	HANDLE hConsole = GetStdHandle(STD_OUTPUT_HANDLE);
	SetConsoleTextAttribute(hConsole, color);
}
int main()
{
	c(14);
	system("start \"\" \"D:\\VisualStudioFile\\source\\repos\\Vinhdepzai\\x64\\Debug\\khongbuong.mp3\"");
	this_thread::sleep_for(chrono::seconds(1));
	te("Gio thi da qua tre roi", 35);
	te("vi phut boc dong...", 100);
	te("Ma doi ta chang the nao canh ben...", 75);
	te("Hoi em con yeu khong?", 75);
	te("em tra loi la: khong con", 75);
	td("Nhung do chi la", 75);
	te(" doi long...", 165);
	return 0; 
}
