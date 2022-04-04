
import random
from random import randint
from rich import print
from rich.panel import Panel
from colour import Color
import time

x = [0,1,2,3,4]
S = "C:\\Users\\mgla56\\Desktop\\ex_test\\dedent.txt"
class ColorUp():
    def __init__(self, a, b):
        self.a = a
        self.b = b
        self.c = []
    def color_up(self):
        self.a = Color(self.a)
        self.b = Color(self.b)
        self.c = list(self.a.range_to(self.b, 5))
        return self.c

class Ran_X():
    def __init__(self, y):
        self.y = y
        
    def IndexT(self):
        Inde = random.randint(0, len(self.y)- 1)
        return   self.y[Inde]
        



if __name__ == "__main__":
    
    col = ColorUp("red", "violet")
    col.color_up()
    ranx = Ran_X(x)
    ranx.IndexT()
    #r = ranx.IndexT()
    
    with open(S) as file:
        data = file.read() #работает все буквы разные по цвету
        #file.readline()
        for num_line, line in enumerate(data, 1):
            n = len(line)
            if line == n:
                line = f'{line}'
            time.sleep(.01)
            #print(f'[bold {col.c[r]}]{line}', end='')
            print(f'[bold {col.c[ranx.IndexT()]}]{line}', end='')#все буквы разные по чвету
            #print(Panel.fit(f'[bold {col.c[ranx.IndexT()]}]{line}',border_style=f"{col.c[ranx.IndexT()]}"), end='')#меняем не только цвет строк но и border
