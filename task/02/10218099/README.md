# 10218099
Nawaf Alfarizki


## materi sebelumnya
+ Menentukan solusi dari persamaan differensial menggunakan metode euler
+ Menentukan solusi dari persamaan differensial menggunakan metode runge-kutta orde 4
+ Menentukan solusi dari persamaan diff
+ Menentukan solusi dari sistem osilasi teredam
+ Menentukan suatu fungsi menggunakan metode monte carlo


## materi paling menarik
+ Menentukan suatu fungsi menggunakan metode monte carlo


## materi paling membosankan
+ Menentukan solusi dari osilasi teredam


## materi yang sudah dipami
+ Metode monte carlo


## materi yang belum dipahami
+ Metode runge-kutta, hubungannya dengan menggunakan persamaan numerik biasa


## contoh program
+ Buat suatu contoh program dalam Python dan sertakan di sini dengan hasil keluarnnya.

```python
# import numpy as np

def func1(x):
    # function f(x)= 10 + sum_i(-x_i^2)
    # for 2D: f(x)= 10 - x1^2 - x2^2
    return 10 + np.sum(-1*np.power(x, 2), axis=1)
  
def mc_integrate(func, a, b, dim, n = 1000):
    # Monte Carlo integration of given function over domain from a to b (for each parameter)
    # dim: dimensions of function
    
    x_list = np.random.uniform(a, b, (n, dim))
    y = func(x_list)
    
    y_mean =  (y.sum())/len(y)
    domain = np.power(b-a, dim)
    
    integ = domain * y_mean
    
    return integ

# Examples
print("For f(x)= 10 - x1\u00b2 - x2\u00b2, integrated from -2 to 2 (for all x's)")
print(f"Monte Carlo solution for : {mc_integrate(func1, -2, 2, 2, 1000000): .3f}")
print(f"Analytical solution: 117.333")

print("For f(x)= 10 - x1\u00b2 - x2\u00b2 - x3\u00b2, integrated from -2 to 2 (for all x's)")
print(f"Monte Carlo solution: {mc_integrate(func1, -2, 2, 3, 1000000): .3f}")
print(f"Analytical solution: 384.000")
```

Hasilnya adalah
For f(x)= 10 - x1² - x2², integrated from -2 to 2 (for all x's)
Monte Carlo solution for :  117.356
Analytical solution: 117.333
For f(x)= 10 - x1² - x2² - x3², integrated from -2 to 2 (for all x's)
Monte Carlo solution:  383.733
Analytical solution: 384.000
```
```


## cara perkuliahan
+ Kuliah berjalan dengan baik tetapi kurang dalam mensimulasikan apa yang diajarkan secara teori/konseptual dan aplikasinya terhadap permasalahan fisis/nyata


## topik sistem fisis
+ Sistem agen dari suatu objek fisis terkuantisasi (butiran, bisa juga manusia (agent-based))


## simulasi dan visualisasi
+ Apakah Anda tertarik dengan simulasi dan visualisasi? Jelaskan topik yang ingin Anda simulasikan / visualisasikan serta cantumkan alasannya dan perkiraan pusataka Python yang perlu digunakan.
+ Simulasi dan visualisasi dari pergerakan suatu benda fisis mengikuti fungsi tertentu bisa order/chaos. Seperti bagaimana virus covid menyebar, bagaimana menemukan solusi dari three-body problem, bagaimana menebak fungsi dari suatu naik turunnya indeks saham. Pustaka Python yang mungkin digunakan adalah Pandas, Seaborn, SciPy, atau Numpy
