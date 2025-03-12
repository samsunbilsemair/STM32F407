# STM32F407
# PYTHON İLE STM32F407 KULLANIMI
import pyb
yesilLed = pyb.Pin("PD12", pyb.Pin.OUT_PP)  #yeşil
yesilLed.on()

turuncuLed = pyb.Pin("PD13", pyb.Pin.OUT_PP)  #turuncu
turuncuLed.on()

kirmiziLed = pyb.Pin("PD14", pyb.Pin.OUT_PP)  #kırmızı
kirmiziLed.on()

maviLed = pyb.Pin("PD15", pyb.Pin.OUT_PP)  #mavi
maviLed.on()

zaman = 250
"""

for i in range(5):#range(5)
    yesilLed.on()
    pyb.delay(zaman)
    yesilLed.off()
    pyb.delay(zaman)
 
"""

ledList = [yesilLed, turuncuLed, kirmiziLed, maviLed]
#ledlist[0]=yesilLed
while True:
    for i in range(0, 4):
        ledList[i].on()
        pyb.delay(zaman)
        ledList[i].off()
        pyb.delay(zaman)
    pyb.delay(1000)

import pyb

# LED nesnelerini bir liste içinde tanımlayalım
leds = [pyb.LED(1), pyb.LED(2), pyb.LED(3), pyb.LED(4)]
bekle = 250  # Gecikme süresi (ms)

while True:
    # LED'leri ileri doğru yak
    for led in leds:
        led.on()
        pyb.delay(bekle)
        led.off()

    # LED'leri geri doğru yak
    for led in reversed(leds[:-1]):  # Son LED’i iki kez yakmamak için son elemanı çıkarıyoruz
        led.on()
        pyb.delay(bekle)
        led.off()