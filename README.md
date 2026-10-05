#include<bits/stdc++.h>
using namespace std;

class Book
{
public:
    string title, author;
    double price;
    double calculate(Book b)
    {
        return b.price;
    }
    double calculate(Book b1, Book b2)
    {
        return b1.price + b2.price;
    }
    double calculate(Book book[], int n)
    {
        double total = 0;

        for(int i = 0; i < n; i++)
        {
            total += book[i].price;
        }

        return total;
    }

    void display()
    {
        cout << "Title: " << title << endl<< "Author: " << author << endl
             << "Price: " << price << endl;
    }
};

int main()
{
    Book ob[5];

    ob[0].title = "C++";
    ob[0].author = "aa";
    ob[0].price = 500;

    ob[1].title = "Java";
    ob[1].author = "ss";
    ob[1].price = 600;

    ob[2].title = "ef";
    ob[2].author = "oo";
    ob[2].price = 450;

    ob[3].title = "Data";
    ob[3].author = "ppp";
    ob[3].price = 700;

    ob[4].title = "amaa";
    ob[4].author = "pp";
    ob[4].price = 800;
    for(int i = 0; i < 5; i++)
    {
        ob[i].display();
    }
    cout << "Price one: "<< ob[0].calculate(ob[0]) << endl;
    cout << "Price two: "<< ob[0].calculate(ob[0], ob[1]) << endl;
    cout << "Total all books: "<< ob[0].calculate(ob, 5) << endl;

    return 0;
}
