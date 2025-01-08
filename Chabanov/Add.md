# Ответы на дополнительные вопросы

1) Дана лямбда-функция на языке С++. Какой её тип возвращаемого значения?<br>
```cpp
[](int a, int b){return a > b;};
```
>bool

---

2) Язык С++. Что из нижеперечисленного приведёт к объявлению структуры?<br>

> ```cpp
>struct {
>     int a;
>} s;
>```
> ```cpp
> struct a_struct{
>     int a;
>};
> ```

---

3) Дан фрагмент кода на языке С++. Что выведется на экран в результате его работы?<br>
```cpp
enum Color {
    YELLOW,
    BLACK,
    PINK,
    GREEN
};

Color color = Color::BLACK;
std::cout << color;
```
>1

---

4) Дан фрагмент кода на С++. Что будет содержать переменная container после его выполнения?<br>
```cpp
std::map<int, int> container{{1, 2}, {3, 2}};
container[-1] = 5;
```
>Пары: -1:5, 1:2, 3:2
---

5) Язык Go. Что из нижеперечисленного приведёт к объявлению структуры?<br>

>```cpp
>var Address struct {
>     Name    string
>     City    string
>     Pincode int
>}
>```
>```cpp
>pizza := struct {
>     address string 
>     name string
>     cost int
>}{
>     address: "address",
>     name:    "Pizza",
>     cost:    100,
>}
>```
>```cpp
>type Employee struct {
>     name string
>     age int
>}
>```
>```cpp
>type Mail = struct {
>     Address string
>     Message string
>     Code int
>}
>```


---

6) Дан фрагмент кода на С++. Что будет содержать переменная container после его выполнения?<br>
```cpp
std::set<int> container{1, 2, 3, 4};
container.insert(container.begin(), 4);
```
>1, 2, 3, 4

---

7) Дан фрагмент кода на Go. Что будет содержать переменная container после его выполнения?<br>
```cpp
var container map[int]int
container[-1] = 1
```
>Ошибка во время исполнения - под словарь не выделена память

---

8) Дан фрагмент кода на С++. Что будет содержать переменная container после его выполнения?<br>
```cpp
std::vector<int> container{1, 2, 3, 4};
container.insert(container.begin(), 4);
```
>4, 1, 2, 3, 4

---

9) Дан фрагмент кода на С++ и класс MyClass объявленный как:<br>
```cpp
class MyClass{};
```
Выберите все верные варианты, которые являются допустимыми объявлениям.<br>

>double operator+ (MyClass a, double b);</br>

>double operator+ (double a, MyClass b);</br>

>double operator+ (MyClass a, MyClass b);

---

10) Язык Go. Какие поля могут быть в структурном типе?<br>

>Анонимные поля;</br>

>Не константные поля;

---

11) Дан кода на Go. Что будет выведено на экран в результате его выполнения:<br>
```go
package main
import "fmt"

func change(abc []int) {
    for i := range abc {
        abc[i] = 4
    }
    fmt.Println(abc)
}

func main() {
    abc := []int{1, 2, 3}
    change(abc)
    fmt.Println(abc)
}
```
> [!NOTE]  
> Это один вариант ответа

>[4 4 4]</br>
>[4 4 4]

---

12) Язык С++. Что будет напечатано в результате исполнения следующего кода?<br>
```cpp
#include <iostream>

class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B: public A{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B{
public:
    void get(){
        std::cout << 'C';
    }
};

int main(){
    A* obj = new C;
    obj->get();
}
```
>A

---

13) Язык Go. Дан фрагмент кода:<br>
```go
type A struct{
    value int
}

type Printer interface{
    print()
}

func main() {
    var obj A
    p := Printer(&obj)
    p.print()
}
```
Что нужно добавить, чтобы он стал рабочим?</br>

