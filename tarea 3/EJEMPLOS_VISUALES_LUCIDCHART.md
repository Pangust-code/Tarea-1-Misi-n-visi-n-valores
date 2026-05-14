# Ejemplos visuales de cómo deben verse los diagramas en Lucidchart

## Objetivo
Este documento muestra una referencia visual simple para que el grupo pueda recrear en Lucidchart los diagramas que se mostrarán en el video de Pangust Systems.

---

## 1. Diagrama de datos

### Cómo debería verse
Debe verse como un diagrama limpio con cajas rectangulares para cada entidad y líneas entre ellas indicando relaciones.

### Ejemplo visual

```text
                ┌──────────────┐
                │   CLIENTE    │
                │──────────────│
                │ ID           │
                │ Nombre       │
                │ Email        │
                │ Teléfono     │
                └──────┬───────┘
                       │ 1
                       │
                       │ N
                ┌──────▼───────┐
                │    VENTA    │
                │──────────────│
                │ ID           │
                │ Fecha        │
                │ Total        │
                │ Estado       │
                └──────┬───────┘
                       │ 1
                       │
                       │ N
                ┌──────▼──────────┐
                │  DETALLE_VENTA  │
                │─────────────────│
                │ ID              │
                │ Cantidad        │
                │ Subtotal        │
                └──────┬──────────┘
                       │
                       │ N
                ┌──────▼───────┐
                │  PRODUCTO    │
                │──────────────│
                │ ID           │
                │ Nombre       │
                │ Precio       │
                │ Stock        │
                └──────────────┘

                ┌──────────────┐
                │   VENDEDOR   │
                │──────────────│
                │ ID           │
                │ Nombre       │
                │ Territorio   │
                └──────┬───────┘
                       │ 1
                       │
                       │ N
                    ┌──▼───┐
                    │VENTA │
                    └──────┘
```

### Qué debe transmitir
- El cliente compra o solicita algo.
- El vendedor registra la venta.
- La venta contiene productos.
- Todo queda organizado en datos relacionados.

### En Lucidchart
- Usa rectángulos con bordes suaves.
- Coloca la entidad principal en el centro: VENTA.
- Pon CLIENTE y VENDEDOR arriba o a los lados.
- Pon PRODUCTO abajo.
- Usa líneas con cardinalidad 1 y N si sabes agregarlas.
- Mantén mucho espacio en blanco para que no se vea saturado.

---

## 2. Arquitectura del sistema

### Cómo debería verse
Debe verse como una estructura en capas o bloques conectados de izquierda a derecha o de arriba hacia abajo.

### Ejemplo visual

```text
┌──────────────────────────┐
│        USUARIO           │
│  Vendedor / Gerente      │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│       APLICACIÓN         │
│   App móvil / Web        │
│   React Native / React   │
└────────────┬─────────────┘
             │ HTTPS
             ▼
┌──────────────────────────┐
│          API             │
│     Servidor central     │
│   Node.js / Express      │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│      BASE DE DATOS       │
│       PostgreSQL         │
│  clientes, ventas, etc.  │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│        SEGURIDAD         │
│  login, roles, backup    │
│  encriptación, auditoría │
└──────────────────────────┘
```

### Qué debe transmitir
- El usuario entra al sistema.
- La app se conecta al servidor.
- El servidor guarda información en la base de datos.
- La seguridad protege todo el proceso.

### En Lucidchart
- Usa cajas horizontales o verticales.
- Pon iconos si puedes: persona, celular, nube, base de datos, candado.
- Usa flechas claras entre bloques.
- El flujo debe ser fácil de seguir.
- No pongas demasiados detalles técnicos en el dibujo; solo lo necesario.

---

## 3. Interfaces del sistema

### Cómo debería verse
Debes mostrar pantallas simples, como si fueran bocetos o wireframes. No tienen que ser perfectas, solo claras y funcionales.

### Ejemplo visual

```text
PANTALLA 1: LOGIN
┌──────────────────────────────┐
│       PANGUST SYSTEMS        │
│                              │
│   Usuario:  [___________]    │
│   Clave:    [___________]    │
│                              │
│   [ Ingresar ]               │
└──────────────────────────────┘

PANTALLA 2: MENÚ PRINCIPAL
┌──────────────────────────────┐
│       MENÚ PRINCIPAL         │
│                              │
│   [ Nueva Venta ]            │
│   [ Clientes ]               │
│   [ Productos ]              │
│   [ Reportes ]               │
└──────────────────────────────┘

PANTALLA 3: NUEVA VENTA
┌──────────────────────────────┐
│        NUEVA VENTA           │
│                              │
│ Cliente:   [___________]     │
│ Producto:   [___________]    │
│ Cantidad:   [___________]    │
│                              │
│   [ Guardar Venta ]          │
└──────────────────────────────┘
```

### Qué debe transmitir
- El sistema debe ser fácil de usar.
- El usuario debe entender rápido qué hacer.
- Las pantallas deben ser limpias y sin saturación.
- El diseño de interfaz es parte de la etapa de diseño.

### En Lucidchart
- Usa rectángulos grandes simulando pantallas.
- Dentro coloca campos de texto, botones y títulos.
- Mantén el estilo simple, como wireframe.
- No intentes hacer una interfaz final bonita; solo una maqueta clara.

---

## 4. Cómo debe verse todo junto en el video

### Orden visual recomendado
1. Mostrar primero el diagrama de datos.
2. Luego mostrar la arquitectura del sistema.
3. Al final mostrar las interfaces.

### Secuencia visual esperada

```text
[Diagrama de datos]
        ↓
[Arquitectura del sistema]
        ↓
[Interfaces del usuario]
        ↓
[Conclusión: así resolvemos el problema]
```

### Idea de presentación
- En el video, cada diagrama debe ocupar toda la pantalla o casi toda.
- No pongas muchas cosas al mismo tiempo.
- Explica cada diagrama mientras señalas sus partes.
- Haz zoom si es necesario para que se vea bien.

---

## 5. Recomendaciones de diseño visual en Lucidchart

### Sí hacer
- Usar pocos colores.
- Mantener alineación recta.
- Poner títulos claros.
- Separar cada bloque con espacio.
- Usar flechas para guiar la vista.

### No hacer
- No llenar la hoja de elementos.
- No usar demasiados colores.
- No poner textos largos dentro de cada caja.
- No mezclar datos, arquitectura e interfaz en una sola diapositiva.

---

## 6. Regla fácil para recordar

Si el diagrama se ve así:
- claro
- ordenado
- simple
- con relaciones visibles

entonces está bien para el video.

Si se ve así:
- lleno de cosas
- confuso
- con líneas cruzadas por todos lados

entonces está mal y hay que simplificarlo.

---

## 7. Cómo explicarlo en el video

Puedes decir algo como:

> "En esta parte usamos Lucidchart para representar la solución.
> Primero mostramos el diagrama de datos, donde definimos la información del sistema.
> Luego mostramos la arquitectura, donde explicamos cómo funcionará técnicamente.
> Finalmente mostramos las interfaces, para que se vea cómo lo usará el usuario final.
> Así aplicamos la etapa de diseño al caso de Pangust Systems."

---

## 8. Resumen final

### Tu Lucidchart debería tener esta idea:
- Un diagrama de datos limpio.
- Una arquitectura por bloques y flechas.
- Una o varias pantallas simples tipo wireframe.

### El objetivo no es decorar
El objetivo es que el profesor vea que ustedes entienden cómo la etapa de diseño convierte un problema real en una solución técnica clara.
