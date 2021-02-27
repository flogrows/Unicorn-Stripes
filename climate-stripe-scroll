import unicornhathd
import csv
import time

unicornhathd.rotation(90)
unicornhathd.brightness(0.5)

colours = {"r1":[254,224,210], "r2":[252,187,161], "r3":[252,146,114], "r4":[251,106,74],
           "r5":[239,59,44], "r6":[203,24,29], "r7":[165,15,21], "r8":[103,0,13],
           "b1":[222,235,247], "b2":[198,219,239], "b3":[158,202,225], "b4":[107,174,214],
           "b5":[66,146,198], "b6":[33,113,181], "b7":[8,81,156], "b8":[8,48,107]}

def colourpix(x,y,c):
    r = colours[c][0]
    g = colours[c][1]
    b = colours[c][2]
    unicornhathd.set_pixel(x,y,r,g,b)

with open('stripes.csv','r') as file:
    stripes = csv.reader(file, delimiter=',')
    stripe_list = [row[1] for row in stripes]

for scroll in range(155):
    for x in range(16):
        for y in range(8):
            colourpix(x,y,stripe_list[x+scroll])
    unicornhathd.show()
    time.sleep(0.1)


off = input("press c then enter to cancel: ")
if off == "c":
    unicornhathd.off()
