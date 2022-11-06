<h1> Delincuencia en Chile 2017-2022</h1>
<p></p>

<h2>Herramientas y entorno de trabajo</h2>
<p>Para el desarrollo de este proyecto se utilizaron las siguientes herramientas:</p>
<ul>
    <li>Sistema Operativo: Linux Ubuntu</li>
    <li>Editor de código: VSCode</li>
    <li>Lenguaje de programación: Python 3.8.10</li>
</ul>

<h2> Procesamiento y obtención de datos</h2>
<h3>1. Obtención de datos</h3>
<p>Los datos han sido obtenido a través del <a href="http://cead.spd.gov.cl/estadisticas-delictuales/">Centro de Estudios y Análisis del Delito (CEAD)</a>. Se utilizaron los siguientes parámetros de búsqueda:</p>

<h4>Estadísticas por delito</h4>
<ul>
    <li><b>[Medida]:</b> Frecuencia</li>
    <li><b>[Tipo de Datos]:</b> Casos policiales</li>
    <li><b>[Unidad Territorial]: </b>
        <ul>
            <li><b>[Regiones]:</b> TOTAL PAÍS</li>
        </ul>
    </li>
    <li><b>[Delito]:</b>
        <ul>
            <li><b>[Grupo Delictual]:</b> Ninguno (de todas forma se autoselecciona).</li>
            <li><b>[Delitos]:</b> Se seleccionaron todos los delitos.</li>
        </ul>
    </li>
    <li><b>[Temporalidad]:</b>
        <ul>
            <li><b>[Año]:</b> 2017, 2018, 2019, 2020, 2021, 2022</li>
            <li><b>[Mes]:</b> Enero, Febrero, Marzo, Abril, Mayo, Junio, Julio, Agosto, Septiembre, Octubre, Noviembre, Diciembre</li>
        </ul>
    </li>
</ul>

<h3>2. Modificación para lectura del archivo</h3>
<p>El archivo resulta una extensión <b>.xls</b>, al tener dificultades para leerlo, se procesa el archivo de manera manual.</p>
<ol>
    <li>Se crea una carpeta <b>data</b> y dentro un archivo <b>delitos_2017_2022.csv</b>-</li>
    <li>Se abre reportesEstadisticos-porDelito.xls, <b>se seleccionan</b> y <b>copian</b> la tabla desde "GRUPO DELICTUAL / DELITO" hasta "Robo frustrado", pasando a lo largo por todos los meses (se enumeran de 1 a 12)</li>
    <li>Se pega en <b>delitos_2017_2022.csv</b></li>
    <li>En <b>delitos_2017_2022.csv</b> las tabulaciones se reemplazan con comas (CTRL+F -> "	" reemplazar todo ",")</li>
    <li>Luego se reemplazan los meses (1 al 12) añadiendo el año correspondiente, ej: Primer "1" -> "2017_1" </li>
    <li>Revisar que no queden comas en los delitos, ej: "Lesiones menos graves, graves o gravísimas" dejarlo como "Lesiones menos graves graves o gravísimas", ya que el archivo al ser <b>.csv</b> separará la información por comas.</li>
    <li>Como último paso se borrarán algunos "Grupos delictuales" ya que solo corresponde a la suma de los delitos de cada grupo, los que no se borran a pesar de ser grupos, no tienen "sub delitos"</li>:
        <ul>
            <li>Delitos de mayor connotación social</li>
            <li>Infracción a ley de armas</li>
            <li>Incivilidades</li>        
            <li>Violencia intrafamiliar</li>
        </ul>
    </li>
</ol>