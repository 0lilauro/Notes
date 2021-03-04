# O Principio da substituição de Barbara Liskov

Barbara Liskov, uma cientista da computação,  introduziu em 1987 os primeiros principios da substituição de liskov: 


### O Principio da substituição:

> Se S é subtipo de T, então S deve poder ser usado em qualquer situação em que T pode ser usado.

Por exemplo: 

```c++
struct Retangle {
    // code ...
}
struct Square: Retangle {
    // code ...
}

int main () {
    Retangle* r = new Square();
    return 0;
}
```

No caso acima é possivel quebrar o comportamento da substituição ?

SIm, quando os coportamentos da classe Square não condizem com os da classe retangle 