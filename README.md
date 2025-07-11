# Game Wheel — управление потенциометрами через Arduino как игровой руль

Этот проект позволяет использовать потенциометры как руль, газ, тормоз и сцепление, создавая полноценный самодельный контроллер для игр. Работает через Arduino и эмуляцию VJoy.

## 🎛️ Подключение потенциометров к Arduino

| Элемент        | Arduino | Назначение    |
|----------------|---------|---------------|
| `xValue`       | A0      | Руль          |
| `yValue`       | A1      | Газ           |
| `zValue`       | A2      | Тормоз        |
| `sliderValue`  | A3      | Сцепление     |
| `VCC`          | 5V      | Питание       |
| `GND`          | GND     | Земля         |

---

## 🚀 Как запустить

### 1. Arduino
- Открой `arduino.ino` в **Arduino IDE**.
- Залей код на плату (например, Arduino Uno).

### 2. Настройка VJoy
- Скачай и установи **VJoy**.
- Запусти **VJoy Config** → нажми **"Add Device"**.
- Отметь галочки: **X**, **Y**, **Z**, **Slider**.
- В поле **"Number of Buttons"** установи значение `3`.

### 3. Python-скрипты (на ПК)

#### 📌 Перед запуском:
- Установи необходимые библиотеки:
  ```bash
  pip install pyserial pyvjoy tkinter

Вариант 1: joyv1.py

Открой файл в редакторе.

Укажи свой COM-порт Arduino вручную в коде.

Запусти скрипт.

Вариант 2: joyv2.py

Запусти программу.

Выбери COM-порт Arduino через графический интерфейс (Tkinter).

🕹️ Возможное применение

Симуляция управления в автосимуляторах.

Альтернатива геймпаду.

DIY-контроллер для роботов, машинок, авиасимуляторов и т.д.

📌 Примечания

Если ты используешь Linux, порт будет выглядеть примерно как /dev/ttyUSB0.

Если не работает — проверь драйвер VJoy и права администратора.

Подходит для игр вроде Euro Truck Simulator, BeamNG, Assetto Corsa и других.

👨‍💻 Автор

Bublika© (2025)
Проект создан как DIY-альтернатива дорогим игровым рулям.
