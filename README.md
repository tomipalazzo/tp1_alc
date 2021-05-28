# tp1_alc
Trabrajo Practico nro1 Algebra Lineal Computacional


Funciones:
	Generar matriz: genera una matriz de JxJ tridiagonal con 'unos' en la diagonal +-1 y '-2' 		en la diagonal principal
	
	res_L: Dada una Matriz diagonal ingerior y un vector b, resuelve Lx = b
	res_U: Dado un 'U' diagonal superior y un 'y' resuelve Ux = y
	
	LU: realiza la descomposicion LU de una matriz A
	
	resolver_sistema: dada una matriz A y un vector b, resuelve Ax = b utilizando la 		descomposicion LU.
	
	lu_tridiagonal: realiza la descomposicion LU de una matriz A tridiagonal, evitando operar 		sobre los ceros de la matriz.
	
	res_L_reducido:  Dada una Matriz L bidiagonal inferior, con unos en la diagonal principal, 		resuelve Ly = b.
	
	res_U_reducido: Dada una Matriz U bidiagonal superior, la funcion resuelve Ux=y.
	
	res_A_tridiagonal: dada una matriz A tridiagonal y un vector b, resuelve Ax = b utilizando 		la descomposicion LU reducida.
	
	generar_A_vec: dado los vectores d de (n,1), ds de (n-1,1) y di de (n-1,1), la funcion 		devuelve una matriz nxn con la diagonal principal = d, diagonal +1 = ds, diagonal -1 = di
	
	res_sistema_tri: resuelve el sistema de la matriz formada por los vectores aneriores t un 		vector b
	
	calcular_tiempo: calcula el tiempo de ejecucion de una funcion f
	
	calcular_tiempo: compara los tiempos de ejecucion de LU y LU_reducido, para matrices A de 		distintos tamaños, luego grafica los tiempos de cada una
