# Collections

En el siguiente [link](https://github.com/programacion-basica-2-unlam/ejercicios/blob/master/Colllections.md) estan estos mismos ejercicios en formato un formato continuo mas piola sin saltos de pagina que genera el export a pdf

### Ejercicio 1

Crea los assert por cada punto y responde cada pregunta

```
public class ListTest {

    @Test
    public void listTest(){

        List<Integer>  miLista = new LinkedList<>();

        miLista.add(1);
        miLista.add(2);
        miLista.add(3);
        miLista.add(4);
        miLista.add(1);
        miLista.add(2);
        miLista.add(3);
        miLista.add(4);
            
        //1. miLista tiene 7 elementos

        //2. el cuarto elemento es 3

        // ¿que pasa en este caso?
        miLista.add(2,2);

        //3. ¿Como probarias lo que paso anterior?

        // ¿que pasa en este caso?
        miLista.remove(8);

	    // ¿que prueba se te ocurre?
    }

}
```

### Ejercicio 2

Modifica la siguiente porcion de codigo para que compile.
Explica que tuviste que agregar para que compile. 

```
public class ListTest {

    @Test
    public void borrarUnaPosicionNoExistente(){


        List<Integer>  miLista = new LinkedList<>();

        miLista.add(1);

	    miLista.remove()
    }
    
    @Test
    public void agregarUnElementoEnUnaPosicion(){

        List<Integer>  miLista = new LinkedList <>();

        miLista.add(1);
		miLista.add(2);

	    miLista.add(3, 3);
    }

}
```


### Ejercicio 3
Completa los siguientes siguiente test

```
public class ListTest {
  @Test
    public void ejemplosLista(){

        List<Integer>  miLista = new LinkedList<>();

        miLista.add(8);
        miLista.add(4);
        miLista.add(7);
        miLista.add(10);
        miLista.add(12);
        miLista.add(90);
        miLista.add(24);
        miLista.add(84);
        miLista.add(18);

        assertEquals(257, calcularPromedio(miLista), 0.01);
        assertEquals(90, buscarElMayor(miLista).intValue());

    }

    private Double calcularPromedio(List<Integer> miLista) {

        Double promedio = 0d;

       //...

        return promedio;
    }
    
    private Integer buscarElMayor(List<Integer> miLista) {

        //...
        return null;
    }
```

###Ejercicio 4

Dada la sentencia 

```
List<Integer>  miLista = new LinkedList<>(); 
```
Cual de las siguientes lineas son validas 
para reemplazar la sentencia anterior

```
/*a*/ List<Integer> miLista = new List<>();
/*b*/ List<Integer> miLista = new List<Integer>();
/*c*/ List<Integer> miLista = new ArrayList<Integer>();
/*d*/ List<Integer> miLista = new LinkedList<String>();  
```


### Ejercicio 5

Que diferencia existe entra la implementacion de un
ArrayList y la de LinkedList y contesta las siguientes preguntas.

* ¿Puedo hacer lo mismo con los dos?
* ¿Hay algo que puedo hacer con uno que con otro no?
* ¿Cuando usarias cada uno de ellos?


### Ejercicio 6
Modifica Los puntos 1,2 y 3 con las sentencias validas del punto 4 y comprueba que todos los test den verde
Explica por que sucede esto


### Ejercicio 7

Dada la clase Cuadrado y la interfaz Figura 

```
public interface Figura {


    Double calcularArea();
    Double calcularPerimetro();
}
```

```
public class Rectangulo implements Figura{

    private Double lado1;
    private Double lado2;


    public Rectangulo(Double lado1, Double lado2){

        this.lado1 = lado1;
        this.lado2 = lado2;
    }

    public Double calcularArea(){

        return lado2 * lado1;
    }

    public Double calcularPerimetro(){

        return this.lado2 * 2 + this.lado1 * 2;
    }

    public Double diferenciaArea(Rectangulo rectangulo){

        return this.calcularArea() - rectangulo.calcularArea();
    }

}  
```

Que modificaciones tenes que hacer para que el siguiente test de verde

```
 @Test
 public void ordenarRectangulosDeMenorAMyorPorPerimetro(){

        List<Rectangulo>  miLista = new LinkedList<>();

        miLista.add(new Rectangulo(4d,6d));
        miLista.add(new Rectangulo(3d,2d));
        miLista.add(new Rectangulo(4d,5d));


        Collections.sort(miLista);

        assertEquals(10, miLista.get(0).calcularPerimetro());
        assertEquals(18, miLista.get(1).calcularPerimetro());
        assertEquals(20, miLista.get(2).calcularPerimetro());

    }
```

**Tip:** investiga el funcionamiento de la clase [Collections](https://docs.oracle.com/javase/7/docs/api/java/util/Collections.html#sort(java.util.List)) 

**Tip:** pegale una mirada a este [link](https://www.geeksforgeeks.org/comparator-interface-java/)

### Ejercicio 8

Completa el siguiente test

```
@Test
 public void ordenarRectangulosDeMenorAMyorPorSuperfice(){

        List<Rectangulo>  miLista = new LinkedList<>();

        miLista.add(new Rectangulo(4d,6d));
        miLista.add(new Rectangulo(3d,2d));
        miLista.add(new Rectangulo(4d,5d));


        Collections.sort(miLista, new Comparator<Rectangulo>() {
            @Override
            public int compare(Rectangulo o1, Rectangulo o2) {
                return 0;// implementa la comparacion
            }
        });

		
        Double superficie1 = 0d; 
        Double superficie2 = 0d;
        Double superficie3 = 0d;
        assertEquals(superficie1, miLista.get(0));
        assertEquals(superficie2, miLista.get(1));
        assertEquals(superficie3, miLista.get(2));

    }
```

### Ejercicio 9

El siguiente test no compila, falta declarar la variable **unaColeccion**. Declara la variable y cambia el valor del variable tamanioEsperado para que el test de verde 

```
public class SetTest {

    @Test
    public void listTest(){	

		unaColeccion.add(1);
		unaColeccion.add(1);
		assertEquals(1,unaColeccion.size());
		   
		unaColeccion.add(2);
		unaColeccion.add(3);
		
		Integer tamanioEsperado = 0;
assertEquals(tamanioEsperado,unaColeccion.size());       
		
	}  
}
```

### Ejercicio 10

Implementa el metodo eliminar repetidos y prueba que funciona correctamente

```
public class ListTest {

    @Test
    public void listTest(){

        List<Integer>  miLista = new LinkedList<>();

        miLista.add(1);
        miLista.add(2);
        miLista.add(3);
        miLista.add(4);
        miLista.add(1);
        miLista.add(2);
        miLista.add(3);
        miLista.add(4);
       
       Set sinRepetidos = eliminarRepetidos(miLista);     
       
    }
    
    private Set<Integer> eliminaRepetidos(List<Integer> miLista){
    
    }
}
```
### Ejercicio 11

¿Que pasa con el orden de insercion de los elemenos de un Set cuando lo iteras?

### Ejercicio 12

Queremos borrar la linea 

```
	Collections.sort(miLista)
```

del test del Ejercicio 7 y que el mismo siga dando verde. ¿Que cambios tenes que hacer?

```
 @Test
 public void ordenarRectangulosDeMenorAMyorPorPerimetro(){

        List<Rectangulo>  miLista = new LinkedList<>();

        miLista.add(new Rectangulo(4d,6d));
        miLista.add(new Rectangulo(3d,2d));
        miLista.add(new Rectangulo(4d,5d));


        Collections.sort(miLista);

        assertEquals(10, miLista.get(0));
        assertEquals(18, miLista.get(1));
        assertEquals(20, miLista.get(2));

    }
```

### Ejercicio 13

Completa el valor de la variable indiceEsperado para que el test de verde y contesta las preguntas

```
@Test
    public void mapaTest(){


        Map<Integer,Integer> mapa = new HashMap<>();


        mapa.put(1,2);
        mapa.put(2,4);
        mapa.put(3,6);

        Integer indiceEsperado;
        assertEquals(6, mapa.get(indiceEsperado).intValue());
        
    }
```

* ¿Como llamamos a los numeros 1,2 y 3? 
* ¿Son la posicion del elemento en el Mapa?


### Ejercicio 14

¿Como haria para obtener el promedio de las claves del ejercicio anterior?


### Ejercicio 15

Utilizando el ejercicio 13 implementa el metodo **crearNuevoMapa** para que el siguiente test de verde

```
@Test
public void mapearElementosTest(){
	
	
    Map<Integer,Integer> mapa = new HashMap<>();
	
	
    mapa.put(1,2);
    mapa.put(2,4);
    mapa.put(3,6);
	
    Map<Integer, String> otroMapa = crearNuevoMapa(mapa);
    
    
    assertEquals(otroMapa.get(1), "El doble de 1 es 2");
    assertEquals(otroMapa.get(2), "El doble de 2 es 4");
    assertEquals(otroMapa.get(3), "El doble de 3 es 6");
	
}
```

### Ejercicio 16

Explica la diferencia entre los dos assertNull del siguiente test

```
@Test
public void nullElements(){


    Map<Integer,Integer> mapa = new HashMap<>();


    mapa.put(1,null);
    
    
    assertNull(mapa.get(1);
    assertNull(mapa.get(2;
    
}
```

### Ejercicio 17

Crea un metodo que te devuelva todos los multiplos de 4 ordenados de menor a mayor

```
@Test
public void multiplosDe4Ordenados(){


    Map<Integer,Integer> mapa = new HashMap<>();

    mapa.put(1,2);
    mapa.put(2,4);
    mapa.put(3,6);
    mapa.put(12,24);
    mapa.put(6,12);
}
```
