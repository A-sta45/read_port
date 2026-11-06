# Read Port

Script simple en Python para leer datos de un puerto serial (Arduino/microcontrolador) y convertir el valor ADC recibido a voltaje.

## Qué hace

`main.py` abre el puerto serial (`COM4`, 115200 baudios) y por cada línea recibida:

- Si el dato es un número crudo, lo convierte a voltaje (rango 0–3.3V).
- Si viene en formato `ADC:valor`, extrae el valor y hace la misma conversión.
- Si ya viene como voltaje (contiene `V`) o en otro formato, lo muestra tal cual.

## Configuración

Ajusta el puerto serial en `main.py` según tu sistema (`COM4` en Windows, o algo como `/dev/ttyUSB0`/`/dev/ttyACM0` en Linux).

## Ejecución

```bash
python -m venv .venv
source .venv/bin/activate  # en Windows: .venv\Scripts\activate
pip install -r requirements.txt
python main.py
```
