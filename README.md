# Como traducir con UABEA Avalonia
## _Unity - PowerQuest_
Buscar en _"sharedassets0.assets"_ o en otro que esté el monobehaviour con nombre _"SystemText"_ que además tiene un tamaño bastante mayor. Con **UABEA Avalonia** se puede traducir sin problemas.

## _Unity - Adventure Creator_
Buscar primero con **TotalCommander** cualquier texto que aparezca durante el juego. Nos dirá en qué recurso aparece. Abrir **UABEA Avalonia** y buscar en los asset con nombre _"ActionSpeech"_. Hay debe estar todo el texto. Seleccionar todos los _"ActionSpeech"_ y dar a ***"Export Dump"***, nos preguntará en qué carpeta exportar. Tan solo queda traducir el texto que aparezca y de nuevo, seleccionando los _"ActionSpeech"_, debemos darle ***"Import Dump"*** y aparecerá señalados con un asterisco. Solo queda darle a _"Save"_.

## **Ejemplos**
## _Brassheart (Unity - Adventure Creator)_
Existe un archivo con nombre _"data.unity3d"_ que es un bundle comprimido. Usar **UABEA Avalonia** para descomprimir en una carpeta. Luego meter todos los archivos descomprimidos en la carpeta ***"Brassheart Prologue_Data"*** y quitar el archivo anterior. 
Existen subtítulos en cinemáticas y en el gameplay. Para traducir los primeros, se busca algún texto que aparezca con **Total Commander** y nos arroja un resultado en el archivo ***"Assembly-CSharp.dll"***, el cual se pueden traducir usando **"dnSpy"**. Para los segundos hay que volver a usar **Total Commander** y nos mostrará que está en varios archivos, el que nos interesa, por pruebas que he realizado, es ***"resources.assets"*** y debemos usar **UABEA Avalonia** e irnos hasta el asset _"Klucz_SpeechManager"_ con ***pathid 6365***. Podremos observar que el tamaño de este asset es muy grande, pues guarda todos los diálogos. Usar la opción _"Export Dump"_ en forma txt. Traducir lo que queramos y volver a **UABEA** para usar _"Import Dump"_. Le damos a _"Save"_ y ya está traducido.

## **NOTAS**
Si nos diera el caso de que Unity esté usando ***"il2cpp"***, hay que usar la herramienta **"il2cppdumper"** sobre el archivo ***"Gameassembly.dll"*** y extraer todos los recursos en una carpeta temporal. Luego copiar esos recursos extraidos en la carpeta ***"Manager"*** donde debería estar el archivo ***"Assembly-CSharp.dll"*** y en el programa **UABEA** desactivar la opción _"Cpp2Il"_.

## TO-DO
- Poner imágenes.
