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
