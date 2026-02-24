# Summative-Assignment---01-An-Interactive-Game


Presentation :
file:///C:/Users/radhi/AppData/Local/Packages/5319275A.WhatsAppDesktop_cv1g1gvanyjgm/LocalState/sessions/C5046863B52DAB33B60A848E1694B84D75B04482/transfers/2026-08/ODT%20PRESENTATION%20FINAL.pdf

Canva Original link : https://www.canva.com/design/DAHCN-e8WIs/RcXKK8lx0MFZkhaYGrYiDQ/edit?utm_content=DAHCN-e8WIs&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

(The final photos of the end to end process of the interactive game are in the given presentation)

Photos : file:///C:/Users/radhi/AppData/Local/Packages/5319275A.WhatsAppDesktop_cv1g1gvanyjgm/LocalState/sessions/C5046863B52DAB33B60A848E1694B84D75B04482/transfers/2026-08/Workinprogress_ODT.pdf

The Code :

from machine import PWM, Pin
import time
import neopixel
import random

n=neopixel.NeoPixel(Pin(21),16)
b=Pin(18, Pin.OUT)
pb=Pin(19,Pin.IN,Pin.PULL_UP)

while True:
    pb_val=pb.value()
    for r in range(0,16,1):
        r=random.randint(0,15)
        n[r]=(225,4,0)
        n.write()
        time.sleep(0.05)
        n[r]=(0,0,0)
        if pb_val==0:
            if r==8:
                b.value(1)
                time.sleep(0.05)
                b.value(0)
                print("Success!")
                break
            elif r!=8:
                b.value(1)
                print("Better Luck Next Time!")
                time.sleep(0.05)
                break
        time.sleep(0.05)


The Youtube video link : https://youtube.com/shorts/b4FsV_x7oaU?feature=share

THANKYOU...

        
