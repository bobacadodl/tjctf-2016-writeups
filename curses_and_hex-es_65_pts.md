# Curses and Hex-es (65 pts)

---

## Problem
Wow! I think I just magicked a flag into this image.

---

## Solution
We take the pixel values of each image, convert to hex, and concatenate them.

```python
from PIL import Image
im = Image.open("curses_and_hexes.png")
width, height = im.size
a=open('out.txt','w')
for pixel in im.getdata():
    a.write(chr(pixel[0]))
    a.write(chr(pixel[1]))
    a.write(chr(pixel[2]))
a.close()
```

We then get a long text, seemingly from a book. Inside we find the flag (ctrl+f "tjctf").

---

## Flag
`tjctf{y0u'r3_a_w1z4rd_H4rry!!}`