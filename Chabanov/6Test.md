# Ответы на вопросы из 6 теста Чабанова

## Вопросы
1) Язык Go. Пакет импортирован следующим образом:&nbsp;<br>
<code>import . "github.com/vigo5190/example/name"</code><br>
Каким образом можно использовать экспортируемые имена из этого пакета в своём коде?<br>

> Ответ: <code>Имена объявленные в пакете name доступны для использования просто по своему имени</code>

2) Язык Go. Пакет импортирован следующим образом:&nbsp;<br>
<code>import _ "github.com/vigo5190/example/name"</code><br>
Каким образом можно использовать экспортируемые имена из этого пакета в своём коде?<br>

> Ответ: <code>Имена объявленные в пакете name НЕ доступны для использования</code>

3) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace C{
    int i = 2;
}

namespace A {
    namespace B {
        using namespace C;
        void print() {
            std::cout << i;
        }
    }
    int i = 3;
}

int main() {
    A::B::print();
}
```
> Ответ: <code>Ошибка</code>

4) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main(){
    bool i = true;
    {
        int i = 5;
        i = !i;
    }
    std::cout << i;
}
```
> Ответ: <code>1</code>

5) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main() {
    int i = 1;
    int i = 1;
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

6) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace {
    int i = 1;
}

int main() {
    std::cout << i;
}
```
> Ответ: <code>1</code>

7) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int i = 2;

int main() {
    using namespace A;
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

8) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
inline namespace A{
    int i = 1;
}

int main() {
    std::cout << i;
    int i = 2;
}
```
> Ответ: <code>1</code>

9) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    A::B::print();
}
```
> Ответ: <code>1</code>

10) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
        int i = 2;
    }
}

int main() {
    int i = 3;
    A::B::print();
}
```
> Ответ: <code>1</code>

11) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    int i = 1;
    A::B::print();
}
```
> Ответ: <code>Ошибка</code>

12) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace {
    int i = 1;
}

int i = 2;

int main() {
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

13) Язык Go. Пакет импортирован следующим образом:&nbsp;<br>
<code>import "github.com/vigo5190/example/name"</code><br>
Каким образом можно использовать экспортируемые имена из этого пакета в своём коде?<br>

> Ответ: <code>Имя из пакета name можно использовать так: name.требуемое_имя</code>

14) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int A = 1;

int A(){
    return 2;
}

int main() {
    std::cout << A();
}
```
> Ответ: <code>Ошибка</code>

15) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    int i = 2;
    std::cout << i;
}
```
> Ответ: <code>2</code>

16) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
    }
}

int i = 1;

int main() {
    A::B::print();
}
```
> Ответ: <code>Ошибка</code>

17) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    std::cout << i;
    int i = 2;
}
```
> Ответ: <code>Ошибка</code>

18) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int i = 2;

int main() {
    using A::i;
    std::cout << i;
}
```
> Ответ: <code>1</code>

19) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace D{
    int i = 1;
}

namespace C{
    using namespace D;
    int i = 2;
}

namespace A {
    namespace B {
        using namespace C;
        void print() {
            std::cout << i;
        }
    }
    int i = 3;
}

int main() {
    A::B::print();
}
```
> Ответ: <code>Ошибка</code>

20) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;
int main() {
    int i = 1;
    std::cout << i;
}
```
> Ответ: <code>1</code>

21) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using A::i;
    std::cout << i;
    int i = 2;
}
```
> Ответ: <code>Ошибка</code>

22) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace A {
    namespace B {
        int i = 2;
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    int i = 3;
    A::B::print();
}
```
> Ответ: <code>2</code>

23) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace C{
    int i = 2;
}

namespace A {
    int i = 3;
    namespace B {
        using namespace C;
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    A::B::print();
}
```
> Ответ: <code>3</code>

24) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main(){
    const int i = 1;
    {
        int i = i;
        std::cout << i;
    }
}
```
> Ответ: <code>Мусор. Т.к. i неинициализированная переменная</code>

25) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main() {
    std::cout << i;
}

