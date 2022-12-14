# input type="number"

Можна вказати мінімум `min`, максимум `max` для валідації, та крок `step`. Браузери додають до таких полів стрілочки "більше/менше". Їх дизайн залежить від браузера.

```html
<!-- ціле число -->
<input type="number" id="nHumd" name="n_humd" min="1" max="99" step="1">
<!-- десятковий дріб -->
<input type="number" id="nTemp" name="n_temp" min="-20" max="40" step="0.1">
<!-- початкове значення -->
<input id="number" type="number" value="42">
```
`pattern` (шаблону регулярного виразу) для валідації не підтримується. Обґрунтування цього полягає в тому, що введені числа не будуть дійсними, якщо вони містять щось, крім чисел, і ви можете обмежити мінімальну та максимальну кількість дійсних цифр за допомогою атрибутів `min` і `max`.

### Докладніше:

- (https://developer.mozilla.org/ru/docs/Web/HTML/Element/Input/number) :link:
- (https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/inputmode) :link:

### Мої примітки:

На різних системах (або браузерах?) по-різному.  
На Linux Chrom - проходять валідацію і крапки, і коми.  
На Win95 Firefox - в одному випадку проходять тільки крапки, в іншому тільки коми...  
Очевидно, поля з type "number" добре підходять **тільки для цілих чисел**. Особливо це **зручно на мобільних**, де вмикається цифрова клавіатура і валідний розділовий символ - крапка або кома.
