# TomasPonceEmbarcadero26
Realizar los ejercicios hasta la página 7 - (Ejercicio 4)... pero hacerlos móvil   (file - new - Multidevice Aplication)

Ejercicio 1:

 Crear una nueva aplicación VCL (librería visual C para Windows) escogiendo del menú: File  New  VCL FormApplicaton C++ Builder.

 En un formulario nuevo, desde la Tool palette, añade un
componente TButton (botón Button1). Desde el panel de
propiedades, cambia su propiedad Caption por: Aceptar

 Pulsa doble clic sobre el botón e introduce el código (en el
evento OnClic del botón Button1) por:

void __fastcall TForm1::Button1Click(TObject *Sender)
{
Button1->Caption="Vale";
ShowMessage ("Hola mundo");
}

(Importante escribir “Button” con la 1a letra en mayúsculas, ya que C++ distingue mayúsculas de minúsculas)
 Prueba la aplicación pulsando en Run .

 Si funciona correctamente, guarda la aplicación: File  Save all . El archivo de proyecto se llamará Clase0cpp.
Ejercicio 2:

 Abre el proyecto anterior Clase0cpp.

 Desde la Tool palette, añade al ejercicio anterior un
componente TEdit y un componente TLabel con las
propiedades de la imagen:

 Cambiar el evento: OnClick del botón Button1 por:

void __fastcall TForm1::Button1Click(TObject *Sender)
{
ShowMessage("Hola, " + Edit1->Text + ".");
}

ShowMessage es una función que sirve para mostrar una ventana
de mensaje

Guarda el proyecto con el nombre: ClaseunoCpp

Ejercicio 3. Contador:

StrToInt y InttoStr: Son funciones que convierten un valor de numérico entero (Integer) a texto (String) y viceversa

 Recupera el ejercicio anterior.

 Cambia el texto (propiedad caption) del botón por: 0

 Añade un segundo botón a la ventana formulario desde la paleta
Tool palette – sección Standard: Tbutton

Al botón 2 cambia el texto (propiedad caption) por Contar

Pulsa doble clic encima de él, para abrir la ventana de código.

Entre las llaves { } debes escribir el código:

Button1->Caption= Button1->Caption +1;

Si lo ejecutas (run), verás cuenta mal porque añade la letra 1 pero no suma el número 1

Para ello hay que convertir las letras en números enteros: string to integer o abreviado: StrToInt

Button1->Caption = StrToInt(Button1->Caption) +1;

Si ahora lo ejecutas, verás que ya funciona.

 Si funciona correctamente, guarda la aplicación: File – Save Project as.. El archivo de proyecto se llamará Contador.

 File – Save as...Guarda la unidad como: Contador1.cpp

Ejercicio 4: Conversor

Ejercicio:

 Crear una nueva aplicación VCL (librería visual c para windows) escogiendo
del menú: File - New – VCL Form Applicaton C++ Builder.

 En el formulario nuevo, desde la Tool palette, añade: 2 edits, 1 botón y 3
labels

 Cambia la propiedad caption de las label y del botón para que muestre el
texto de la imagen.

 Pulsa doble clic encima del botón para llamar al evento (on click)
void __fastcall TForm1::Button1Click(TObject *Sender) y escribe:

Edit2->Text=Edit1->Text * 1.3;

Si no funciona correctamente escribe en su lugar:

Edit2->Text=StrToInt(Edit1->Text) * 1.3;

 Si funciona correctamente, guarda toda la aplicación: Fila – Save all

El archivo de proyecto se llamará Conversor y la unidad: Conversor1.cpp

Usar dos botones con la misma función (usando el parámetro sender)

Añade un segundo botón Button2 como en la imagen. 

En el código del botón Button1 cambia el código por el del recuadro.

 En el evento onclick del botón 2 tienes que asignar el mismo evento que el del botón 1 para que ambos botones
llamen a la misma función.

 Si funciona correctamente, guarda toda la aplicación: Fila – Save all.

Ejercicio 4 ext: - Área del triángulo
 Añadir al ejercicio anterior los componentes de la imagen.

 Cambiar el evento: OnClick del botón Button1 por:

void __fastcall TForm1::Button1Click(TObject *Sender)
{
Edit3->Text=FormatFloat("###.##",Edit1->Text.ToDouble() *
Edit2->Text.ToDouble()/ 2 );

}