>```go
>func (a *A) print(){
>     fmt.Print(a.value)
>}

---

14) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?<br>
```cpp
class Point{ 
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
>1

---

15) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?<br>
```cpp
class SomeClass{
public:
    int value = 1;
    void method(int value){
        value = value;
    }
} s;

s.method(5);
std::cout << s.value;
```
>1

---

16) Язык Go. Что будет выведено на экран в результате работы этого кода?<br>
```go
package main
import "fmt"

type Data struct{
    i int
}

func (d Data) method(){
    d.i = 1
}

func main() {
    var d *Data = &Data{}
    d.method()
    fmt.Print(d.i)
}
```
>0

---

16) Язык Go. Что будет выведено на экран в результате работы этого кода?<br>
```go
package main
import "fmt"

type Data struct{
    i int
}

func (d Data) method(){
    d.i = 1
}

func main() {
    var d *Data = &Data{}
    d.method()
    fmt.Print(d.i)
}
```
>0

---

17) Дан фрагмент кода на С++.<br>
```cpp
class SomeClass{
    int value = 0;
public:
    void method() const{
        value = 1;
        std::cout << value;
    }
};

int main(){
    const SomeClass s;
    s.method();
}
```
Что нужно добавить в код, чтобы код стал рабочим?</br>

>Добавить ключевое слово mutable к объявлению value;

---

18) Дан фрагмент кода на С++. Каким образом можно получить доступ к полю x переменной p?<br>
```cpp
struct Point{
    double x, y;
} p;
```
>p.x;

---

19) Дан фрагмент кода на С++. Что будет содержать переменная container после его выполнения?<br>
```cpp
std::map<std::string, int> container{{"1", 2}, {"3", 2}};
container[-1] = 5;
```
>Ошибка компиляции - недопустимый тип

---

20) Дан фрагмент кода на Go. Каким образом можно получить доступ к полю x переменной var p Point = Point{}?<br>
```cpp
type Point struct{
    x float64
    y float64
}
```
>fmt.Print( p.x )</br>

>fmt.Print( (&p).x )</br>

---

20) Дан фрагмент кода на С++. Что будет содержать переменная container после его выполнения?<br>
```cpp
std::unordered_set<int> container{1, 2, 3, 4};
container.insert(container.begin(), 4);
```
>1, 2, 3, 4</br>

---

21) Дан фрагмент кода на С++. Что будет содержать переменная container после его выполнения?<br>
```cpp
std::unordered_set<int> container{1, 2, 3, 4};
container.insert(container.begin(), 4);
```
>1, 2, 3, 4 но в порядке зависящем от хэш-функции</br>

---

22) Дан фрагмент кода на С++. Что будет содержать переменная container2 после его выполнения?<br>
```cpp
std::set<int> container1{4, 3, 2, 1, 2, 3, 4};
std::vector<int> container2(container1.begin(), container1.end());
```
>1, 2, 3, 4</br>

---

23) Дан фрагмент кода на С++ и класс MyClass объявленный как:<br>
```cpp
class MyClass{};
```
Выберите все верные варианты, которые являются допустимыми объявлениям.</br>

>double operator/ (MyClass a, double b);</br>

>double operator+ (MyClass a, double b);</br>

>double operator- (MyClass a, double b);</br>

---

24) Дан фрагмент кода на языке С++. Что выведется на экран в результате его работы?<br>
```cpp
enum class Color {
    YELLOW,
    BLACK,
    PINK,
    GREEN
};

Color color = Color::BLACK;
std::cout << color;
```

>Ошибка. Для Color не определён оператор <<</br>

---

25) Дан кода на Go. Что будет выведено на экран в результате его выполнения:<br>
```go
package main
import "fmt"

func change(abc []int) {
    abc = append(abc, 4)
    for i := range abc {
        abc[i] = 4
    }
    fmt.Println(abc)
}

func main() {
    abc := []int{1, 2, 3}
    change(abc)
    fmt.Println(abc)
}
```

>[4 4 4 4]</br>
>[1 2 3]

---

