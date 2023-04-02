/*
Шестое задание
Создайте приложение «Каталог текстов песен».
Приложение должно иметь следующие возможности:
■ Добавление текста песни:
• Текст песни:
ӽ может быть введен с клавиатуры;
ӽ загружен из файла.
• Для каждой песни нужно указывать название песни, автора текста и
год создания песни (если он известен).
■ Удаление текста песни.
■ Изменение текста песни.
■ Отображение текста песни на экран.
■ Сохранение текста песни в файл.
■ Поиск и отображение всех песен одного автора.
■ Поиск и отображение всех песен, содержащих слово, указанное пользователем
*/

#define _CRT_SECURE_NO_WARNINGS 

#include <iostream>
#include <fstream>
#include <windows.h> 
#include<string>
using namespace std;

struct music {
    string name;
    string avtor;
    string god;
    string text;
};




void vvod (int kol, music * mass) //вопросы!!!!
{
       kol++;

       muz* mass2 = new muz[kol];

       for (int u = 0; u < kol - 1; u++) {
           mass2[u].name = mass[u].name;
           mass2[u].avtor = mass[u].avtor;
           mass2[u].god = mass[u].god;
           mass2[u].text = mass[u].text;
       }

       cout << "vvedite nazvanie: " << endl;
    cin >> mass2[kol - 1].name;
    cout << endl;
    cout << "vvedite avtora:" << endl;
    cin >> mass2[kol - 1].avtor;
    cout << endl;
    cout << "vvedite god vipuska: " << endl;
    cin >> mass2[kol - 1].god;
    cout << endl;
    for (;;) {
        cout << "vi xotite vvesti text s klaviaturi(1) ili vzyat ego iz faila(2) ? " << endl;
        cin >> qu;
        if (qu == 1) {
            cout << "vvedite text" << endl;
            cin >> mass2[kol - 1].text;
            cout << endl;
            break;
        }
        else if (qu == 2) {

            string strokk;
            ifstream openfile("koroll.txt");
            if (openfile.is_open())
            {
                while (getline(openfile, strokk))
                {
                    openfile >> strokk;
                    mass2[kol - 1].text = strokk ;
                }
            }

            break;
        }
        else {
            cout << " vi nepravilno vveli chislo..poprobuite eche raz)" << endl;
        }
    }

    delete[]  mass;

    mass = mass2;
}




void izmenu (int kol, music * mass)  //вопросы!!!!!
{
    int ox;
    for (;;) {
        cout << "vvedite kakuyu po chety pesnu vi xotite izmenit - " << endl;
        cin >> ox;
        if (ox > kol) {
            cout <<endl<< "vi nepravilno vveli chislo.. povtorite eche raz))" << endl;
        }
        else if (ox < kol) {
            cout <<endl<< "vi nepravilno vveli chislo.. povtorite eche raz))" << endl;
        }
        else {
            int ha;
            cout << endl << "vi xotite vvesti text s klaviaturi(1) ili vzuat ego iz faila(2)?" << endl;
            if (ha == 1) {
                cout << "vvedite novui text pesni - " << endl;
                cin >> mass[ox].name;
                break;
            }
            else if (ha == 2) {
                string strokk;
                ifstream openfile("koroll.txt");
                if (openfile.is_open())
                {
                    while (getline(openfile, strokk))
                    {
                        openfile >> strokk;
                        mass[ox].text = strokk;
                    }
                }
                break;
            }
            else {
                cout << "vi nepravilno vveli choslo.. poprobuite eche raz))" << endl;
            }
        }
    }
}





void udalenie(int kol, music* mass)  //вопросы..!
{
    int lol;
    int ho;
    for (;;) {
        cout << "vvedite nomer dela, kotoroe nado ydalit - ";
        cin >> ho;
        if (ho > kol) {
            cout << endl << "vi nepravilno vveli nomer, poprobuite eshe raz))" << endl;
        }
        else if (ho < kol) {
            cout << endl << "vi nepravilno vveli nomer, poprobuite eshe raz))" << endl;
        }
        else {
            break;
        }
    }

    for (;;) {
    cout << "if ti yveren - vvedi 1, esli oshibsya - vvedi 2 :  ";
    cin >> lol;
    
        if (lol == 1) {
            delete[] mass[ho];
            break;
        }
    

        else if (lol == 2) {
            cout << endl << "okay !" << endl;
            break;
        }
        else {
            cout << "vi oshiblis, vvedite eshe raz))" << endl;
        }
    }
}



