Sistema de Guía de Apoyo para Drones
Trabajo Práctico Integrador · Algoritmos y Estructuras de Datos
UTN Facultad Regional Buenos Aires (UTN FRBA) · Curso K1054 · Año 2026

📋 Descripción del Proyecto
Este sistema en C++ (C++17) modela, valida y simula rutas de navegación y operaciones tácticas para drones sobre un tablero de 200 x 200 celdas. El programa procesa archivos binarios estructurados que contienen los comandos de vuelo, asegurando que las trayectorias cumplan estrictamente con las reglas de adyacencia ortogonal, restricciones operativas (despegues únicos, exclusividad de aterrizaje o kamikaze) y control de integridad de los datos.

👥 Integrantes del Equipo
Santillan, Agustin (Legajo: 232.765-0) — Estructuras de datos y entrada/salida binaria (ops. 1 y 6) + Repositorio 
Perrotta, Pilar (Legajo: 234.929-2) — Función de validación y recorrido de la ruta
Dejo, Guillermo (Legajo: 235.392-1) — Menú principal y opción 2 (paginación y mapa)
Monge, Facundo Martin (Legajo: 150.932-9) — Opciones 3, 4 y 5 + Probador aleatorio y capturas

🛠️ Tecnologías y Entorno
Lenguaje: C++ (C++17)
Compilación: main.cpp -> main.exe
Control de Versiones: Git / GitHub
Visualización de Pruebas: Informe Visual de Pruebas en Netlify

📏 Criterios de Validación Aplicados
El motor de validación implementado evalúa rigurosamente los siguientes aspectos lógicos:
Contenido mínimo: El archivo binario debe poseer al menos un registro.
Límites espaciales: Las coordenadas (X, Y) deben encontrarse estrictamente en el rango [0, 199].
Unicidad: No se permite repetir una coordenada dentro de la misma ruta.
Despegue único: Debe existir exactamente una instrucción de despegue.
Independencia de despegue: La celda de despegue no puede contener órdenes adicionales.
Fin excluyente: La misión debe terminar con exactamente 1 aterrizaje (sin kamikaze) o 1 ataque kamikaze (sin aterrizaje).
Adyacencia y tránsito: Cada salto subsiguiente debe realizarse hacia una celda ortogonal adyacente (arriba, abajo, izquierda, derecha), previamente ocupada y no visitada.
Punto terminal: La ruta debe finalizar correctamente en la celda de aterrizaje o kamikaze designada.
Cohesión de ruta: La secuencia debe cubrir todos los registros sin dejar celdas colgadas o desconectadas.

🚀 Compilación y Ejecución
Para compilar y ejecutar el proyecto localmente mediante un compilador compatible con C++17:
g++ -std=c++17 main.cpp -o main.exe
./main.exe

🔗 Enlaces de Interés 
Repositorio Oficial: https://github.com/asantillan-utn/TP-AyED-Drones
Tablero de Pruebas Interactivo: https://github-step-report.netlify.app