26) Дан фрагмент кода на Go. Что будет содержать переменная container после его выполнения?<br>
```cpp
var container map[string]int
container[-1] = 1
```
>Ошибка компиляции - недопустимый тип

---

27) Язык С++. Что будет напечатано в результате исполнения следующего кода?<br>
```cpp
#include <iostream>

class A{
public:
    virtual void get(){
        std::cout << 'A';
    }
};

class B: public A{
public:
    void get(){
        std::cout << 'B';
    }
};

class C: public B{
public:
    void get(){
        std::cout << 'C';
    }
};

int main(){
    A* obj = new C;
    obj->get();
}
```

>C

---

28) Язык Go. Дан фрагмент кода:<br>
```go
type A struct{
    value int
}

func (a A) get() int{
    return a.value
}

func (a A) set(val int){
    a.value = val
}

type Accessor interface{
    get() int
    set(val int)
}

func main() {
    var obj A
    g := Accessor(obj)
    g.set(10)
    
    fmt.Print(obj.get())
}
Что будет выведено в результате его работы?</br>
```

>0

---

29) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?<br>
```cpp
class Point{
    Point(){}
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
>Ошибка. Не доступен конструктор по умолчанию

---

30) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?<br>
```cpp
class SomeClass{
    int value = 1;
    void method(int value){
        value = value;
    }
} s;

s.method(5);
std::cout << s.value;
```
>Ошибка

---

31) Язык Go. Что будет выведено на экран в результате работы этого кода?<br>
```cpp
package main
import "fmt"

type Data struct{
    i int
}

func (d *Data) method(){
    d.i = 1
}

func main() {
    var d Data = Data{}
    d.method()
    fmt.Print(d.i)
}
```
>1

---

32) Какое, из перечисленных, ключевых слов нужно использовать при объявлении структуры в С++?<br>

>struct

---

> [!NOTE]  
> Скорее всего он имел в виду C++
33) Дан код на языке Go:<br>
```cpp
#include <iostream>
#include <map>

void add(std::map<int, int> c, int value){
    c[c.size()] = value;
}

int main(){
    std::map<int, int> container;
    add(container, 10);
    std::cout << container.size();
}
```
В результате его исполнения:</br>
>Переменная container не изменится;

---

34) Дан фрагмент кода на Go. Каким образом можно получить доступ к полю x переменной var p *Point = &Point{}?<br>
```go
type Point struct{
    x float64
    y float64
}
```
>fmt.Print( (*p).x )

>fmt.Print( p.x )

---

35) Дан фрагмент кода на С++. Что будет содержать переменная container2 после его выполнения?<br>
```cpp
std::vector<int> container1{4, 3, 2, 1, 2, 3, 4};
std::set<int> container2(container1.begin(), container1.end());
```
>1, 2, 3, 4

---

36) Дан фрагмент кода на С++. Что будет содержать переменная container2 после его выполнения?<br>
```cpp
std::vector<int> container1{4, 3, 2, 1, 2, 3, 4};
std::vector<int> container2(container1.begin(), container1.end());
```
>4, 3, 2, 1, 2, 3, 4

---

37) Дан фрагмент кода на С++ и класс MyClass объявленный как:<br>
```cpp
class MyClass{};
```
Выберите все верные варианты, которые являются допустимыми объявлениям.<br>

>void operator/ (MyClass a, double b);

>double operator/ (MyClass a, double b);

---

38) Дан фрагмент кода на языке С++. Что выведется на экран в результате его работы?<br>
```cpp
enum Color {
    YELLOW,
    BLACK,
    PINK,
    GREEN
};

int BLACK = 0;
Color color = Color::BLACK;
std::cout << color;
```
Выберите все верные варианты, которые являются допустимыми объявлениям.<br>

>Ошибка. Повторное объявление имени BLACK

---

39) Дан кода на Go. Что будет выведено на экран в результате его выполнения:<br>
```go
package main
import "fmt"

