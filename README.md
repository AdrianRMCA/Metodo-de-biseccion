# Metodo-de-biseccion

#evaluo primer valor medio
m = a + (b - a)/2

#Evaluacion de la función en los puntos a,b y m
fa = funcion1(a)
fb = funcion1(b)
fm = funcion1(m)

print("#inter\t\t a \t\t f(a) \t\t f(b) \t\t m \t\t f(m) \t\t error")
print("{0} \t\t {1:6.4f} \t {2:6.4f} \t {3:6.4f} \t {4:6.4f} \t {5:6.4f} \t {6:6.4f} \t {7:6.4f}".format(niter,a0, fa, b0, fb, m, fm, error))

#ciclo iterativo
while error > tol and niter < nmax:
 m = a + (b - a) / 2
 if np.sign(fa) == np.sign(fm):
  a = m
  fa = funcion1(a)
else:
  b = m
  fb = funcion1(b)

m = a + (b - a)/2
fm = funcion1(m)
error = abs(b - a)
niter += 1
print("{0} \t\t {1:6.4f} \t {2:6.4f} \t {3:6.4f} \t {4:6.4f} \t {5:6.4f} \t {6:6.4f} \t {7:6.4f}".format(niter, a, fa, b, fb, m, fm, error ))

print("La raíz de la función dada en el intervalo [{0:6.4f},{1:6.4f}] es {2:6.7f}".format(a0,b0,m))
