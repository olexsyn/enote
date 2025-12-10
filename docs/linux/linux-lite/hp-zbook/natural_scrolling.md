# Налаштування планшетної прокрутки

```
Device 'AlpsPS/2 ALPS DualPoint TouchPad':
	Device Enabled (156):	1
	Coordinate Transformation Matrix (158):	1.000000, 0.000000, 0.000000, 0.000000, 1.000000, 0.000000, 0.000000, 0.000000, 1.000000
	libinput Tapping Enabled (284):	1
	libinput Tapping Enabled Default (285):	0
	libinput Tapping Drag Enabled (286):	1
	libinput Tapping Drag Enabled Default (287):	1
	libinput Tapping Drag Lock Enabled (288):	0
	libinput Tapping Drag Lock Enabled Default (289):	0
	libinput Tapping Button Mapping Enabled (290):	1, 0
	libinput Tapping Button Mapping Default (291):	1, 0
	libinput Natural Scrolling Enabled (292):	0
	libinput Natural Scrolling Enabled Default (293):	0
	libinput Disable While Typing Enabled (294):	1
	libinput Disable While Typing Enabled Default (295):	1
	libinput Scroll Methods Available (296):	1, 1, 0
	libinput Scroll Method Enabled (297):	1, 0, 0
	libinput Scroll Method Enabled Default (298):	1, 0, 0
	libinput Middle Emulation Enabled (299):	1
	libinput Middle Emulation Enabled Default (300):	1
	libinput Accel Speed (301):	-0.600000
	libinput Accel Speed Default (302):	0.000000
	libinput Accel Profiles Available (303):	1, 1, 1
	libinput Accel Profile Enabled (304):	1, 0, 0
	libinput Accel Profile Enabled Default (305):	1, 0, 0
	libinput Accel Custom Fallback Points (306):	<no items>
	libinput Accel Custom Fallback Step (307):	0.000000
	libinput Accel Custom Motion Points (308):	<no items>
	libinput Accel Custom Motion Step (309):	0.000000
	libinput Accel Custom Scroll Points (310):	<no items>
	libinput Accel Custom Scroll Step (311):	0.000000
	libinput Left Handed Enabled (312):	0
	libinput Left Handed Enabled Default (313):	0
	libinput Send Events Modes Available (269):	1, 1
	libinput Send Events Mode Enabled (270):	0, 0
	libinput Send Events Mode Enabled Default (271):	0, 0
	Device Node (272):	"/dev/input/event7"
	Device Product ID (273):	2, 8
	libinput Drag Lock Buttons (314):	<no items>
	libinput Horizontal Scroll Enabled (315):	1
	libinput Scrolling Pixel Distance (316):	15
	libinput Scrolling Pixel Distance Default (317):	15
	libinput High Resolution Wheel Scroll Enabled (318):	1
```


Добре. Оскільки твій тачпад зараз керується через **libinput** як PS/2 пристрій, зробимо скрипт, який при запуску сесії встановлює “натуральну” прокрутку і налаштовує швидкість курсору.

Створюємо файл, наприклад `~/.config/touchpad-settings.sh`:

```bash
#!/bin/bash
# Налаштування AlpsPS/2 ALPS DualPoint TouchPad через libinput

# Отримуємо ID пристрою
DEVICE="AlpsPS/2 ALPS DualPoint TouchPad"
ID=$(xinput list --id-only "$DEVICE")

# Вмикаємо натуральну прокрутку (пальці вниз -> прокрутка вниз)
xinput set-prop $ID "libinput Natural Scrolling Enabled" 1

# Швидкість курсору (-1.0 до 1.0, 0.0 — стандартна)
xinput set-prop $ID "libinput Accel Speed" 0.2

# Вмикаємо тап-дії (якщо потрібно)
xinput set-prop $ID "libinput Tapping Enabled" 1
```

Потім робимо скрипт виконуваним:

```bash
chmod +x ~/.config/touchpad-settings.sh
```

І додаємо його в автозапуск сесії. Наприклад, для **GNOME / Xfce / KDE** можна додати у **Startup Applications** або додати рядок у `~/.xprofile`:

```bash
~/.config/touchpad-settings.sh &
```

Після перезавантаження сесії курсор і прокрутка будуть працювати зручно:

* Планшетна прокрутка
* Контроль швидкості тачпаду
* Тапи та перетягування працюють