func change(abc []int) {
    abc = append(abc, 4)
    for i := range abc {
        abc[i] = 4
    }
    fmt.Println(abc)
}

func main() {
    abc := []int{1, 2, 3}
    change(abc)
    abc = append(abc, 4)
    fmt.Println(abc)
}
```
>[4 4 4 4]<br>
>[1 2 3 4]

---

40) Дан фрагмент кода на Go. Что будет содержать переменная container после его выполнения?<br>
```go
var container map[int]int = make(map[int]int)
container[-1] = 1
```
>Ключ: -1 со значением: 1

---

41) Язык С++. Что будет напечатано в результате исполнения следующего кода?<br>
```cpp
#include <iostream>

class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B: public A{
public:
    virtual void get(){
        std::cout << 'B';
    }
};

class C: public B{
public:
    virtual void get(){
        std::cout << 'C';
    }
};

int main(){
    A* obj = new C;
    obj->get();
}
```
>A

---

42) Язык Go. Дан фрагмент кода:<br>
```go
type A struct{
    value int
}

func (a *A) get() int{
    return a.value
}

func (a *A) set(val int){
    a.value = val
}

type Accessor interface{
    get() int
    set(val int)
}

func main() {
    var obj A
    g := Accessor(&obj)
    g.set(10)
    
    fmt.Print(obj.get())
}
```
>10

---

43) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?<br>
```cpp
class Point{
    char i;
public:
    Point(char val):i(val){}
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
>Ошибка. Отсутствует конструктор по умолчанию

---

44) Дан фрагмент кода на языке С++. Что будет на экране в результате выполнения данного фрагмента?<br>
```cpp
class SomeClass{
public:
    int value = 1;
    void method(int value){
        this->value = value;
    }
} s;

s.method(5);
std::cout << s.value;
```
>5

---

45) Язык Go. Что будет выведено на экран в результате работы этого кода?<br>
```go
package main
import "fmt"

type Data struct{
    i int
}

func (d *Data) method(){
    d.i = 1
}

func (d Data) method(){
    d.i = 1
}

func main() {
    var d *Data = &Data{}
    d.method()
    fmt.Print(d.i)
}
```
>Ошибка

---

46) Где можно объявить структуру в языке С++?<br>

>Внутри тела функции;

>Внутри других структур;

>Вне функции;

---

47) Дан фрагмент кода на С++. Что будет содержать переменная container после его выполнения?<br>
```cpp
std::map<int, int> container;
int a = container[-1];
```
>Ключ: -1 со значением: 0

---

48) Дан фрагмент кода на С++. Что будет содержать переменная container2 после его выполнения?<br>
```cpp
std::vector<int> container1{4, 3, 2, 1, 2, 3, 4};
std::unordered_set<int> container2(container1.begin(), container1.end());
```
>1, 2, 3, 4 но в порядке зависящем от хэш-функции
---

49) Какое, из перечисленных, ключевых слов нужно использовать при объявлении структуры в Go?<br>

>struct

---

50) Дан фрагмент кода на С++. Что будет содержать переменная container после его выполнения?<br>
```cpp
std::vector<int> container{1, 2, 3, 2};
container[-1] = 5;
```
>Ошибка доступа - указанного элемента не существует

---

51) Дан фрагмент кода на языке С++. Что выведется на экран в результате его работы?<br>
```cpp
enum Color {
    YELLOW,
    BLACK = 0,
    PINK,
    GREEN
};

Color color = Color::BLACK;
std::cout << color;
```
>0

---

52) Дан кода на Go. Что будет выведено на экран в результате его выполнения:<br>
```go
package main
import "fmt"

func change(abc []int) {
    abc = append(abc, 4)
    for i := range abc {
        abc[i] = 4
    }
    fmt.Println(abc)
}

func main() {
    abc := []int{1, 2, 3}
    abc = append(abc, 4)
    change(abc)
    fmt.Println(abc)
}
```
>[4 4 4 4 4]<br>
>[4 4 4 4]

---

