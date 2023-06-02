# Decorators-Time-measuring-tools-for-the-code
This Decorator measure in how long time the code is performed.
#Decorator
from time import time
def performance(fn):
  def wrapper(*args, **kawrgs):
    t1 = time()
    result = fn(*args, **kawrgs)
    t2 = time()
    print(f'it took {t2-t1} s')
    return result
  return wrapper

@performance
def long_time():
  for i in range(100000000):
   i*5

long_time()
