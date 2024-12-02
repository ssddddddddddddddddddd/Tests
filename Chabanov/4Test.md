# Ответы на вопросы из 4 теста Чабанова

## Вопросы
1) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(int a){
    std::cout << a;
}

void print(std::string a){
    std::cout << 99;
}

int main()
{
    double i = 0.5;
    print(i);
}
```
Ответ: <code> 0 </code>

2) Дан фрагмент кода на С++. Как инстанцировать данный шаблон?
```cpp
template<typename T>
T foo(T a, T b){
    auto res = a + b;
    return res;
}
```
Ответ: <code> foo<int>(3.0, 0.1415); </code><br>
<code> foo(3, 0); </code><br>
```cpp
foo<double>(3, 0.1415);
```
```cpp
foo<int>(3.0, 0.1415);
```


3) Язык С++. Какой модификатор доступа у <code>some_field</code>?
```cpp
struct SomeClass{
    int some_field;
};
```
Ответ: <code> public </code>

4) Есть ли в языке Go возможность указать параметру значение по умолчанию?<br>

Ответ: <code> Нет </code>

5) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
class Point{
    ~Point(){}
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
Ответ: <code> Ошибка. Не доступен деструктор </code>

6) Есть ли в языке С++ механизм перегрузки функций?<br>

Ответ: <code> Да </code>

7) Дана функция на языке С++. Выберите всё варианты, которые являются допустимым объявлением этой функции:
```cpp
void print(int x, int y=10){
    std::cout << "x: " << x << '\n';
    std::cout << "y: " << y << '\n';
}
```
Ответ: 
```cpp
void print(int, int);
```
```cpp
void print(int x, int y);
```

8) Язык Go. Выберите все ключевые слова которые являются квалификаторами доступа.<br>

Ответ: <code> В Go нет ключевых слов-квалификаторов доступа </code>

9) Есть ли в языке С++ возможность указать параметру значение по умолчанию?<br>

Ответ: <code> Да </code>

10) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(int a){
    std::cout << a;
}

void print(double& a){
    std::cout << 99;
}

int main()
{
    double i = 0.5;
    print(i);
}
```
Ответ: <code> 99 </code>

11) Есть ли в языке Go механизм перегрузки функций?<br>

Ответ: <code> Нет </code>

12) Язык С++. Член класса расположен в секции с модификатором доступа <code>private</code>. Этот член класса:<br>

Ответ: <code> Можно использовать в коде методов класса </code>

13) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(const int  a){
    std::cout << -a;
}

void print(int a){
    std::cout << a;
}

int main()
{
    int i = 10;
    print(i);
}
```
Ответ: <code> Ошибка компиляции </code>

14) Язык С++. Член класса расположен в секции с модификатором доступа protected. Этот член класса:<br>

Ответ: <code> Можно использовать в коде методов класса </code><br>
<code> Можно использовать в коде методов наследников </code>

15) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
template<typename T>
T sum(T a, T b){
    int res = a + b;
    return res;
}

int main()
{
    std::cout << sum(3.0, 0.1415);
}
```
Ответ: <code> 3 </code>

16) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(short a){
    std::cout << a;
}

void print(int a){
    std::cout << 2*a;
}

void print(double a){
    std::cout << 3*a;
}

int main()
{
    int i = 10;
    print(i);
}
```
Ответ: <code> 20 </code>

17) Язык С++. Член класса расположен в секции с модификатором доступа <code>public</code>. Этот член класса:<br>

Ответ: <code> Можно использовать в коде методов наследников </code><br>
<code> Можно использовать в коде методов класса </code><br>
<code> Можно использовать в коде не относящихся к классу функций </code>

18) Код на С++. Требуется запретить доступ к деструктору класса <code>Point</code> из внешнего кода, как это можно сделать?<br>

Ответ: <code> private: ~Point(); </code>

19) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
class Point{
    char i;
public:
    ~Point(char val){}
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
Ответ: <code> Ошибка. У деструктора не может быть параметра </code>

20) Код на С++. Сколько деструкторов может быть у класса?<br>

Ответ: <code> Только 1 </code>

21) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(int a){
    std::cout << -a;
}

void print(double a){
    std::cout << a;
}

void print(bool a);

int main()
{
    bool i = 10;
    print(i);
}
```
Ответ: <code> Ошибка компиляции </code>

22) Язык С++. Какой модификатор доступа у <code>some_field</code>?
```cpp
class SomeClass{
    int some_field;
};
```
Ответ: <code> private </code>

23) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(short a){
    std::cout << a;
}

void print(int a){
    std::cout << 2*a;
}

void print(double a){
    std::cout << 3*a;
}

int main()
{
    float i = 10;
    print(i);
}
```
Ответ: <code> 30 </code>

24) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(int a){
    std::cout << -a;
}

void print(double a){
    std::cout << a;
}

int main()
{
    bool i = 10;
    print(i);
}
```
Ответ: <code> -1 </code>

25) Дан фрагмент кода на С++. Какой прототип соответствует созданной по шаблону функции?
```cpp
template<typename T, typename U>
U sum(T a, U b){
    auto res = a + b;
    return res;
}

int main(){
    auto i = sum(3, 0.1415);
    std::cout << i;
}
```
Ответ:
```cpp
double sum(int a, double b);
```

26) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
template<typename T>
void print(T a){
    std::cout << a;
}

void print(int a){
    std::cout << a;
}

void print(float a){
    std::cout << 99;
}

int main()
{
    double i = 0.5;
    print(i);
}
```
Ответ: <code> 0.5 </code>

27) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
template<typename T>
void print(T a){
    std::cout << "T";
}

template<typename T>
void print(std::vector<T> a){
    std::cout << "vector<T>";
}

int main()
{
    std::vector<std::vector<int> > i;
    print(i);
}
```
Ответ: 
```c
vector<T> 
```

28) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
void print(short a){
    std::cout << a;
}

void print(int a){
    std::cout << 2*a;
}

void print(double a){
    std::cout << 3*a;
}

int main()
{
    unsigned int i = 10;
    print(i);
}
```
Ответ: <code> Ошибка компиляции </code>

29) Выберите все перегрузки функции <code>void print(double a);</code><br>

Ответ:
```cpp
void print(std::vector<double> a);
```
```cpp
void print(double a, int b);
```
```cpp
void print(float a);
```

30) Дана функция на языке С++. Выберите всё варианты, которые являются допустимым объявлением этой функции:
```cpp
void print(int x, int y){
    std::cout << "x: " << x << '\n';
    std::cout << "y: " << y << '\n';
}
```
Ответ:
```cpp
void print(int, int);
```
```cpp
void print(int, int=10);
```
```cpp
void print(int x, int y);
```
```cpp
void print(int x=10, int y=10);
```
```cpp
void print(int x, int y=5);
```
```cpp
void print(int x, int y=10);
```

31) Язык С++. Что из перечисленного может быть использовано в качестве объявления деструктора для класса <code>SomeClass</code>?<br>

Ответ:<code>~SomeClass(){}</code><br>
<code>~SomeClass() = default;</code>

32) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
template<typename T>
T sum(T a, T b){
    auto res = a + b;
    return res;
}

int main()
{
    std::cout << sum(3.0, 0.1415);
}
```
Ответ: <code> 3.1415 </code>