53) Дан код на языке Go:<br>
```go
package main
import "fmt"

func add(c map[int]int, value int){
    c[len(c)] = value
}

func main() {
    var container map[int]int = make(map[int]int)
    add(container, 10)
    fmt.Print(len(container))
}
```
В результате его исполнения:<br>
>Переменная container изменится;

---

54) Язык С++. Что будет напечатано в результате исполнения следующего кода?<br>
```go
#include <iostream>

class A{
public:
    void get(){
        std::cout << 'A';
    }
};

class B: public A{
public:
    virtual void get(){
        std::cout << 'B';
    }
};

class C: public B{
public:
    virtual void get(){
        std::cout << 'C';
    }
};

int main(){
    C* obj = new A;
    obj->get();
}
```
>Ошибка

---

55) Язык Go. Дан фрагмент кода:<br>
```go
type A struct{
    value int
}

func (a *A) print(){
    fmt.Print("*")
}

type Printer interface{
    print()
}

func main() {
    var obj *A = nil
    p := Printer(obj)
    
    if p == nil{
        fmt.Print("+")
    } else {
        fmt.Print("-")
    }
}
```
Что будет выведено в результате его работы?<br>

>&nbsp;-

---

56) Дан фрагмент кода на С++:<br>
```cpp
class MyClass{
public:
    double i = 1.0;
};

double operator+ (MyClass a, double b){
    return a.i + b;
}

MyClass obj;
double value = 2.0;
```
Выберите все выражения, которые НЕ вызовут ошибки:<br>

>obj + value;

>value + value;

>obj + 2.0;

---

57) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?<br>
```cpp
class Point{
    char i;
public:
    Point(char val=0):i(val){}
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
>1

---

58) Язык С++. Дан класс:<br>
```cpp
class SomeClass{
    int value = 0;
public:
    void one(){
        value = 1;
    }
    void one() const{
        std::cout << value;
    }
    
    void two(){
        value = 2;
    }
    
    void three() const {
        std::cout << 3;
    }
    
    void four() {
        std::cout << 4;
    }
};
```
и переменная созданная таким образом:
```cpp
const SomeClass s;
```
Какие из перечисленных вызовов метода НЕ приведут к ошибке?<br>

>s.one();

>s.three();

---

59) Каким образом можно создать переменную типа структура в языке С++?<br>

>```cpp
>struct Point{
>     int x,y;
>} p1, p2;
>```
>```cpp
>struct Point{
>     int x,y;
>};
>
>Point p1, p2;
>```
>```cpp
>struct{
>     int x,y;
>} p1, p2;
>```

---

60) Дан фрагмент кода на языке С++. Что выведется на экран в результате его работы?<br>
```cpp
enum Color {
    YELLOW = 1,
    BLACK = 1,
    PINK,
    GREEN
};

Color color = Color::BLACK;
std::cout << color;
```
>1

---

61) Язык Go. В текущий пакет из пакета other была импортирована структура:<br>
```go
type Book struct {
    Title       string
    author      string
    Description string
    Price       int
    pages       int
}
```
Какие поля будут доступны для использования в текущем пакете?<br>

>Title

>Price

>Description

---

62) Дан фрагмент кода на Go. Что будет содержать переменная container после его выполнения?<br>
```go
var container map[int]int = make(map[int]int)
var a = container[-1]
```
>Ключ: -1 со значением: 0

---

63) Язык С++. Что будет напечатано в результате исполнения следующего кода?<br>
```cpp
#include <iostream>

class A{
    char value = 'a';
public:
    virtual void get(){
        std::cout << value;
    }
};

class B: public A{
    char value = 'b';
public:
    virtual void get(){
        std::cout << value;
    }
};

void print(A* obj){
    obj->get();
}

int main(){
    print(new B);
}
```
>b

---

64) Дан фрагмент кода на С++:
```cpp
struct MyClass{
    double i = 1.0;
};

double operator+ (double a, MyClass b){
    return a + b.i;
}

