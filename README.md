﻿# linear_algebra

import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
#import seaborn as sns

x = [-2, 2, -2, 2]
y = [-4, 4, 0.5, 2.5]

fig = plt.figure()
plt.axhline(y=0, c='black')
plt.axvline(x=0, c='black')

ax = plt.gca()
ax.set_xlim(-2.5,2.5)
ax.set_ylim(-3,4)

from functools import partial

arraw_vector = partial(plt.arrow,width=0.01,head_width=0.1,head_length=0.2,length_includes_head=True)

arraw_vector(0,0,2,-1,color='g')
arraw_vector(0,0,-1,2,color='c')
arraw_vector(2,-1,-2,4,color='b')
arraw_vector(0,0,0,3,color='r',width=0.05)

plt.draw()

plt.show()

plt.close(fig)


