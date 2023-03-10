# HW9
## Створення нейронної мережі
У цьому завдання ми створимо повнозв'язкову нейронну мережу, використовуючи при цьому низькорівневі механізми tensorflow.

Архітектутра нейромережі представлена на наступному малюнку. Як бачите, в ній є один вхідний шар, два приховані, а так само вихідний шар. Як активаційну функцію в прихованих шарах буде використовуватися сигмоїда. На вихідному шарі ми використовуємо softmax.

## Архітектура нейронної мережі

<img src="http://cs231n.github.io/assets/nn1/neural_net2.jpeg" alt="nn" style="width: 400px;"/>

## Про датасет MNIST

Дану нейромережу ми навчатимемо на датасеті MNIST. Цей датасет є великою кількістю зображень рукописних цифр розміром $28 \times 28$ пікселів. Кожен піксель набуває значення від 0 до 255.

Як і раніше датасет буде розділений на навчальну та тестову вибірки. При цьому ми виконаємо нормалізацію всіх зображень, щоб значення пікселів знаходилися у проміжку від 0 до 1, розділивши яскравість кожного пікселя на 255.

Крім того, архітектура нейронної мережі очікує на вхід вектор. У нашому випадку кожен об'єкт вибірки є матрицею. Що ж робити? У цьому завдання ми "розтягнемо" матрицю $28 \times 28$, отримавши при цьому вектор, що складається з 784 елементів.
