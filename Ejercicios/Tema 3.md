Ejercicio con utilización de funciones y librerias  
  
Fuente:   
Universidad Johns Hopkins  
Python for Genomic Data Science  
  
~~~
import time

x="absbsbsbscss"
y="b"
def count1(dna, base):
    i = 0
    for c in dna:
        if c == base:
	    i += 1 
    return i

def count2(dna, base):
    i = 0 
    for j in range(len(dna)):
        if dna[j] == base:
	    i += 1 
    return i 

def count3(dna, base):
    match = [c == base for c in dna]
    return sum(match)

def count4(dna, base):
    return dna.count(base)

def count5(dna, base):
    return len([i for i in range(len(dna)) if dna[i] == base])

def count6(dna,base):
    return sum(c == base for c in dna)

t0 = time.time()
print count1(x,y)
print time.time() - t0
t0 = time.time()
print count2(x,y)
print time.time() - t0
t0 = time.time()
print count3(x,y)
print time.time() - t0
t0 = time.time()
print count4(x,y)
print time.time() - t0
t0 = time.time()
print count5(x,y)
print time.time() - t0
t0 = time.time()
print count6(x,y)
print time.time() - t0
~~~