MyClass obj;
double value = 2.0;
```
Выберите все выражения, которые НЕ вызовут ошибки:<br>

>value + value;

>value + obj;

---

65) Дан фрагмент кода на С++. Что отобразится на экране после его выполнения?
```cpp
class Point{
    char i;
public:
    Point():i(0){}
    Point(char val=0):i(val){}
};
 
int main(){
    Point p;
    std::cout << sizeof(p);
}
```
>Ошибка. Двусмысленность при вызове конструктора

---

66) Язык С++. Дан класс:
```cpp
class SomeClass{
    int non_static_value = 0;
    static const int static_value = 0;
public:
    static void static_method() {
    }
    static void other_static_method() {
    }    

    void non_static_method() {
    }
    void other_non_static_method() {
    }
};
```
>В static_method можно использовать other_static_method;

>Чтобы вызвать static_method НЕ обязательно иметь объект;

>В static_method можно использовать static_value;

---

67) Язык С++. Что будет напечатано в результате исполнения следующего кода?
```cpp
#include <iostream>

class A{
    char value = 'a';
public:
    void get(){
        std::cout << value;
    }
};

class B: public A{
    char value = 'b';
public:
    void get(){
        std::cout << value;
    }
};

void print(A* obj){
    obj->get();
}

int main(){
    print(new B);
}
```
>a

---

68) Язык С++. Дан класс:
```cpp
class SomeClass{
    int non_static_value = 0;
    static const int static_value = 0;
public:
    static void static_method() {
    }
    static void other_static_method() {
    }    

    void non_static_method() {
    }
    void other_non_static_method() {
    }
};
```
>Чтобы вызвать non_static_method обязательно нужно создать объект;

>В non_static_method можно использовать non_static_value;

>В non_static_method можно использовать static_value;

>В non_static_method можно использовать static_method;

>В non_static_method можно использовать other_non_static_method;

---

69) Язык С++. Дана структура:
```cpp
struct Point{
    int x,y;
};
```
Каким образом можно создать переменную типа Point?<br>

>Point p {1, 2};

>Point p = {1, 1};

>Point p = {};

---

70) Язык С++. Что из перечисленного может быть использовано в качестве объявления конструктора по умолчанию для класса SomeClass?

>SomeClass() = default;

>SomeClass(){}

>SomeClass(int a=0, int b=0){}

---

71) Дан фрагмент кода на языке С++. Что выведется на экран в результате его работы?
```cpp
enum Color {
    YELLOW = -2,
    BLACK,
    PINK = -1,
    GREEN = 0
};

Color color = Color::BLACK;
std::cout << color;
```
>-1

---

72) Язык Go. Структуры A, B и С и переменные a, b, c объявлены следующим образом:
```go
type A struct {
    Title       string
    Author      string
}

type B struct {
    Title       string
    Author      string
}

type C = struct {
    Title       string
    Author      string
}
    
a := A{}
b := B{}
c := C{}
```
Выберите все допустимые выражения.<br>

>a = c

>b = c

>c = b

>c = a

---

73) Дан фрагмент кода на С++:
```cpp
class MyClass{
    double i = 1.0;
    friend double operator+ (MyClass a, double b);
};

double operator+ (MyClass a, double b){
    return a.i + b;
}

