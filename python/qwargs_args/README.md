# `*`args i `**`qwargs

У функцію в Python можна передати змінну кількість аргументів двома способами:

- `*args` - для неіменованих аргументів; (**arg**ument**s**).
- `**kwargs` -  для іменованих аргументів (**k**ey**w**ord **arg**ument**s**).

Ми використовуємо `*args` і `**kwargs` як аргумент, коли завчасно невідомо, скільки значень ми захочемо передати функції.

[Приклад функції, яка цікава тим, що один її параметр може приймати як рядок, так і список або словник](#my_func)


### Приклад з `*args`:

```python
def adder(*nums):
    sum = 0

    for n in nums:
        sum += n

    print("Sum: ", sum)

adder(3, 5)
adder(4, 5, 6, 7)
adder(1, 2, 3, 5, 6)
```
```
Sum: 8
Sum: 22
Sum: 17
```

### Приклад з `**kwargs`:

```python
def intro(**data):
    print("\nData type of argument: ",type(data))

    for key, value in data.items():
        print("{} is {}".format(key, value))

intro(Firstname="Sita", Lastname="Sharma", Age=22, Phone=1234567890)
intro(Firstname="John", Lastname="Wood", Email="johnwood@nomail.com", Country="Wakanda", Age=25, Phone=9876543210)
```
Ми отримаємо наступне:
```
Data type of argument: <class 'dict'>
Firstname is Sita
Lastname is Sharma
Age is 22
Phone is 1234567890

Data type of argument: <class 'dict'>
Firstname is John
Lastname is Wood
Email is johnwood@nomail.com
Country is Wakanda
Age is 25
Phone is 9876543210
```

- `*args` і `**kwargs` — спеціальний синтаксис, що дозволяє передавати змінну кількість аргументів у функцію. При цьому зовсім не обов'язково використовувати саме такі імена аргументів: 'args' і 'kwargs';
- `*args` використовується для неіменованих аргументів, з якими можна працювати як зі списком;
- `**kwargs` використовується для іменованих аргументів, з якими можна працювати як зі словником;
- якщо ви хочете використовувати і `*args`, і `**kwargs`, це робиться так: `func(fargs, *args, **kwargs)`, порядок аргументів є важливим;

<a href="my_func"></a>
### Приклад функції, яка цікава... 

... тим, що один її параметр може приймати як рядок, так і список або словник і в залежності від цього обробляє передані дані

```python
# ---------------------------------------------------------------------
def log(level, mess, vals=None):

	if vals:
		if isinstance(vals, str):
			logger.log(level, mess.format(vals))    # рядок
		elif isinstance(vals, (tuple, list)):
			logger.log(level, mess.format(*vals))   # список/кортеж
		elif isinstance(vals, dict):
			logger.log(level, mess.format(**vals))  # словник
	else:
		logger.log(level, mess)
```
