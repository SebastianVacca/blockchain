# Blockchain Básico con Flask
 
Este proyecto implementa una aplicación básica de blockchain descentralizado utilizando Python y Flask. Permite simular transacciones, minar bloques y consultar la cadena de bloques a través de una API REST.
 
---
 
## Características principales
- Crear un blockchain básico con bloques, transacciones y prueba de trabajo.
- Minar nuevos bloques para agregar transacciones a la cadena.
- Consultar la cadena de bloques completa.
- API REST para interactuar con el blockchain.
 
---
 
## Requisitos previos
1. **Python**: Versión 3.7 o superior.
2. **Bibliotecas necesarias**:
   - Flask
   - Werkzeug
 
---
 
## Instalación
1. Clona este repositorio o descarga el código fuente.
2. Asegúrate de tener Python instalado en tu sistema.
3. Instala las dependencias utilizando `pip`:
 
```bash
pip install -r requirements.txt
```
 
Si no tienes un archivo `requirements.txt`, instala Flask manualmente:
 
```bash
pip install flask werkzeug
```
 
---
 
## Uso
 
### 1. Iniciar el servidor
Ejecuta el siguiente comando para iniciar el servidor Flask:
 
```bash
python app.py
```
 
### 2. Endpoints disponibles
 
#### **Consultar la cadena de bloques**
- **Método**: `GET`
- **URL**: `/chain`
- **Descripción**: Devuelve la cadena completa de bloques.
- **Ejemplo**:
  ```
http://127.0.0.1:5000/chain
  ```
 
#### **Crear una nueva transacción**
- **Método**: `POST`
- **URL**: `/transactions/new`
- **Descripción**: Crea una nueva transacción en el blockchain.
- **Cuerpo de la solicitud**:
  ```json
  {
    "sender": "address1",
    "recipient": "address2",
    "amount": 10
  }
  ```
- **Ejemplo**:
  ```
  curl -X POST -H "Content-Type: application/json" -d '{"sender": "address1", "recipient": "address2", "amount": 10}' http://127.0.0.1:5000/transactions/new
  ```
 
#### **Minar un bloque**
- **Método**: `GET`
- **URL**: `/mine`
- **Descripción**: Ejecuta la prueba de trabajo y crea un nuevo bloque en la cadena.
- **Ejemplo**:
  ```
http://127.0.0.1:5000/mine
  ```
 
---
 
## Estructura del proyecto
```plaintext
|-- blockchain.py    # Lógica del blockchain
|-- app.py           # Servidor Flask con API REST
|-- requirements.txt # Dependencias necesarias
```
 

 
