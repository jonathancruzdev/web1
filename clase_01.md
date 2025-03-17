
# Introducción a  p5.js

## 📌 Funciones setup() y draw()
Estas funciones son esenciales en p5.js. `setup()` se ejecuta una sola vez al inicio, mientras que `draw()` se ejecuta en un bucle.
```javascript
function setup() {
  createCanvas(400, 400); // Crea un lienzo de 400x400 píxeles
}

function draw() {
  background(220); // Establece un fondo gris claro
  ellipse(200, 200, 100, 100); // Dibuja un círculo en el centro
}
```

## 📌 Funciones Básicas
### **createCanvas(ancho, alto)**
Define el tamaño del lienzo donde se dibujará.
```javascript
function setup() {
  createCanvas(500, 300); // Crea un lienzo de 500x300 píxeles
}
```

### **background(color)**
Establece el color de fondo del lienzo.
```javascript
function draw() {
  background(100, 150, 255); // Fondo azul claro
}
```

## 📌 El Canvas y Sistema de Coordenadas
El sistema de coordenadas en p5.js tiene su origen (0,0) en la esquina superior izquierda.
```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  line(0, 200, 400, 200); // Línea horizontal en Y=200
  line(200, 0, 200, 400); // Línea vertical en X=200
}
```

## 📌 Figuras Primitivas
### **point(x, y)**
Dibuja un punto en la posición especificada.
```javascript
function draw() {
  background(220);
  point(200, 200); // Dibuja un punto en el centro
}
```

### **line(x1, y1, x2, y2)**
Dibuja una línea entre dos puntos.
```javascript
function draw() {
  background(220);
  //line(x1, y1, x2, y2)
  line(50, 50, 350, 350); // Línea diagonal
}
```

### **rect(x, y, ancho, alto)**
Dibuja un rectángulo en la posición dada.
```javascript
function draw() {
  background(220);
  rect(150, 150, 100, 50); // Rectángulo
}
```

### **square(x, y, lado)**
Dibuja un cuadrado en la posición dada.
```javascript
function draw() {
  background(220);
  square(150, 150, 100); // Cuadrado
}
```

### **circle(x, y, radio)**
Dibuja un círculo con el centro en (x, y) y el diámetro dado.
```javascript
function draw() {
  background(220);
  circle(200, 200, 100); // Círculo en el centro
}
```

### **ellipse(x, y, ancho, alto)**
Dibuja una elipse con el centro en (x, y) y los tamaños especificados.
```javascript
function draw() {
  background(220);
  ellipse(200, 200, 150, 100); // Elipse horizontal
}
```

### **triangle(x1, y1, x2, y2, x3, y3)**
Dibuja un triángulo con los tres vértices especificados.
```javascript
function draw() {
  background(220);
  triangle(200, 100, 150, 300, 250, 300); // Triángulo
}
```

### **arc(x, y, ancho, alto, inicio, fin)**
Dibuja un arco entre dos ángulos especificados en radianes.
```javascript
function draw() {
  background(220);
  arc(200, 200, 100, 100, 0, PI); // Arco semicircular
}
```

## 📌 Figuras Personalizadas
Permiten dibujar formas más complejas utilizando vértices.
```javascript
function draw() {
  background(220);
  beginShape();
  vertex(100, 100);
  vertex(300, 100);
  vertex(200, 300);
  endShape(CLOSE); // Dibuja un triángulo personalizado
}
```

## 📌 Configuraciones de Dibujo
### **fill(color)**
Establece el color de relleno para las figuras.
```javascript
function draw() {
  background(220);
  fill(255, 0, 0); // Relleno rojo
  rect(100, 100, 200, 200);
}
```

### **stroke(color)**
Define el color del contorno de las figuras.
```javascript
function draw() {
  background(220);
  stroke(0, 255, 0); // Borde verde
  strokeWeight(5); // Grosor del borde
  rect(100, 100, 200, 200);
}
```

### **strokeWeight(pixels)**
Especifica el grosor de las líneas y bordes.
```javascript
function draw() {
  background(220);
  strokeWeight(10); // Línea gruesa
  line(100, 100, 300, 300);
}
```

### **noStroke()**
Elimina los bordes de las figuras.
```javascript
function draw() {
  background(220);
  noStroke();
  rect(100, 100, 200, 200);
}
```

### **noFill()**
Hace que las figuras sean transparentes (solo el contorno visible).
```javascript
function draw() {
  background(220);
  noFill();
  ellipse(200, 200, 150, 100);
}
```

## 📌 Transformaciones y Modos de Dibujo
### **push() y pop()**
Guardan y restauran configuraciones de dibujo.
```javascript
function draw() {
  background(220);
  push(); 
  fill(255, 0, 0);
  rect(100, 100, 100, 100); // Rojo
  pop();
  rect(200, 100, 100, 100); // Sin relleno rojo
}
```

### **rectMode(CENTER)**
Cambia el modo de referencia del rectángulo al centro.
```javascript
function setup() {
  createCanvas(400, 400);
  rectMode(CENTER);
}
function draw() {
  background(220);
  rect(200, 200, 100, 50);
}
```

### **random()**
Genera valores aleatorios en un rango.
```javascript
function draw() {
  background(220);
  let x = random(400);
  let y = random(400);
  ellipse(x, y, 20, 20);
}
```
```
