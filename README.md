# PROYECTO LIBROS
| Integrante:             |
|-------------------------|
| Lorenzo Masgo Josue Elí |

El CODIGO LIBRO, es un programa que proporciona una biblioteca básica para organizar libros

## FUNCIÓN MAIN():

  Este método es el mas destacable ya que todo programa empieza ejecutandose por este. Este metodo al iniciarse presenta un Menú, los cuales son los siguientes:


  1. Agregar libro
  2. Buscar libro por título
  3. Mostrar todos los libros
  4. Salir  

  La opción 1 del menú en el programa permite al usuario agregar un nuevo libro a la biblioteca. Solicita al usuario que ingrese el título, autor y año de publicación del libro deseado.
  Luego, valida que el título y el autor estén presentes. Si se proporcionan estos detalles, se crea un nuevo objeto Libro con la información ingresada.
  Este libro se agrega a la biblioteca utilizando el método correspondiente. Si no se proporciona un título o un autor, se informa al usuario del error.  

  Los errores que esta opción posee son las siguientes:  

  ***ErrorLibroSinTitulo***  : Cuando no se ingresa un título al libro
  
  ***ErrorLibroSinAutor*** : Cuando no se ingresa un autor al libro  

  ***ValueError*** : Cuando se ingresa una letra a la fecha del libro

  En todos los errores no se guarda la información caso contrario se almacena, asimismo se puede buscar y mostrar los datos  

  La opción 2 permite al usuario buscar un libro en la biblioteca utilizando su título. El programa solicita al usuario que ingrese el título del libro que desea buscar.
  Luego, busca en la biblioteca un libro que coincida exactamente con el título proporcionado. Si encuentra un libro con ese título, muestra los detalles del libro encontrado (título, autor y año de publicación).
  Si no se encuentra ningún libro con el título especificado, se informa al usuario con un error "No se encontró ningún libro con el título '{Dato ingresado}'"  

  La opción 3 muestra todos los libros presentes en la biblioteca. Si la biblioteca está vacía, se muestra el siguiente mensaje "La biblioteca está vacía".
  Si la biblioteca contiene libros, se muestra una lista con los detalles de cada libro, incluyendo su título, autor y año de publicación.  

  Por último, la opción 4 permite al usuario salir del programa. Al seleccionar esta opción, se muestra un mensaje de despedida "¡Hasta luego!" y el programa termina su ejecución.

## CLASE BIBLIOTECA:  

***__init__(self)*** : Inicializa una nueva instancia de la clase Biblioteca. Crea una lista vacía llamada libros que almacenará los libros en la biblioteca.  

***agregar_libro(self, libro)*** : Agrega un nuevo libro a la biblioteca. Verifica que el libro tenga un título y un autor antes de agregarlo a la lista de libros. Si el libro pasa las validaciones, se agrega a la lista libros de la biblioteca.

***buscar_libro(self, titulo)*** : Busca un libro en la biblioteca por su título. Itera sobre la lista de libros y compara el título de cada libro con el título proporcionado. Si encuentra un libro con el título especificado, lo devuelve. Si no se encuentra ningún libro con ese título, levanta una excepción.

***mostrar_libros(self)*** : Muestra todos los libros en la biblioteca. Verifica si la lista de libros está vacía. Si la lista no está vacía, imprime los detalles de cada libro (título, autor y año de publicación). Si la lista está vacía, muestra un mensaje indicando que la biblioteca está vacía.

## CLASE LIBRO: 

***__init__(self, titulo, autor, año_publicacion)***: Inicializa una nueva instancia de la clase Libro con los atributos titulo, autor y año_publicacion.
Estos atributos representan respectivamente el título del libro, el autor del libro y el año de publicación del libro.  

## CLASES DE ERROR: (***ErrorLibroSinTitulo***, ***ErrorLibroSinAutor*** y ***ValueError***)  
  
***__init__(self, mensaje)*** : Inicializa excepciones personalizadas para libros sin título o autor.
