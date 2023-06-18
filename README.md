# Python-Metodo-Cadena-de-Caracteres
Las cadenas de texto soportan una gran cantidad de métodos para transformaciones básicas y búsqueda.


# Metodos de cadenas de caracteres

Los métodos de caracteres son funciones incorporadas en Python que se pueden aplicar a las cadenas para realizar diversas operaciones, como manipulación, búsqueda, reemplazo y transformación de cadenas

`#` str.capitalize()

  Retorna una copia de la cadena con el primer carácter en mayúsculas y el resto en minúsculas.
  
    capitalize = 'capitalize'.capitalize()
    print(capitalize) # Capitalize

`#`  str.casefold()

  Retorna el texto de la cadena, normalizado a minúsculas. Los textos así normalizados pueden usarse para realizar búsquedas textuales independientes de mayúsculas y minúsculas.
  
      casefold = 'CaseFold'.casefold()
      print(casefold) # casefold

`#` str.endswith('cadena'[, start[, end]])

  Retorna True si la cadena termina con la 'cadena' especificada y False en caso contrario. También podemos usar 'cadena' para pasar una tupla de sufijos a buscar. Si especificamos el parámetro opcional start, la comprobación empieza en esa posición. Con el parámetro opcional stop, la comprobación termina en esa posición.

      endswith = 'busca una cadena'.endswith('cadena')
      print(endswith)

`#`  str.find(sub[, start[, end]])

   Retorna el menor índice de la cadena s donde se puede encontrar la cadena sub, considerando solo el intervalo s[start:end]. Los parámetros opcionales start y end se interpretan como notación de segmento. Retorna -1 si no se encuentra la cadena.
   
   El método find() se debe usar solo si se necesita saber la posición de la cadena sub. Si solo se necesita comprobar si sub es una parte de s, es mejor usar el operador in.
   
    find = 'busca una cadena de texto en especifico'.find('texto')
    print(find) # Respuesta: 20 
    find = 'busca una cadena de texto en especifico'.find('existe')
    print(find) # Respuesta: -1
    
`#`  str.format()

   Realiza una operación de formateo. La cadena de caracteres sobre la que se está ejecutando este método puede contener texto literal y también marcas de reemplazo de texto definidas mediante llaves {}. Cada sección a reemplazar contiene o bien un índice numérico que hace referencia a un parámetro por posición, o el nombre de un parámetro por nombre. Retorna una copia de la cadena donde se han sustituido las marcas de reemplazo por los valores correspondientes pasados como parámetros.
    
    metodoFormat = 'La suma de 5 + 6 es igual a {0}'.format(5+6)
    print(metodoFormat) # La suma de 5 + 6 es igual a 11
    
`#` str.index('cadena')

   Como find(), pero lanza una excepción de tipo ValueError si no se encuentra la cadena a buscar.
    
    index = 'busca una cadena de texto en especifico'.index('texto')
    print(index) # Respuesta: 20 
    index = 'busca una cadena de texto en especifico'.index('existe')
    print(index)
    # Respuesta
    '''
    Traceback (most recent call last):
      File "/Users/user/Desktop/tutoriales/Python/Metodos-de-Caracteres/metodosCaracteres.py", line 25, in <module>
        index = 'busca una cadena de texto en especifico'.index('existe')
    ValueError: substring not found
    '''
    
    

`#` str.islower()

   Retorna True si todos los caracteres de la cadena que tengan formas en mayúsculas y minúsculas están en minúsculas y hay, al menos, un carácter de ese tipo, en caso contrario, retorna False.

    isLower = 'minuscula'.islower()
    print(isLower) # True
    
`#` str.isupper()

   Retorna True si todos los caracteres de la cadena que tengan formas en mayúsculas y minúsculas 4 están en mayúsculas y hay, al menos, un carácter de ese tipo, en caso contrario, retorna False.
   
      isUpper = 'MAYUSCULA'.isupper()
      print(isUpper) # Respuesta: True
      isUpper = 'mayuscula'.isupper()
      print(isUpper) # Respuesta: False
      isUpper = ' '.isupper()
      print(isUpper) # Respuesta: False
      
 
`#` str.join(iterable)

   Retorna una cadena de caracteres formada por la concatenación de las cadenas en el iterable. Se lanza una excepción de tipo TypeError si alguno de los elementos en el iterable no es una cadena, incluyendo objetos de tipo bytes. Se usa como separador entre los elementos la cadena de caracteres pasada como parámetro.
   
    from pathlib import Path
    import os
    
    BASE_DIR = Path(__file__).resolve().parent.parent # Buscamos el directorio actual
    concatenado = os.path.join(BASE_DIR, 'metodoCaracteres') # y lo concatenenamos con el directorio al cual queremos hacer referencia
    print(concatenado) # Respuesta: /Users/user/Desktop/tutoriales/Python/metodoCaracteres
    
El módulo os.path proporciona funciones y constantes para trabajar con rutas de archivo y directorio, y os.path.join() es una función específica que combina partes de una ruta en una ruta completa y válida, teniendo en cuenta el separador de ruta adecuado para el sistema operativo en uso.


 `#` str.lower()

   Retorna una copia de la cadena de caracteres con todas las letras en minúsculas.
    
      minuscula = 'PalabraEnMINUSCULA'.lower()
      print(minuscula) # Resultado: palabraenminuscula
   
   
 `#`  str.lstrip([chars])

   Retorna una copia de la cadena, eliminado determinados caracteres si se encuentren al principio. El parámetro chars especifica el conjunto de caracteres a eliminar. Si se omite o si se especifica None, se eliminan todos los espacios en blanco. No debe entenderse el valor de chars como un prefijo, sino que se elimina cualquier combinación de sus caracteres:
   
    lstrip = 'elimina determinados caracteres si se encuentran al principio'.lstrip('abceli')
    print(lstrip) # mina determinados caracteres si se encuentran al principio
 
 Es importante tener en cuenta que el método lstrip() no modifica la cadena original, sino que devuelve una nueva cadena con los caracteres eliminados. Si deseas actualizar la variable original, debes asignar el resultado a la misma variable o a una nueva variable.
 

`#` str.replace(old, new[, count])

   Retorna una copia de la cadena con todas las ocurrencias de la cadena old sustituidas por new. Si se utiliza el parámetro count, solo se cambian las primeras count ocurrencias.
   
   

