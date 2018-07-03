En el siguiente [link](https://github.com/programacion-basica-2-unlam/ejercicios/blob/master/Exceptions.md) estan estos mismos ejercicios en formato un formato continuo mas piola sin saltos de pagina que genera el export a pdf

### Ejercicio 1

* ¿Cual es la diferencia entre una chequeada y una no chequeada?


### Ejercicio 2

A continuacion te mostramos un ejemplo de como se prueba una que un metodo arroje una Eception


```
@Test(expected = Exception.class)
public void queLaDividionPorCeroArrojeUnaException() throws Exception{

	Calculadora c = new Calculadora();
	
	c.dividir(2,0);
	
} 

```

Basandote en este test crea la clase CalculadoraTest y la clase Calculadora para que cumpla con el test anterior.


### Ejercicio 3

Crea un excepcion no chequeada llamada DivisionPorCeroException 
refactoriza el metodo dividir de la clase calculadora para que arroje esta nueva excepcion. 

### Ejercicio 4

Crea los test que cubran el siguiente método

```
public class UsuarioService{

public Usuario registrar(Persona unaPersona) 
throws NotBlankException{

	if(!unaPersona.esMayorEdad(){
		throw new PersonaMenorDeEdadExepction("Para regisgistrarte tenes que ser mayor de edad")
	}
	
	if(unaPersona.getNombre() == null ||
	   unaPersona.getApellido() == null   ){
			throw new Exception("Los atributos nombre y apellido no pueden ser null");
	}
	
		if("".equals(unaPersona.getNombre() ||
		   "".equals(unaPersona.getApellido()   ){
						throw new NotBlankException("Los atributos nombre y apellido no pueden ser vacios");
	}

	Usuario usuario = new Usuario()
	usuario.setNombre(unaPersona.getNombre() 
				 + "." + unaPersona.getNombre());
	
	return usuario; 
	
} 

```

El codigo no compila, tenes que realizar algunos cambios para que lo haga y crear todas las clases que creas necesarias.



