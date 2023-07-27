# Text-Mining-and-Image-recognition
Tercer trimestre. 
# Problema No.5 (Laboratorio 1) 
# Espacio de Color HSV

## Introducción

El espacio de color HSV (Hue, Saturation, Value) es un modelo de representación de colores que se basa en tres componentes principales:

1. **Matiz (Hue)**: Representa el tipo de color, como rojo, verde, azul, etc. El matiz se mide en grados, formando un círculo cromático de 360°, donde el rojo está en 0°, el verde en 120° y el azul en 240°, entre otros colores. El matiz determina la dominancia espectral del color.

2. **Saturación (Saturation)**: Representa la intensidad o pureza del color. Se mide como un porcentaje que va desde 0% (gris) hasta 100% (color puro y brillante). Una saturación baja se traduce en colores más apagados, mientras que una saturación alta resulta en colores más intensos y vivos.

3. **Valor (Value)**: Representa el brillo o la luminosidad del color. También se mide como un porcentaje, donde 0% es totalmente oscuro (negro) y 100% es el brillo máximo del color.

El espacio de color HSV es muy útil en aplicaciones gráficas, diseño de imágenes y procesamiento de colores, ya que permite manipular fácilmente los atributos del color sin tener que trabajar directamente con la representación en el espacio de color RGB (Rojo, Verde, Azul).

## Mapeo de Colores al Espacio de Color HSV

El mapeo de colores al espacio de color HSV se realiza a través de una conversión desde el espacio de color RGB. El espacio de color RGB se basa en la combinación de los tres colores primarios: rojo, verde y azul, en diferentes intensidades para formar el espectro completo de colores. Sin embargo, en el espacio de color HSV, los colores se describen mediante el matiz, la saturación y el valor, lo que permite trabajar con ellos de una manera más intuitiva.

La conversión desde RGB a HSV se realiza mediante las siguientes fórmulas:

1. Para obtener el matiz (H):
   - Si el valor máximo entre R, G y B es R, entonces H = (G-B)/(Vmin-Vmax) si G ≥ B, o H = (G-B)/(Vmin-Vmax) + 6 si G < B.
   - Si el valor máximo entre R, G y B es G, entonces H = 2.0 + (B-R)/(Vmin-Vmax).
   - Si el valor máximo entre R, G y B es B, entonces H = 4.0 + (R-G)/(Vmin-Vmax).

2. Para obtener la saturación (S):
   - S = (Vmax - Vmin) / Vmax, donde Vmax es el valor máximo entre R, G y B, y Vmin es el valor mínimo.

3. Para obtener el valor (V):
   - V = Vmax, donde Vmax es el valor máximo entre R, G y B.

Es importante tener en cuenta que algunas implementaciones pueden normalizar los valores de H, S y V en rangos específicos, como por ejemplo H en el rango [0, 360], S en el rango [0, 1] y V en el rango [0, 1].

En resumen, el espacio de color HSV proporciona una representación más intuitiva y fácil de manipular para los colores, lo que lo convierte en una herramienta valiosa en diversas aplicaciones relacionadas con el procesamiento y manipulación de imágenes.
