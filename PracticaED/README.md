Práctica 2
Antonio y Beatriz deciden darse de alta como clientes en el Banco Java y abrirse una cuenta. La política del banco es que para abrir una cuenta haya que aportar exactamente 100€.
Antonio y Beatriz consultan el saldo de su cuenta y comprueban que efectivamente, cada uno tiene 100€.
Antonio pide 50€ prestados a Beatriz, así que realizan una transferencia y luego vuelven a consultar el saldo.
Pasados unos días Antonio gana 100€ en una rifa y Beatriz tiene que pagar 30€ a hacienda, así que cada uno ingresa y retira el dinero correspondiente.
Como Beatriz se ha quedado con menos dinero en la cuenta, Antonio hace una nueva transferencia para devolverle los 50€ a Beatriz.
Nos pidieron codificar todo, y el resultado es el siguiente:

	1public class TestBanco {
	2public static void main(String[] args) {
	3/* Antonio y Beatriz se hacen cliente del banco */
	4Cliente antonio = new Cliente(123456789Z, Antonio Alonso, Av. Pueblo Saharaui, s/n);
	5Cliente beatriz = new Cliente(987654321A, Beatriz Benítez, Calle Sol, 4);
	6 
	7/* Por defecto, todas las cuentas nuevas tienen 100€ */
	8Cuenta cuentaAntonio = new Cuenta(48151, 100, antonio);
	9Cuenta cuentaBeatriz = new Cuenta(62342, 100, beatriz);
	10 
	11/* Antonio y Beatriz consultan el saldo */
	12System.out.println(La cuenta de  + cuentaAntonio.getCliente().getNombre() +  tiene 
	13+ cuentaAntonio.getSaldo() +  euros.);
	14System.out.println(La cuenta de  + cuentaBeatriz.getCliente().getNombre() +  tiene 
	15+ cuentaBeatriz.getSaldo() +  euros.);
	16 
	17/* Beatriz transfiere 50€ a Antonio */
	18cuentaBeatriz.setSaldo(cuentaBeatriz.getSaldo() - 50);
	19cuentaAntonio.setSaldo(cuentaAntonio.getSaldo() + 50);
	20 
	21/* Antonio y Beatriz vuelven a consultar para comprobar que todo ha ido bien */
	22System.out.println(La cuenta de  + cuentaAntonio.getCliente().getNombre() +  tiene 
	23+ cuentaAntonio.getSaldo() +  euros.);
	24System.out.println(La cuenta de  + cuentaBeatriz.getCliente().getNombre() +  tiene 
	25+ cuentaBeatriz.getSaldo() +  euros.);
	26 
	27/* Antonio gana 100€ en una rifa y hace un ingreso en su cuenta */
	28cuentaAntonio.setSaldo(cuentaAntonio.getSaldo() + 100);
	29 
	30/* Beatriz tiene que pagar 30€ a hacienda y retira el dinero */
	31cuentaBeatriz.setSaldo(cuentaBeatriz.getSaldo() - 30);
	32 
	33/* Antonio transfiere 50€ a Beatriz */
	34cuentaAntonio.setSaldo(cuentaAntonio.getSaldo() - 50);
	35cuentaBeatriz.setSaldo(cuentaBeatriz.getSaldo() + 50);
	36}
	37}

Se pide:

	1Ejercicio 1: Crear un nuevo repositorio privado en Github y enlazarlo con Eclipse.
	2Ejercicio 2: Abir tres issues en Github: Subir código fuente, Refactorizar el código y Comentar el código.
	3Ejercicio 3: Subir la solución aportada enlazando el commit con el primer issue y cerrarlo.
	4Ejercicio 4: Refactorizar el código enlazando los commits necesarios con el segundo issue. Cerrar el issue cuando la tarea esté completada.
	5Ejercicio 5: Usar las herramientas de JavaDoc para comentar los métodos que hayan surgido como resultado de la refactorización. Enlazar los commits con el tercer issue y cerrar el issue cuando la tarea esté completada.
	6Ejercicio 6: Compartir el proyecto conmigo (usuario mjmartinezstudium).

Hay que entregar un único archivo PDF que contenga:
	•Enlace a tu repositorio privado de Github con la práctica resuelta.
	•Documentación de cómo se han realizado los ejercicios 1 y 6.
	•Explicación de qué patrones de refactorización se han aplicados y por qué.
