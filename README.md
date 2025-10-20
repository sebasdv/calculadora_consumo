# Calculadora de Consumo Energético

Una herramienta web para calcular el consumo energético, potencia y autonomía de baterías en proyectos con microcontroladores (MCU) y sensores, especialmente diseñada para ESP32 y sistemas embebidos.

## Características

- **Cálculo de consumo energético**: Estimación precisa del consumo medio de corriente
- **Análisis de potencia**: Cálculo de potencia total en carga
- **Autonomía de batería**: Dos métodos de cálculo (Wh y mAh aproximado)
- **Múltiples componentes**: Soporte para agregar varios dispositivos y sensores
- **Duty cycle**: Consideración del ciclo de trabajo de cada componente
- **Exportación de datos**: Exportar resultados a formato CSV
- **Interfaz responsiva**: Diseño moderno y adaptable a diferentes dispositivos

## Uso

1. Abre `index.html` en tu navegador web
2. Configura los parámetros de la batería:
   - Capacidad en mAh
   - Voltaje nominal
   - Eficiencia de conversión
3. Agrega componentes y dispositivos:
   - Nombre del componente
   - Voltaje de operación
   - Corriente de consumo
   - Porcentaje de duty cycle
4. Haz clic en "Calcular" para obtener los resultados
5. Opcionalmente, exporta los datos a CSV

## Parámetros de Entrada

### Batería
- **Capacidad (mAh)**: Capacidad total de la batería en miliamperios-hora
- **Voltaje nominal (V)**: Voltaje de operación de la batería
- **Eficiencia de conversión**: Factor de eficiencia del sistema de conversión (0.5-1.0)

### Componentes
- **Nombre**: Identificación del componente o dispositivo
- **Voltaje (V)**: Voltaje de operación del componente
- **Corriente (mA)**: Consumo de corriente en miliamperios
- **Duty Cycle (%)**: Porcentaje de tiempo activo (0-100%)

## Resultados

La calculadora proporciona los siguientes valores:

- **Corriente media total**: Suma ponderada de corrientes según duty cycle
- **Potencia total en carga**: Potencia total consumida por todos los componentes
- **Energía de batería**: Energía total disponible en Wh
- **Autonomía (método Wh)**: Tiempo de funcionamiento calculado por energía
- **Autonomía (método mAh)**: Tiempo aproximado basado en capacidad de corriente

## Casos de Uso

Esta herramienta es especialmente útil para:

- Proyectos con ESP32 y sensores IoT
- Sistemas embebidos con múltiples componentes
- Estimación de autonomía en dispositivos portátiles
- Análisis de consumo en proyectos de automatización
- Planificación de sistemas alimentados por batería

## Consideraciones Técnicas

- Los resultados son estimaciones basadas en valores teóricos
- Para mediciones precisas, se recomienda usar sensores de corriente como INA219 o INA226
- La eficiencia de conversión debe ajustarse según el regulador de voltaje utilizado
- El duty cycle es crucial para componentes que no funcionan continuamente

## Tecnologías Utilizadas

- HTML5
- CSS3 (con variables CSS y diseño responsivo)
- JavaScript (ES6+)
- Sin dependencias externas

## Estructura del Proyecto

```
calculadora_consumo/
├── index.html          # Aplicación principal
└── README.md          # Documentación
```

## Contribuciones

Las contribuciones son bienvenidas. Para cambios importantes:

1. Fork del proyecto
2. Crear una rama para la nueva característica
3. Commit de los cambios
4. Push a la rama
5. Abrir un Pull Request

## Licencia

Este proyecto está disponible bajo la licencia MIT. Ver el archivo LICENSE para más detalles.

## Autor

Desarrollado por Sebastián Duarte Villanueva

## Contacto

Para preguntas o sugerencias, contacta a: sebastian.duarte@uai.cl
