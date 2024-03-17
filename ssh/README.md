# Як підключитися до симулятору PLCnext з використанням SSH та отримати права root
![ua](https://img.shields.io/badge/lang-ua-blue.svg)

### 1. Запуск симулятору PLCnext з командного рядку:
- Використайте файл [runSimulation.bat](https://github.com/ebabeshko/plcnext-ua/blob/main/simulation/runSimulation.bat)

![PLCnext Simulation](https://github.com/ebabeshko/plcnext-ua/assets/63898296/5b4c5756-3a11-4aa5-83b3-6798e533e9ae)


### 2. Підключення з використанням SSH-клієнту:

- Використайте ```Putty``` або інший ```SSH-клієнт``` для підключення до IP-адреси, де запущено симулятор, або до 127.0.0.1, якщо симулятор запущено локально. За замовчуванням у симулятора SSH доступний на порту ```5555```.

![SSH](https://github.com/ebabeshko/plcnext-ua/assets/63898296/f9e5e049-3b80-4a10-90ce-80f03ab1eb28)


- Авторизуйтеся з іменем користувача ```admin``` та паролем ```plcnext```

![LOGIN](https://github.com/ebabeshko/plcnext-ua/assets/63898296/e81863e4-9eb0-495e-986e-41234fbee872)


### 3. Отримання прав root:

- Створіть пароль для користувача root, виконавши команду ```sudo passwd root```
  
```
sudo passwd root
```

> [!NOTE]
> Зверніть увагу, що користувачі ```admin``` та ```root``` - це різні користувачі. Завдання паролю для користувача root не вплине на користувача ```admin```.


![PASSWD](https://github.com/ebabeshko/plcnext-ua/assets/63898296/813a85c9-2289-4ab4-8f2e-99b1c906f7a5)

- Виконайте команду ```su``` та введіть пароль користувача root
  
```
su
```

![SU](https://github.com/ebabeshko/plcnext-ua/assets/63898296/6b538fd6-abc1-4658-b4b5-e3cde9f2f03f)

- Доступ root отримано!
