# Laboratorio: Minimax y Poda Alfa-Beta

## Descripción
Este proyecto implementa los algoritmos Minimax y Poda Alfa-Beta para resolver un árbol de decisión simplificado.

## Objetivo
Comparar el resultado y la eficiencia de Minimax frente a Poda Alfa-Beta.

## Instalación
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Ejecución
```bash
python -m src.main
```

## Pruebas
```bash
pytest --cov=src --cov-report=term-missing
```

## Preguntas de análisis

1. ¿Por qué Minimax y Alfa-Beta devuelven el mismo valor?
Porque ambos algoritmos buscan la mejor decisión posible dentro del árbol de juego. La diferencia es que Alfa-Beta evita explorar ramas que no afectan el resultado final, pero mantiene la misma decisión que obtendría Minimax.

2. ¿Cuándo Alfa-Beta reduce más nodos?
Alfa-Beta reduce más nodos cuando las mejores jugadas se evalúan primero. Esto permite identificar antes las ramas que no influirán en la decisión final y descartarlas sin explorarlas completamente.

3. ¿Qué ocurre si el árbol está mal ordenado?
Si el árbol está mal ordenado, Alfa-Beta realiza menos podas y debe evaluar una mayor cantidad de nodos. Aunque el resultado final sigue siendo correcto, el algoritmo pierde eficiencia.

4. ¿Cómo se aplicaría este algoritmo en ajedrez, damas o tres en raya?
Este algoritmo se utiliza para analizar las posibles jugadas de ambos jugadores y seleccionar la mejor opción disponible. Evalúa diferentes escenarios futuros asumiendo que el oponente también tomará decisiones óptimas, permitiendo al agente elegir la jugada más conveniente.