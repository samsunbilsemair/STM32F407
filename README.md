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

