<h1 align = "center">✨ LilyGO T-Deck  ✨</h1>

## **German | [中文](README_CN.MD) | [English](READM.MD)** 



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

1. Installieren Sie [ArduinoIDE](https://www.arduino.cc/de/software)
2. Kopieren Sie alle Ordner im `T-Deck/lib`-Verzeichnis in `<C:\Users\UserName\Documents\Arduino\libraries>`. Wenn nicht vorhanden, erstellen Sie bitte einen neuen Ordner. Bitte beachten Sie, dass Sie nicht den `lib`-Ordner, sondern die Ordner im lib-Ordner kopieren.
3. Öffnen Sie ArduinoIDE, gehen Sie zu `Werkzeuge` und wählen Sie das passende Board aus
    | T-Deck(ESP32S3)      | T-Keyboard(ESP32C3)  |
    | -------------------- | -------------------- |
    | ![s3](images/s3.jpg) | ![c3](images/c3.jpg) |
4. Stecken Sie den USB-Stecker in den PC und klicken Sie auf "Hochladen". <Wenn der Upload fehlschlägt, halten Sie die BOOT-Taste gedrückt, klicken Sie auf RST und klicken Sie dann auf Hochladen. Nach dem Hochladen klicken Sie auf RST, um den Download-Modus zu beenden.>

## 3️⃣ Tipps:

1. Wenn ein Mikrofon verwendet wird, kann die GPIOO-Taste nicht verwendet werden
2. Wenn das Skript nicht hochgeladen werden kann, müssen Sie die Mitte des Trackballs drücken und dann den USB anschließen. Dies bedeutet, dass der Chip im Download-Modus ist, und dann klicken Sie, um das Skript hochzuladen.
3. Die Programmier- und Brennschnittstelle von ESP32C3 für T-Keyboard befindet sich am 6-poligen Stecker neben der RST-Taste, und die Reihenfolge beginnt von der Oberseite der RST-Taste, und dies sind 3V3, GND, RST, BOOT, RX, TX, Sie müssen USB VON TTL extern anschließen, um das Tastatur-Firmware zu brennen. Für TTL ohne automatische Downloadschaltung kurzschließen Sie vor dem Einschalten die BOOT-Pin und GND und schalten Sie dann ein. In diesem Fall wird T-Keyboard in den Download-Modus schalten. Nach Abschluss des Brennens müssen Sie GND und BOOT vor dem Ausführen des Programms trennen.

   ![c3_boot](images/c3_boot.jpg)

4. Das Skript für T-Deck kann nicht hochgeladen werden. Bitte gehen Sie manuell in den Upload-Modus.
   1. Verbinden Sie die Platine über das USB-Kabel.
   2. Halten Sie die BOOT-Taste gedrückt.
   3. Drücken Sie während Sie die BOOT-Taste gedrückt halten die RST-Taste.
   4. Lassen Sie die RST-Taste los.
   5. Lassen Sie die BOOT-Taste los.
   6. Skript hochladen.

## 4️⃣ Where to buy:

1. [AliExpress](https://www.aliexpress.com/item/1005005692235592.html)
2. [LilyGo Store](https://www.lilygo.cc/products/t-deck)



## 5️⃣ Pins:

See [utilities.h](./examples//UnitTest//utilities.h)
