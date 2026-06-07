# Para mencionar a otra persona 

```git

$ git commit -m "Adicionar nova funcionalidade. 

> 

> 

Co-authored-by: NOMBRE <nombre@email.com> 

Co-authored-by: OTRO-NOMBRE <otro@email.com>" 
```

- Esta manera de hacer un commit es para que en GitHub pueda ser facil de identificar para quien va dirigido

- La estructura exacta es:  
	`Co-authored-by: Nombre Apellido <correo@email.com>`
	
	- **Co-authored-by:** comando de git
	
	- **Nombre:** Va justo después de los dos puntos. Puede llevar espacios pero no es necesario que tenga el nombre exacto pero es bueno para llevar un orden en GitHub.
	
	- **Correo:** Es obligatorio y **debe ir encerrado entre los símbolos de menor y mayor que (`< >`)**. Si no pones los símbolos `< >`, Git lo ignorará y no le dará el crédito a tu compañero.


---