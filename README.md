# compiler

#Установка
  - Скачайте данный репозиторий
  - Откройте проект в IDE c установленным Antlr4 плагином
  
#Запуск
  - Запустите Main.java (аргументом должен подаваться файл с кодом на языке MathLanguage, по умолчанию - test1.math)
  - В результате выполнения программы исходный код из файла test1.math будет преобразован в код на языке Java, хранящийся по пути:
 (project_directory)/compiled/scr/result/Main.java
   - Получившийся код будет выполнен и вы увидите результат работы программы test1

#Грамматика
 - Была реализована грамматика языка, описывающего математические вычисления
 - Файл граматики хранится по пути: (project_directory)/scr/main/java/compiler/grammar/mathGrammar.g4

# Демо

## test1.math: 
```
   fun integer fExample (integer data) {
    data=data+1
    return data
}

main {
  integer k = 6
  float n = 1.2

  const integer m = 3

  integer a = 0
  integer b = 5

  integer h = (integer) n

  a = ((k*h)/m + 5^2 - m%2)-1
  print a

  a = fExample(a)
  print a

  float j = n + 1.5

  for (b=0; b<7; b++){
  a=b
  print a

  }

  if (j>=n){
  print j
  }
  else{
  print n
  }

  while (b>0){
  b=b-1
  print b
  }

  for (b=0; b<7; b++){
  a=b
  print a

  }


}
```
## Сгенерированный Main.java: 
```
// program Test1_math compiled on Sun May 24 11:14:22 MSK 2020
package result;
public class Main {
private static int fExample(int data){
data=data+1;
return data;
}
public static void main(String[]args) throws Exception{
int k = 6;
float n = 1.2f;
final int m = 3;
int a = 0;
int b = 5;
int h = (int)n;
a=((k*h)/m+5^2-m %2)-1;
System.out.println(a);
a=fExample(a);
System.out.println(a);
float j = n+1.5f;
for (b=0; b<7; b++){
a=b;
System.out.println(a);
}
if (j>=n){
System.out.println(j);
}else{
System.out.println(n);
}
while (b>0){
b=b-1;
System.out.println(b);
}
for (b=0; b<7; b++){
a=b;
System.out.println(a);
}
}
}



```

# Приятного использования!
