
# Análisis de Código Java  
[Enlace al Código CCCF](https://github.com/RaulPlayo/prg1-22-23/blob/main/RETO%20CCCF/RetoCCCF.java)  

---

### **1. Nombres Incorrectos o Poco Descriptivos**  
- **Línea 2:** `RetoCCCF` → Nombre críptico (no revela propósito).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L2)
- **Líneas 5-9:** `caja1`, `caja2`, etc. → Nombres genéricos (no indican qué almacenan).   (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L5)
- **Línea 10:** `colaCero` → Confuso (cuenta minutos sin clientes).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L10)
- **Línea 14:** `cliente` → Tipo `double` pero sugiere un objeto cliente.  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L14)

### **2. Variables No Utilizadas**  
- **Línea 15:** `compra` → Declarada pero nunca usada.  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L15)
- **Líneas 11-12:** `totalItems`, `colaTotal` → Declaradas pero no usadas.  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L12)

### **3. Lógica Estructural Incorrecta**  
- **Línea 16:** Bucle `for` procesa minutos, pero **las cajas (líneas 21-58) están fuera del bucle** → Se ejecutan una sola vez (error crítico).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L16)

### **4. Nombres de Variables Confusos**  
- **Líneas 40,42,51,53,74:** `objetos` → Genérico y reutilizado para múltiples cajas.  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L40)(https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L42)https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L51)

### **5. Convenciones de Java Incumplidas**  
- **Línea 3:** Clase `main` con toda la lógica → Debería dividirse en métodos.  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L3)
- **Líneas 21-83:** Código repetitivo para cajas → Falta de modularidad.  

### **6. Errores de Semántica**  
- **Línea 90:** `entrada.nextLine()` → Detiene la simulación hasta que el usuario presione Enter (¿intencional?).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/RETO%20CCCF/RetoCCCF.java#L90)

---

[Enlace al Código whacAMole](https://github.com/RaulPlayo/prg1-22-23/blob/main/retos/entregas/WhacAMole/whacAMole.java)  


### **1. Nombres Poco Descriptivos**  
- **Línea 3:** `whacAMole` → No sigue **CamelCase** (debería ser `WhacAMole`).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L3)
- **Línea 9:** `monigote`, `monigote1` → Nombres en español y no revelan su propósito (deberían ser `molePosition1`, `molePosition2`). (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L9)
- **Línea 4:** `dimension` → No indica que representa el tamaño del tablero (mejor `gridSize`). (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L4) 

### **2. Variables con Nombres Confusos**  
- **Línea 10:** `contador` → Usado para numerar celdas, pero su nombre no lo refleja (mejor `currentCell`).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L10)
- **Línea 8:** `casilla` → Ambigüedad (¿casilla seleccionada? ¿casilla actual?).   (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L8)

### **3. Números sin constantes**  
- **Línea 20:** `100` → Valor arbitrario en `Math.random() * 100` (debería usarse `16` directamente). (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L20)  
- **Línea 5:** `4` → Tamaño del tablero "hardcodeado" ( consiste en incluir valores específicos directamente en el código en lugar de utilizar variables o funciones para obtenerlos de forma dinámica) (debería ser `final int GRID_SIZE = 4;`).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L5)

### **4. Lógica Redundante**  
- **Líneas 29 y 35:**  
  - Código duplicado para verificar `monigote` y `monigote1` (debería usarse un array o método). (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L29) 

### **5. Validación de Entrada Incorrecta**  
- **Líneas 19-22:**  
  - El `do-while` permite `casilla = 0` (inválido). La condición debe ser `casilla < 1 || casilla > 16`. (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L19) 

### **6. Sesgo en Generación de Números Aleatorios**  
- **Líneas 18-20:**  
  - `(Math.random() * 100) % 16` genera distribución no uniforme (mejor `new Random().nextInt(16) + 1`).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L18)

### **7. Inconsistencia en Idioma**  
- **Variables en español** (`turno`, `acierto`, `casilla`) en un contexto de código que debería ser en inglés (estándar en Java).  (https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L6)(https://github.com/RaulPlayo/prg1-22-23/blob/e4b923764dab705734184aeb66b77f8b94f033cd/retos/entregas/WhacAMole/whacAMole.java#L7)

---

## **Problemas de Diseño**  
- **Clase monolítica:** Toda la lógica está en `main`, sin métodos auxiliares (ej. `generateMolePosition()`).  
- **Falta de encapsulación:** Variables como `acierto` o `turno` podrían ser parte de un objeto `Juego`.  
- **Efectos laterales no documentados:** Modificación simultánea de `contador`, `monigote`, y `acierto` sin claridad.  

---



