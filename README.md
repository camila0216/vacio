# Parcial Camila Gómez Schrader 201531412

El celular utilizado para el desarrollo del parcial corresponde a un Moto G5 plus con Android Oreo. Se realizó un proyecto en Java que contiene el sdk dentro de la carpeta. Para correrlo solo basta con darle click derecho a la clase Script.java y hacer click en la opción "Run As" y después en "2 Java Application".

# Comandos

Dimensiones de la pantalla: adb shell wm size
1080x1920

Instalar una app: adb install ./com.whatsapp_452954_apps.evozi.com.apk

Abrir la app: adb shell monkey -p com.whatsapp -c android.intent.category.LAUNCHER 1

Ir al menú de home: adb shell input keyevent 3

Tomar un screen ejemplo: adb shell screencap /sdcard/AppAbierta.png

Hacer pull de un screen ejemplo: adb pull /sdcard/AppAbierta.png ./img/AppAbierta.png

Entrar a la primera App haciendo click: adb shell input tap 100 400

Hacer long tab en las primeras 3 applicaciones: adb shell input touchscreen swipe 100 400 100 400 3000, shell input touchscreen swipe 500 400 500 400 3000, input touchscreen swipe 980 400 980 400 3000

Conectarse al celular desde wifi: adb tcpip 5555, adb shell "ip addr show wlan0 | grep -e wlan0$ | cut -d\" \" -f 6 | cut -d/ -f 1", adb connect 172.20.10.5:5555

Agregar un contacto: adb shell am start -a android.intent.action.INSERT -t vnd.android.cursor.dir/contact -e name 'Camila Gomez' -e phone 3678906123.

Devolverse: adb shell input keyevent 4

Desinstalar la aplicación: adb uninstall ./com.whatsapp_452954_apps.evozi.com.apk

# Screenshots e Imágenes
Los screenshots solicitados se encuentran dentro de la carpeta img del proyecto. De igual forma la secuencia completa de comandos puede verse en la consola a medida que va corriendo el script. 