int i = 1;
```
> Ответ: <code>Ошибка</code>

26) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int A(){
    int i = 1;
}

int main() {
    int i = 2;
    std::cout << A::i;
}
```
> Ответ: <code>Ошибка</code>

27) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main() {
    const int i = 1;
    {
        int i[i] = {};
    }
    std::cout << i;
}
```
> Ответ: <code>1</code>

28) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int i = 2;

int main() {    
    std::cout << i;
}
```
> Ответ: <code>2</code>

29) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

int main() {
    std::cout << i;
    int i = 2;
    {
        std::cout << i;
        int i = 3;
    }
    std::cout << i;
}
```
> Ответ: <code>122</code>

30) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int i = 2;

int main() {
    int i = 3;
    {
      using namespace A;      
      std::cout << i;
    }
}
```
> Ответ: <code>3</code>

31) Дан кода на Go. Что будет напечатано в результате его выполнения?
```cpp
package main
import "fmt"

func main() {
    fmt.Print(i)
}

var i int = 1
```
> Ответ: <code>1</code>

32) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
inline namespace A{
    int i = 1;
}

int i = 2;

int main() {
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

33) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using A::i;
    int i = 2;
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>

34) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
void A(){
    std::cout << i;  
}

int i = 1;

int main() {
    A();
}
```
> Ответ: <code>Ошибка</code>

35) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using namespace A;
    std::cout << i;
    int i = 2;
}
```
> Ответ: <code>1</code>

36) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int main(){
    bool i = true;
    {
        int i = 5;
        i = !i;
        std::cout << i;
    }
}
```
> Ответ: <code>0</code>

37) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace D{
    int i = 1;
}

namespace C{
    using namespace D;
}

namespace A {
    namespace B {
        using namespace C;
        void print() {
            std::cout << i;
        }
    }
    int i = 3;
}

int main() {
    A::B::print();
}
```
> Ответ: <code>1</code>

38) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using namespace A;
    int i = 2;
    std::cout << i;
}
```
> Ответ: <code>2</code>

39) Язык Go. Код программы написан полностью в одном файле. Какое имя пакета должно быть указано в начале файла.<br>

> Ответ: <code>main</code>

40) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    using namespace A;
    int i = 2;
    std::cout << i;
}
```
> Ответ: <code>2</code>

41) Язык Go. Пакет импортирован следующим образом:&nbsp;<br>
<code>import example "github.com/vigo5190/example/name"</code><br>
Каким образом можно использовать экспортируемые имена из этого пакета в своём коде?<br>

> Ответ: <code>Имя из пакета name можно использовать так: example.требуемое_имя</code>

42) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace C{
    int i = 2;
}

namespace A {
    namespace B {
        void print() {
            std::cout << i;
        }
    }
    int i = 3;
}

int main() {
    A::B::print();
}
```
> Ответ: <code>1</code>

43) Язык Go. Может ли код пакета быть разделён на несколько .go файлов?<br>

> Ответ: <code>Да. При условии, что во всех файлах указано одно и тоже имя пакета и они лежат в одной папке</code>

44) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
inline namespace A{
    int i = 1;
}

int main() {
    std::cout << i;
}
```
> Ответ: <code>1</code>

45) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    std::cout << A::i;
}
```
> Ответ: <code>1</code>

46) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
int i = 1;

namespace C{
    int i = 2;
}

namespace A {
    int i = 3;
    namespace B {
        using C::i;
        void print() {
            std::cout << i;
        }
    }
}

int main() {
    A::B::print();
}
```
> Ответ: <code>2</code>

47) Дан фрагмент кода на С++. Что будет напечатано в результате его выполнения?
```cpp
namespace A{
    int i = 1;
}

int main() {
    std::cout << i;
}
```
> Ответ: <code>Ошибка</code>
