```mermaid
classDiagram
    class Cine {
        +nombre
    }

    class Sala {
        +numero
        +cantidadAsientos
        +tipo: String <<HD/3D/4D>>
    }

    class Pelicula {
        +titulo
        +genero
        +clasificacion
    }

    class Director {
        +nombre
        +apellido
    }

    class Protagonista {
        +nombre
        +apellido
    }

    class Personaje {
        +nombre
    }

    class Pase {
        +fecha
        +hora
        +turno <<Mañana/Tarde/Noche/Trasnoche>>
    }

    class Precio {
        +turno
        +valor
    }

    class Entrada {
        +asiento
        +fecha
        +turno
    }

    class Persona {
        +nombre
        +apellido
    }

    Cine --> Sala
    Cine --> Precio
    Sala --> Pase
    Pase --> Pelicula
    Pelicula --> Director
    Pelicula --> Protagonista
    Protagonista --> Personaje
    Entrada --> Sala
    Entrada --> Pelicula
    Entrada --> Persona
