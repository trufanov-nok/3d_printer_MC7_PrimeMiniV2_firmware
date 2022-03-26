# 3d_printer_MC7_PrimeMiniV2_firmware
A copy of 3D MC7 Prime mini v2.0 (https://masterkit.ru/shop/2090858) firmware (https://masterkit.ru/zip/3d-start-v2-marlin-mc7-sd.rar).
It's a fork of Marlin provided by the 3D Printer authors.

I've bought such a 3D Printer Kit, assembled it and realized that filament feeder motor holder isn't good enough.
So I printed it by myself and found out that I forget to mirror the detail scl file and thus I needed to move the filament feeder form the left side
of 3D Printer to the right side if I want to use it. I did so and then I realized that I need to invert the motor rotation direction after that.
There are two ways - hardware and software. The software one is to recompile the Marlin firmware with a right E0 drive direction value and flash
it to Arduino.
I've downloaded a copy of Marlin firmware that's provided by the 3D Printer Kit supplier and tried to compile it in Arduino IDE.
Unfortunately, a build process failed on my machine with one error and one warning. I fixed both and uploaded patched firmware copy to this repository.

Main branch original tag - original firmware
Main branch fixed_comp tag - the original firmware with compillation errors and warnings fixed
Adjusted branch - is a fixed_comp with adjustmends needed for my printer (E0 motor direction changed, E0 axis resolution scaled).

===========

Это копия прошивки 3D принтера-конструктора 3D MC7 Prime mini v2.0 (https://masterkit.ru/shop/2090858).
Саму прошивку можно скачать с сайта продавца: https://masterkit.ru/zip/3d-start-v2-marlin-mc7-sd.rar
Она является форком одной из старых версий Marlin.

Я купил такой принтер, собрал его, и меня не устроила одна из деталей конструкции подачи филамента.
Я перепечатал эту деталь из поставляемых с принтером моделей, но не заметил, что она отзеркалена и рассчитана на крепление
с правой стороны принтера, а не с левой. В итоге я перевесил мотор направо, но оказалось, что теперь нужно инвертировать направление вращения
двигателя, подающего филамент. Это можно сделать хардварно (перекинув некоторые провода в контакте двигателя) и программно - в прошивке.
Я скачал прошивку, поставляемую вмести с принтеров и попытался скомпилировать её в Arduino IDE, но сборка на моей машине завершилась одной
ошибкой и одним warning'ом. Я их устранил и результаты заливаю в этот репозиторий.

Ветка main тэг original - оригинальная прошивка
Ветка main тэг fixed_comp - оригинальная прошивка с исправленными ошибками компиляции
Ветка adjusted - прошивка fixed_comp с некоторыми изменениями, которые были мне нужны (инвертированное направление мотора E0 и кол-во его шагов на сантиметр)
