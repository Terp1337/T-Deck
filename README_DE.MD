<h1 align = "center">✨ LilyGO T-Deck  ✨</h1>

## **English | [中文](README_CN.MD) | [German](README_DE)** 



## 1️⃣ Vorschau der Beispiele

````

examples 
├─Keyboard_ESP32C3       # ESP32C3 keyboard I2C slave
├─Keyboard_T_Deck_Master # T-Deck read from keyboard
├─Microphone             # Noise detection  
├─Touchpad               # Read touch coordinates 
└─UnitTest               # Factory hardware unit testing           

````

## 2️⃣ Schnellstart

### PlatformIO

1. Installieren Sie [VisualStudioCode](https://code.visualstudio.com/) und [Python](https://www.python.org/)
2. Suchen Sie in der Erweiterung von `VisualStudioCode` nach dem `PlatformIO-Plugin` und installieren Sie es.
3. Nach Abschluss der Installation müssen Sie `VisualStudioCode` neu starten.
4. Nachdem Sie `VisualStudioCode` neu gestartet haben, wählen Sie in der oberen linken Ecke von VisualStudioCode ´Datei´ -> ´Ordner öffnen´ -> wählen Sie den Ordner ´T-Deck´ aus
5. Klicken Sie auf die Datei `platformio.ini`, und in der Spalte `platformio` kreuzen Sie die zu verwendende Beispielzeile an. Stellen Sie sicher, dass nur eine Zeile gültig ist.
6. Klicken Sie auf das Symbol (✔) in der unteren linken Ecke, um zu kompilieren
7. Schließen Sie die Platine an den Computer-USB an
8. Klicken Sie auf (→), um Firmware hochzuladen
9. Klicken Sie auf (Steckersymbol), um die serielle Ausgabe zu überwachen


### ArduinoIDE

1. Install [ArduinoIDE](https://www.arduino.cc/en/software)
2. Copy all the folders in the `T-Deck/lib` directory to `<C:\Users\UserName\Documents\Arduino\libraries>`. If there is no `libraries` directory, please create a new one. Please note that you are not copying the `lib` directory, but copying the folders in the lib directory
3. Open ArduinoIDE  ,`Tools` , Look at the picture to choose
    | T-Deck(ESP32S3)      | T-Keyboard(ESP32C3)  |
    | -------------------- | -------------------- |
    | ![s3](images/s3.jpg) | ![c3](images/c3.jpg) |
4. Insert USB into the PC and click Upload <If the upload fails, keep pressing the BOOT button, click RST, and then click Upload. When the upload is complete, click RST to exit the download mode>

## 3️⃣ Tips:

1. If a microphone is used, the GPIOO button cannot be used
2. If the sketch cannot be uploaded, then you need to press down the middle of the trackball, and then insert the USB, this means the chip is in the download mode, and then click to upload the sketch.
3. T-Keyboard the programming and burning interface of ESP32C3 is located at the 6Pin header on the side of the RST button, and the order starts from the top of the RST button, which are 3V3, GND, RST, BOOT, RX, TX, You need to connect USB TO TTL externally to burn the keyboard firmware. For TTL without automatic download circuit, before powering on, short-circuit the BOOT Pin and GND, and then power on. At this time, T-Keyboard will enter the download mode. After the burning is completed, you need to disconnect GND and BOOT before running the program.

   ![c3_boot](images/c3_boot.jpg)

4. T-Deck can't upload any sketch，Please enter the upload mode manually.
   1. Connect the board via the USB cable
   2. Press and hold the BOOT button , While still pressing the BOOT(On the trackball above the keyboard, press down) button
   3. Press RST button
   4. Release the RST button
   5. Release the BOOT button
   6. Upload sketch

## 4️⃣ Where to buy:

1. [AliExpress](https://www.aliexpress.com/item/1005005692235592.html)
2. [LilyGo Store](https://www.lilygo.cc/products/t-deck)



## 5️⃣ Pins:

See [utilities.h](./examples//UnitTest//utilities.h)
