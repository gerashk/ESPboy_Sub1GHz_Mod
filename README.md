Библиотека Rc-switch взята от сюда https://github.com/arendst/Tasmota
В файле RCSwitch.h были изменены
строка 62 #define RCSWITCH_MAX_CHANGES 67 // default 67  на #define RCSWITCH_MAX_CHANGES 157        // default 67
строка 68 #define RCSWITCH_SEPARATION_LIMIT 4100 на #define RCSWITCH_SEPARATION_LIMIT 6000

в файле RCSwitch.cpp
добавлен протокол 
{ 20,  16, { 14, 30 }, 1, { 510,  30 }, { 14,  30 }, { 30, 14 }, false,  230 }  // 39 (Louvolite) with premable

Библиотека SmartRC-CC1101 заменена с версии 2.5.2 на 2.5.7 
в файле ELECHOUSE_CC1101_SRC_DRV.cpp было много изменений


в основном скетче в разделе setup добавлено   ELECHOUSE_cc1101.setDRate(5);       // Set the Data Rate in kBaud. Value from 0.02 to 1621.83. Default is 99.97 kBaud! , чем ниже скорость тем больше дальность. с значением 5 , дальность устройства 300-500метров
