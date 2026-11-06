[[Recursion|Recursive]] way to colour a region of pixels starting from $(x, y)$:
```
floodfill(x, y):
    if (x,y) is out of range or already filled then return
    colour pixel (x,y)
    floodfill(x+1, y)
    floodfill(x-1, y)
    floodfill(x, y+1)
    floodfill(x, y-1)
```
The base case is "off the screen or already done", so it stops instead of looping forever
