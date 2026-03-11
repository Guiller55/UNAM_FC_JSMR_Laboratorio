# Linear Regression Toolkit 📊
[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📖 Descripción
Este módulo proporciona herramientas robustas para el cálculo de regresiones lineales simples y estimaciones masivas. Desarrollado para la clase de Inteligencia Artificial, enfocado en código limpio, manejo de excepciones y logging profesional.

## 🚀 Características
- **Cálculo de Regresión:** Obtención de intercepto ($a$) y pendiente ($b$) mediante mínimos cuadrados.
- **Validación Automática:** Manejo de errores para dimensiones incompatibles o varianza cero.
- **Logging Integrado:** Registro de eventos para auditoría de modelos.
- **Type Hinting:** Código totalmente tipado para una mejor experiencia de desarrollo (DX).

## 🛠️ Instalación
Para usar esta biblioteca, clona el repositorio y asegúrate de tener las dependencias necesarias:

```bash
git clone [https://github.com/tu-usuario/nombre-repositorio.git](https://github.com/tu-usuario/nombre-repositorio.git)
cd nombre-repositorio
pip install -r requirements.txt
```

## Seudocógido de A*
```txt
ALGORITMO A_ESTRELLA(grafo, heuristicas, inicio, meta)

    // Inicializar cola de prioridad (f_total, g_acumulado, nodo_actual, camino)
    pq <- NUEVA_COLA_PRIORIDAD()
    f_inicial <- heuristicas[inicio]
    INSERTAR en pq (f_inicial, 0, inicio, [inicio])

    // Diccionario para almacenar el menor costo g encontrado para cada nodo
    visitados <- NUEVO_DICCIONARIO()

    MIENTRAS pq NO ESTÉ VACÍA:
        // Extraer el nodo con el menor f (costo estimado total)
        (f, g, nodo, camino) <- POP_MIN(pq)

        // Si llegamos al objetivo, terminamos
        SI nodo == meta ENTONCES:
            RETORNAR camino, g

        // Si el nodo no se ha visitado o encontramos un camino más corto (menor g)
        SI nodo NO EN visitados O g < visitados[nodo] ENTONCES:
            visitados[nodo] <- g

            // Explorar los vecinos del nodo actual
            PARA CADA (vecino, costo_arista) EN grafo[nodo]:
                nuevo_g <- g + costo_arista
                nuevo_f <- nuevo_g + heuristicas[vecino]
                nuevo_camino <- camino + [vecino]
                
                // Añadir a la cola de prioridad para evaluar después
                INSERTAR en pq (nuevo_f, nuevo_g, vecino, nuevo_camino)

    // Si la cola se vacía y no se llega a la meta
    RETORNAR Nulo, Infinito
FIN ALGORITMO
```

## ⚖️ Licencia

Este proyecto está bajo la Licencia MIT.

Consulta el archivo LICENSE para más detalles