MyClass obj;
double value = 2.0;
```
Выберите все выражения, которые НЕ вызовут ошибки:<br>

>obj + value;

>value + value;

>obj + 2.0;

---

74) Язык С++. Что из нижеперечисленного может быть полем структуры?

>Массивы;

>Структуры и Классы;

>Фундаментальные типы (int, double, ...);

>Строки;

>Указатели;

---

75) Дан фрагмент кода на языке С++. Выберите верные утверждения.
```cpp
enum Color {
    YELLOW = -2,
    BLACK,
    PINK = -2,
    GREEN
};
```

>BLACK равно -1

>GREEN равно -1

76) Язык Go. Какая структура называется анонимной?<br>

>```go
>var a struct {
>    Title     string
>    Author    string
>}
>```

---

77) Язык С++. Для чего используется ключевое слово override?

>Это ключевое слово НЕ обязательно использовать. Оно заставляет компилятор проверить, что у предка существует такой же метод как текущий и что он виртуальный. Если это не так, будет ошибка компиляции;

---

78) Дан фрагмент кода на С++. Каким образом можно создать один или несколько объектов класса Point?
```cpp
struct Point{
    Point(){}
};
```

>new Point();

>Point p[10];

>class Point p;

>Point p;

>new Point;

---

79) Дан фрагмент кода на С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class MyClass{
public:
    double i = 1.0;
};

MyClass obj;
if (obj) std::cout << 1;
else std::cout << 2;
```

>Ошибка

80) Язык С++. Дана структура:
```cpp
struct Point{
    int x,y;
};
```
Выберите фрагменты не вызывающие ошибки.<br>

>```cpp
>Point p = {1, 1}, p2;
>p2 = p;
>```
>```cpp
>Point p = {1, 1}, p2 = {2, 2};
>p2.x = p2.x + p.x;
>p2.y = p2.y + p.y;
>```
>```cpp
>Point p;
>p = {1, 1};
>```
>```cpp
>Point p = {1, 1}, p2;
>p2 = {p.y, p.x};
>```


---

81) Дан фрагмент кода на языке С++. Выберите верные утверждения.
```cpp
enum Color {
    YELLOW = -1,
    BLACK = 0,
    PINK = 1,
    GREEN = 2
};
```
>Color mix = Color(YELLOW + PINK); // mix будет равно BLACK

>int i = YELLOW + PINK; // i будет равно 0

---

82) Код на С++. Требуется запретить доступ к конструктору класса Point из внешнего кода, как это можно сделать?

>private: Point();


---

83) Язык Go. Дан тип данных и функция:
```cpp
type Point struct {
    x, y int
}

func foo(p Point){
    p.x = 10
    p.y = 10
}
```
>Внутри функции будет доступна копия структуры;

---

84) Дан фрагмент кода на С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class MyClass{
public:
    double i = 1.0;
    operator bool(){
        return i > 1.0;
    }
};

MyClass obj;
if (obj) std::cout << 1;
else std::cout << 2;
```
>2

---

85) Язык С++. Какая структура называется анонимной?<br>

>```cpp
>struct {
>     int x,y;
>} s;
>```
---

86) Дан фрагмент кода на языке С++. Выберите верные утверждения.
```cpp
enum class Color {
    YELLOW = -1,
    BLACK = 0,
    PINK = 1,
    GREEN = 2
};
```
>Во всех остальных вариантах будет ошибка, т.к. для Color не определены операторы + и/или =
---

87) Код на С++. Сколько конструкторов может быть у класса?
>Сколько угодно
---

88) Дан фрагмент кода на С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class MyClass{
public:
    double i = 1.0;
    void operator*(double b){
        i * b;
    }
};

MyClass obj;
std::cout << obj * 1.0;
```
>Ошибка
---

89) Язык С++. Дан тип данных и прототип функции:
```cpp
struct Point{
    int x,y;
};

void foo(Point p);
```
Если передать переменную типа Point в функцию foo указанным выше образом, то:<br>

>Внутри функции будет доступна копия структуры;
---

90) Язык С++. Что из перечисленного является правильным объявлением и определением класса?<br>

>class SomeClass{};

>struct SomeClass{};

---

91) Дан фрагмент кода на языке С++:
```cpp
enum class Color {
    YELLOW = 0,
    BLACK = 1,
    PINK = 2
};
Color color = Color::BLACK;
```
и функция с представленным ниже прототипом:
```cpp
void foo(Color clr);
```
Какой вариант вызова функции НЕ приведёт к ошибке?<br>

>foo(color);

>foo(Color::YELLOW);

>foo(Color(1));

