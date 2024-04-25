# DESCRIPCION DEL PROYECTO: 

* En este proyecto se va abarcar clases, categoria de carros,autos, autospersona, persona, lo cual haremos una simplificación a que una persona puede tener varios autos, una marca de auto puede tener un solo dueño

# Categoria de Carros: 

* sedán 
* deportivo
* economico
* electrico

# Autos: 

* Chevrolet Spark
* Mazda 3
* Toyota Tundra 4x4
* Honda civic
* subaru 

# Rf:
* El chevrolet Spark es un carro super economico en gasolina 

# AutoPersona

* Llantas
* Motor
* Espejos 
* Baúl

# Rf Autos: 

* Los atributos de AutoPersona conforman a un atributo de Autos

# Rf Persona: 

* Acá Personas pueden hacer uso de estos atributos de AutoPersona, el baúl por ejemplo sirve para guardar cosas que ya no nos caben en la cabina principal
* Los espejos principales del carro nos sirve para mirar a los lados para prevenir accidentes

# Persona: 

* dueño
* vendedor
* comercializadora responsable
* fabricante de autos 

# 3. MR.wsd: 

#  Cambios realizados:

* Se ha agregado una sección de "Descripción del proyecto" que detalla los objetivos y el alcance del proyecto

* Se ha agregado una categoria de carros, la cual tiene  atributos 

* Se ha agregado una sección de autos la cual tiene 6 atributos, la cual también tiene una referencia sobre categoria autos 

* Se ha agregado una sección de Autos persona, tiene 4 atributos, y tiene 2 referencias, 1 referencia con autos y otra referencia con persona

* Se ha agregado una seccion de Personas, tiene 4 atributos. 

# 4. Script.SQL: 

* CREATE TABLE Categoria_Carros(
* idCategoria_Carros PRIMARY KEY,
   sedán (varchar50),
   deportivo (varchar50),
  economico (varchar50),
  electrico (varchar50)
);

* CREATE TABLE Autos(
    idAutos PRIMARY KEY
    Chevrolet Spark (nvarchar40),
    Mazda 3 (nvarchar40),
    Toyota Tundra 4x4 (nvarchar40),
    Honda civic (nvarchar40),
    subaru (nvarchar40),
    
    (
        ref idAutos -> idCategoria_carros
    )
);


* CREATE TABLE AutoPersona(
    idAutoPersona PRIMARY KEY
    Llantas (varchar30),
    Motor   (varchar60),
    Espejos (varchar30),
    Baúl    (varchar50),
   
    (
     ref idAutoPersona-> idAutos
     ref id AutoPersona-> idPErsonas
    )
);

* CREATE TABLE Persona (
    idPersona PRIMARY KEY
    dueño  (varchar50),
    vendedor(varchar50),
    comercializadora responsable (varchar40),
    fabricante de autos (varchar45),
);