.686
.model flat,c
.stack 4896
data
public SumProcedure
code
SumProcedure PROC
enter 0,0
mov eax, [ebp + 8]
mov ebx, [ebp + 12]
add eax, ebx
leave
ret 8
SumProcedure ENDP
END

.686
.model flat, c
.stack 4896
.data
resultMessage db "2*x: ",
public Power0fTwo
code
PowerOfTwo PROC
mov eax, 1
cmр есх, 0
je done
calculate:
shl eax, 1
loop calculate
15
16
done:
17
ret
18
Power0fTwo ENDP
19
20
END

#include <iostream>
#include <Windows.h>
extern "C" void SumProcedure();
extern "C" void Power0fTwo(int x);
extern "C" void CompareStrings();
int main()
i
int su Result;
＿asm
push 3
push 5
call SumProcedure
mov sw Result, eax
std::cout << "Summa: "< sumResult << std::endl;
6
17
18
int powerResult;
int exponent = 4;
19
20
＿asm
mov ecx, exponent
21
call Power0fTwo mov powerResult, eax std::cout << "2*" << exponent << ": " << powerResult << std::endl;
22
23
24
25
call CompareStrings
26
asu i
27
28
return 0;
29
30
31

# Ароматный мир

 Приложение разработано для компании - ООО «Ароматный мир» - магазин по продаже парфюмерии и косметики. 

## Начало работы

Эти инструкции предоставят вам копию проекта и помогут запустить на вашем локальном компьютере для разработки и тестирования.

## Функции 

- Аутентификация пользователей: пользователи могут зарегистрироваться и войти в систему, чтобы заказать определённые товары.
- Управление товарами: пользователи могут создавать, удалять, (обновлять - Администратор) товар в своих заказах.
- Сортировка: Пользователи могут сортировать товары (заказы) по определённым значениям.
- Срок выполнения задачи: пользователи могут устанавливать срок выполнения для каждой задачи и получать напоминания.
- Просмотр заказов определёнными пользователями: Администраторы и Менеджеры могут удалять, обновлять заказы пользователей.
- Получение чека: Пользователь может получить чек после оформления и оплаты заказа.

### Необходимые условия

- Visual Studio (рекомендуемая версия: Visual Studio 2022) - .NET Framework 8.0
- SQL Server Management Studio 20 и сервер

### Установка

Пошаговая серия примеров для установки проекта:
1. Скопируйте репозиторий с помощью команды:
```
git clone https://github.com/DenobBlack/Exam2114.git
```
3. Настройка базы данных
    - Убедитесь, что у вас установлен SQL Server Management Studio и его сервер.
    - Откройте SSMS и подключитесь к вашему серверу баз данных.
    - Создайте новую базу данных и запустите SQL скрипт(Exam2114.bacpac или Скрипт БД.txt) проекта для создания таблиц, заполнения их начальными данными, создание пользователя ispp2114(по желанию можно поменять логин) и процедур, необходимых для нормального функционирования приложения.
    - Нажмите ПКМ по вашему серверу → Свойства → Безопасность → Аутентификация через SQL Server и Windows → "OK" → Нажмите ПКМ по вашему серверу → Перезагрузка
3. Откройте проект в Visual Studio.

__ВАЖНО__

Поменяйте значение свойств с информацией о базе данных в классе DataAccessLayer два раза кликнув по нему
![Picture](https://github.com/DenobBlack/Exam2114/blob/8c2aa6a575302f712ef7bc95f2dde5460f0b76fd/DataAccessLayer.png)

Затем замените подписанные данные, если они не совпадают с вашими
![Picture](https://github.com/DenobBlack/Exam2114/blob/8c2aa6a575302f712ef7bc95f2dde5460f0b76fd/Data.png)
   
5. Запустите проект, нажав кнопку "Start" или F5.

__Пример работы приложения в роли "Гостя"__
![Picture](https://github.com/DenobBlack/Exam2114/blob/635be778bec5b97fbba8c3cc3b880424939c1537/image.png)

## Авторы

* Хомутов Максим Андреевич - студент 2 курса группы ИСПП-21
* Баранов Егор Алексеевич - студент 2 курса группы ИСПП-21