---

92) Дан фрагмент кода на С++. Что будет на экране в результате выполнения данного фрагмента?
```cpp
class MyClass{
public:
    double i = 1.0;
    double operator*(double b){
        return i * b;
    }
};

MyClass obj;
std::cout << obj * 1.0;
```

>1
---

93) Дан фрагмент кода на языке С++:
```cpp
struct One{
    int x,y;
} a;

struct Two{
    int x,y;
} b;
```
Допустим ли следующий код?
```cpp
a = {1, 2};
b = a;
```

>Нет, т.к. у a и b разные типы;

---

94) Язык С++. Где можно объявить/определить новый класс?<br>

>В глобальной области видимости

>Внутри конструкции блок {}

>В теле функции

>Внутри других классов

---

95) Дан фрагмент кода на языке С++:
```cpp
enum Color {
    YELLOW = 0,
    BLACK = 1,
    PINK = 2
};
Color color = Color::BLACK;
```
и функция с представленным ниже прототипом:
```cpp
void foo(Color clr);
```
Какой вариант вызова функции НЕ приведёт к ошибке?<br>

>foo(color);

>foo(Color::YELLOW);

>foo(Color(1));

>foo(YELLOW);
---

96) Дан фрагмент кода на языке С++:
```cpp
struct One{
    int x,y;
} a, b;
```
Допустим ли следующий код?
```cpp
a = {1, 2};
b = a;
```
>Да, b получит копию полей a;

---

97) Язык С++. Дано перечисление. Выберите все способы получения значения со стандартного ввода.
```cpp
enum Color {
    YELLOW = 0,
    BLACK = 1,
    PINK = 2
} color;
```
>```cpp
>int i;
>std::cin >> i; // Пользователь вводит число: 0
>color = static_cast<Color>(i);
>```
>```cpp
>int i;
>std::cin >> i; // Пользователь вводит число: 0
>color = Color(i);
>```


---

98) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    int i = 0;
    int j = 0;
    
    SomeClass(){
        i = 10;
    }
    
    SomeClass(int value):SomeClass(){
        j = value;
    }
};

SomeClass obj(10);
std::cout << obj.i << ' ' << obj.j;
```

>10 10

---

99) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    int i = 0;
    int j = 0;
    
    SomeClass(){
        i = 10;    
    }
    
    SomeClass(int value){
        SomeClass();
        j = value;
    }
};

SomeClass obj(10);
std::cout << obj.i << ' ' << obj.j;
```
>0 10

---

100) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    int i = 0;
    
    SomeClass(int i){
        i = i;
    }
};

SomeClass obj(10);
std::cout << obj.i;
```
>0

---

101) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    int i = 0;
    
    SomeClass(int i){
        this->i = i;
    }
};

SomeClass obj(10);
std::cout << obj.i;
```
>10

---

102) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    int i = 0;
    
    SomeClass(int i):i(i){
    }
};

SomeClass obj(10);
std::cout << obj.i;
```
>10

---

103) Язык С++. От чего зависит порядок инициализации полей класса, указанных в списке инициализаторов?<br>

>От того, в каком порядке эти поля объявлены

---

104) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    const int i = 0;
    
    SomeClass(int i):i(i){
    }
};

SomeClass obj(10);
cout << obj.i;
```
>10


---

105) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    const int i = 0;
    
    SomeClass(int i){
        this->i = i;
    }
};

SomeClass obj(10);
std::cout << obj.i;
```
>Ошибка

---

106) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    int& i;
    
    SomeClass(int& i):i(i){
    }
};

int i = 0;
SomeClass obj(i);
std::cout << obj.i;
```
>0

---

107) Дан фрагмент кода на языке С++. Что будет напечатано в результате его выполнения?
```cpp
struct SomeClass{
    int& i;
    
    SomeClass(int& i){
        this->i = i;
    }
};

int i = 0;
SomeClass obj(i);
std::cout << obj.i;
```
>Ошибка