void poiskavt (int kol, music* mass)
{           
    string cool;
    cout << "POISK" << endl;
    for (;;) {
        cout << "what avtor do you want to listen?" << endl;
        cin >> cool;
            for (int i = 0; i < kol; i++) {
                if (mass[i].avtor == cool) {
                    cout << endl << mass[i].name;
                    cout << endl << mass[i].avtor;
                    cout << endl << mass[i].god;
                    cout << endl << mass[i].text;
                }
                else {
                    cout << "net takogo avtora !!! " << endl;
                }
            }
        }
    }
}
void poiskslov(int kol, music* mass) {
    string fifa;
    cout << endl << "vvedite slovo" << endl;
    cin >> fifa;
    for (int kok = 0; kok < kol; kok++) {
        for (int l = 0; l < len(mass[kok].text); l++) {
            int yuu = mass[l].text.find(fifa) << endl;
            if (yuu > 0) {
                cout << mass[l].name << endl;
                cout << mass[l].avtor << endl;
                cout << mass[l].god << endl;
                cout << mass[l].text << endl;
            }
        }
    }
}


void pokazpes(int kol, music* mass)
{
    cout << "-VSE PESNI-";
    for (int i = 0; i < kol; i++) {
        cout << mass[i].name << endl;
        cout << mass[i].avtor << endl;
        cout << mass[i].god << endl;
        cout << mass[i].text << endl;
    }
}


void soxrr(int kol, music* mass) {
    for (;;) {
        int gg;
        cout << endl << "vvedite nomer faila,  kotorui xotite soxranit" << endl;
        cin >> gg;
        if (gg > kol or gg < kol) {
            cout << endl << "vi nepravilno napisali chislo.. poprobuite eche raz))" << endl;
        }
        else {
            FILE* myfile;
            myfile = fopen("pupupu.txt", "r+");
            if (myfile == NULL) {
                cout << "error emae!";
            }
            else {
                string str;
                cout << " you cool!";
                getline(cin, mass[gg].text);
                ofstream fout("pupupu.txt"); // создаём объект класса ofstream для записи и связываем его с файлом cppstudio.txt
                fout << str; // запись строки в файл
                //fout.close(); // закрываем файл		
            }

            int m = fclose(myfile);

            if (m == EOF)
                cout << endl << "The file is not closed";
            else
                cout << endl << "The file is closed";

            break;
        }
    }

}

int main()
{
    int kol = 1;
    music* mass = new music[kol];

    for (int y = 0; y < kol; y++) {
        cout << "enter nazvanie pesni - ";
        cin >> mass[y].name;
        cout << endl;
        cout << "enter avtora - ";
        cin >> mass[y].avtor;
        cout << endl;
        cout << "enter god sozdania  - ";
        cin >> mass[y].god;
        cout << endl;

        //либо с клавиатуры, либо с файла
        cout << "enter text pesni - ";
        cin >> mass[y].text;
        cout << endl;
    }


    



    int vib;
    for (;;) {
        cout << "---MENU---";
        cout << "1 - dobavit pesnu" << endl;
        cout << "2 - ydalit pesnu" << endl;
        cout << "3 - redactirovat text pesni" << endl;
        cout << "4 - pokaz texta pesni" << endl;
        cout << "5 - soxranenie v fail" << endl;
        cout << "6 - poisk pesen po avtoru" << endl;
        cout << "7 - poisk pesen po slovu" << endl;
        cout << "8 - vixod" << endl;
        cin >> vib;

        if (vib == 1) {
            vvod(kol, mass);
        }
        else if (vib == 2) {
            udalenie(kol, mass);
        }
        else if (vib == 3) {
            izmenu(kol, mass);
        }
        else if (vib == 4) {
            pokazpes(kol, mass);
        }
        else if (vib == 5) {
            soxrr(kol, mass) {

        }
        else if (vib == 6) {
            poiskavt(kol, mass);
        }
        else if (vib == 7) {
            poiskslov(kol, mass);
        }
        else if (vib == 8) {
            break;
        }
        else {
            cout << "vi nepravilno vveli chislo.. povtorite eche raz !" << endl;
        }
    }
}
 
