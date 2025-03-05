
# Análisis de Código Java  
[Enlace al Código CCCF](https://github.com/RaulPlayo/prg1-22-23/blob/main/RETO%20CCCF/RetoCCCF.java)  

---

### **1. Nombres Incorrectos o Poco Descriptivos**  
- **Línea 2:** `RetoCCCF` → Nombre críptico (no revela propósito).  
- **Líneas 4-7:** `caja1`, `caja2`, etc. → Nombres genéricos (no indican qué almacenan).   
- **Línea 9:** `colaCero` → Confuso (cuenta minutos sin clientes).  
- **Línea 14:** `cliente` → Tipo `double` pero sugiere un objeto cliente.  

### **2. Variables No Utilizadas**  
- **Línea 15:** `compra` → Declarada pero nunca usada.  
- **Líneas 11-12:** `totalItems`, `colaTotal` → Declaradas pero no usadas.  

### **3. Lógica Estructural Incorrecta**  
- **Línea 16:** Bucle `for` procesa minutos, pero **las cajas (líneas 21-58) están fuera del bucle** → Se ejecutan una sola vez (error crítico).  

### **4. Nombres de Variables Confusos**  
- **Líneas 40,42,51,53,74:** `objetos` → Genérico y reutilizado para múltiples cajas.  

### **5. Convenciones de Java Incumplidas**  
- **Línea 3:** Clase `main` con toda la lógica → Debería dividirse en métodos.  
- **Líneas 21-83:** Código repetitivo para cajas → Falta de modularidad.  

### **6. Errores de Semántica**  
- **Línea 90:** `entrada.nextLine()` → Detiene la simulación hasta que el usuario presione Enter (¿intencional?).  

---

[Enlace al Código whacAMole](https://github.com/RaulPlayo/prg1-22-23/blob/main/retos/entregas/WhacAMole/whacAMole.java)  


### **1. Nombres Poco Descriptivos**  
- **Línea 3:** `whacAMole` → No sigue **CamelCase** (debería ser `WhacAMole`).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L3)
- **Línea 9:** `monigote`, `monigote1` → Nombres en español y no revelan su propósito (deberían ser `molePosition1`, `molePosition2`). (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L9)
- **Línea 4:** `dimension` → No indica que representa el tamaño del tablero (mejor `gridSize`).  

### **2. Variables con Nombres Confusos**  
- **Línea 10:** `contador` → Usado para numerar celdas, pero su nombre no lo refleja (mejor `currentCell`).  
- **Línea 8:** `casilla` → Ambigüedad (¿casilla seleccionada? ¿casilla actual?).  

### **3. Números sin constantes**  
- **Línea 20:** `100` → Valor arbitrario en `Math.random() * 100` (debería usarse `16` directamente).  
- **Línea 4:** `4` → Tamaño del tablero "hardcodeado" ( consiste en incluir valores específicos directamente en el código en lugar de utilizar variables o funciones para obtenerlos de forma dinámica) (debería ser `final int GRID_SIZE = 4;`).  

### **4. Lógica Redundante**  
- **Líneas 29 y 35:**  
  - Código duplicado para verificar `monigote` y `monigote1` (debería usarse un array o método).  

### **5. Validación de Entrada Incorrecta**  
- **Líneas 19-22:**  
  - El `do-while` permite `casilla = 0` (inválido). La condición debe ser `casilla < 1 || casilla > 16`.  

### **6. Sesgo en Generación de Números Aleatorios**  
- **Líneas 18-20:**  
  - `(Math.random() * 100) % 16` genera distribución no uniforme (mejor `new Random().nextInt(16) + 1`).  

### **7. Inconsistencia en Idioma**  
- **Variables en español** (`turno`, `acierto`, `casilla`) en un contexto de código que debería ser en inglés (estándar en Java).  

---

## **Problemas de Diseño**  
- **Clase monolítica:** Toda la lógica está en `main`, sin métodos auxiliares (ej. `generateMolePosition()`).  
- **Falta de encapsulación:** Variables como `acierto` o `turno` podrían ser parte de un objeto `Juego`.  
- **Efectos laterales no documentados:** Modificación simultánea de `contador`, `monigote`, y `acierto` sin claridad.  

---



