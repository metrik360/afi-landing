# MÉTRIK Design System - AFI International Group

**Proyecto:** Landing Page (Brochure Digital)
**Basado en:** REQUIREMENTS_DOC.md + Manual Corporativo de Marca AFI
**Fecha:** 14/01/2026

---

## 1. IDENTIDAD VISUAL

### 1.1 Logo

**Archivo principal:**
- URL: `https://i.ibb.co/jZzy6pD6/descarga-2-e1759514991690-png-2.webp`
- Local: `/marca/descarga-2-e1759514991690.png-2.webp`

**Posición en landing:** Header izquierda (fijo)
**Tamaño recomendado:** 150px de ancho (mantiene aspect ratio)

**Descripción del imagotipo:**
- Líneas ascendentes multicolor que representan diversidad de soluciones
- Colores simbolizan evolución, innovación controlada y enfoque integral

---

### 1.2 Paleta de Colores Corporativos

#### Colores Principales (del Manual de Marca)

| Color | HEX | RGB | Uso | Significado |
|-------|-----|-----|-----|-------------|
| **Rojo AFI Principal** | `#CE114E` | 206, 17, 78 | Color institucional dominante | Riesgo, control, alerta, liderazgo |
| **Rojo Secundario** | `#EA1D1C` | 234, 29, 28 | Acentos estratégicos | Acción, firmeza |
| **Dorado Estratégico** | `#CD981E` | 205, 152, 30 | Detalles premium | Valor, experiencia, prestigio |
| **Azul Gris Institucional** | `#5C8891` | 92, 136, 145 | Apoyo visual, fondos | Estabilidad, análisis |
| **Negro Corporativo** | `#0C0D0C` | 12, 13, 12 | Tipografía, contraste | Rigor técnico, formalidad |
| **Blanco Institucional** | `#FDFDFD` | 253, 253, 253 | Fondos, limpieza visual | Transparencia, claridad |

#### Colores del Imagotipo (Acentos)

| Color | Uso | Significado |
|-------|-----|-------------|
| **Azul Corporativo** | Headers, títulos | Confianza, profesionalismo, seguridad jurídica |
| **Verde Estratégico** | Cumplimiento, control | Prevención, sostenibilidad |
| **Naranja Dinámico** | CTAs, alertas | Acción, análisis, alerta temprana |
| **Morado Técnico** | Servicios especializados | Conocimiento, auditoría forense |

#### Paleta para Landing (Aplicación Web)

```css
:root {
  /* Primarios */
  --color-primary: #CE114E;        /* Rojo AFI - CTAs, highlights */
  --color-primary-dark: #A00D3D;   /* Hover states */
  --color-secondary: #0A1628;      /* Azul oscuro - Headers, textos */

  /* Acentos del imagotipo */
  --color-accent-gold: #CD981E;    /* Detalles premium */
  --color-accent-blue: #5C8891;    /* Elementos secundarios */

  /* Fondos */
  --color-bg-primary: #FDFDFD;     /* Fondo principal */
  --color-bg-secondary: #F5F7FA;   /* Secciones alternas */
  --color-bg-dark: #0A1628;        /* Secciones oscuras (hero, CTA) */

  /* Textos */
  --color-text-primary: #0C0D0C;   /* Texto principal */
  --color-text-secondary: #5C8891; /* Texto secundario */
  --color-text-light: #FDFDFD;     /* Texto sobre fondos oscuros */

  /* Bordes y líneas */
  --color-border: #E5E7EB;
  --color-border-light: #F0F0F0;
}
```

---

### 1.3 Tipografía

#### Fuentes Principales (del Manual)

| Tipo | Fuente | Uso |
|------|--------|-----|
| **Principal** | Montserrat | Títulos, encabezados, piezas gráficas |
| **Secundaria** | Open Sans | Textos largos, documentos, body |

#### Implementación Google Fonts

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&family=Open+Sans:wght@400;500;600&display=swap" rel="stylesheet">
```

#### Jerarquía Tipográfica

```css
/* Títulos - Montserrat */
h1 { font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 48px; }
h2 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 36px; }
h3 { font-family: 'Montserrat', sans-serif; font-weight: 600; font-size: 24px; }
h4 { font-family: 'Montserrat', sans-serif; font-weight: 600; font-size: 20px; }

/* Body - Open Sans */
body { font-family: 'Open Sans', sans-serif; font-weight: 400; font-size: 16px; }
.lead { font-family: 'Open Sans', sans-serif; font-weight: 400; font-size: 18px; }
.small { font-family: 'Open Sans', sans-serif; font-weight: 400; font-size: 14px; }
```

---

## 2. ESTRUCTURA DE LA LANDING

### 2.1 Secciones (8 en total)

```
┌─────────────────────────────────────────────────────────────┐
│ 1. HERO                                                      │
│    - Fondo oscuro (#0A1628)                                  │
│    - Logo + Headline + CTAs                                  │
├─────────────────────────────────────────────────────────────┤
│ 2. PROBLEMA/CONTEXTO                                         │
│    - Fondo claro (#FDFDFD)                                   │
│    - ¿Obligado a implementar SARLAFT?                        │
├─────────────────────────────────────────────────────────────┤
│ 3. SERVICIOS                                                 │
│    - Fondo gris claro (#F5F7FA)                              │
│    - 6 cards de servicios                                    │
├─────────────────────────────────────────────────────────────┤
│ 4. ¿POR QUÉ AFI?                                             │
│    - Fondo claro (#FDFDFD)                                   │
│    - Diferenciadores: Velocidad, Confiabilidad               │
├─────────────────────────────────────────────────────────────┤
│ 5. CLIENTES                                                  │
│    - Fondo gris claro (#F5F7FA)                              │
│    - Grid de logos                                           │
├─────────────────────────────────────────────────────────────┤
│ 6. ALIADO (MéTRIK)                                           │
│    - Fondo claro (#FDFDFD)                                   │
│    - Logo + descripción + beneficios                         │
├─────────────────────────────────────────────────────────────┤
│ 7. CTA FINAL                                                 │
│    - Fondo oscuro (#0A1628)                                  │
│    - Llamado a la acción + botones                           │
├─────────────────────────────────────────────────────────────┤
│ 8. FOOTER                                                    │
│    - Fondo muy oscuro (#050A12)                              │
│    - Contacto + Powered by MéTRIK                            │
└─────────────────────────────────────────────────────────────┘
```

---

## 3. MOCKUPS ASCII

### 3.1 Sección 1: HERO

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ ████████████████████████████ FONDO OSCURO #0A1628 ██████████████████████████│
│                                                                             │
│  [LOGO AFI]                                                                 │
│                                                                             │
│   ┌───────────────────────────────┐  ┌─────────────────────────────────┐   │
│   │                               │  │                                 │   │
│   │  "Fortalecemos la confianza   │  │    [IMAGEN OFICINA PROFESIONAL] │   │
│   │        empresarial"           │  │                                 │   │
│   │                               │  │    Unsplash: oficina moderna    │   │
│   │  Implementación integral de   │  │    con ambiente corporativo    │   │
│   │  sistemas de cumplimiento     │  │                                 │   │
│   │                               │  │                                 │   │
│   │  SAGRILAFT | SARLAFT | PTEE   │  │                                 │   │
│   │                               │  │                                 │   │
│   │  ┌────────────┐ ┌───────────┐ │  │                                 │   │
│   │  │📅 Agendar  │ │💬WhatsApp │ │  │                                 │   │
│   │  │  llamada   │ │           │ │  │                                 │   │
│   │  └────────────┘ └───────────┘ │  │                                 │   │
│   │   (Rojo #CE114E) (Borde bco)  │  │                                 │   │
│   └───────────────────────────────┘  └─────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Especificaciones Hero:**
- Altura: 100vh (viewport completo)
- Layout: 2 columnas (50% texto / 50% imagen)
- Imagen: `https://images.unsplash.com/photo-1497366216548-37526070297c` (oficina profesional)
- CTA primario: Fondo rojo `#CE114E`, texto blanco
- CTA secundario: Transparente con borde blanco
- Imagen con border-radius en esquinas y leve sombra

---

### 3.2 Sección 2: PROBLEMA/CONTEXTO

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ ███████████████████████████ FONDO CLARO #FDFDFD ████████████████████████████│
│                                                                             │
│                    ¿Tu empresa está obligada a                              │
│                    implementar SARLAFT?                                     │
│                                                                             │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │                                                                     │   │
│  │   El incumplimiento normativo puede generar:                        │   │
│  │                                                                     │   │
│  │   ⚠️ Sanciones económicas significativas                           │   │
│  │   ⚠️ Riesgos legales y reputacionales                              │   │
│  │   ⚠️ Pérdida de credibilidad ante stakeholders                     │   │
│  │   ⚠️ Exposición a lavado de activos y fraude                       │   │
│  │                                                                     │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│                    AFI International Group es tu aliado                     │
│                    estratégico en cumplimiento normativo                    │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Especificaciones:**
- Padding: 80px vertical
- Título: Montserrat 36px Bold, color `#0C0D0C`
- Lista de riesgos: Open Sans 18px, íconos en `#CE114E`

---

### 3.3 Sección 3: SERVICIOS

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ █████████████████████████ FONDO GRIS #F5F7FA ███████████████████████████████│
│                                                                             │
│                         Nuestros Servicios                                  │
│                                                                             │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐                      │
│   │  🛡️         │   │  📋         │   │  🔒         │                      │
│   │ SARLAFT/    │   │   PTEE      │   │ Protección  │                      │
│   │ SAGRILAFT   │   │             │   │ de Datos    │                      │
│   │             │   │ Transparencia│   │             │                      │
│   │ Prevención  │   │ y Ética     │   │ Ley 1581    │                      │
│   │ LA/FT       │   │ Empresarial │   │ de 2012     │                      │
│   └─────────────┘   └─────────────┘   └─────────────┘                      │
│                                                                             │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────┐                      │
│   │  🔍         │   │  📚         │   │  💼         │                      │
│   │ Auditoría   │   │ Capacitación│   │ Consultoría │                      │
│   │ Forense     │   │ y Formación │   │ Estratégica │                      │
│   │             │   │             │   │             │                      │
│   │ Detección   │   │ Diplomado   │   │ Diseño de   │                      │
│   │ vulnerab.   │   │ 120 horas   │   │ políticas   │                      │
│   └─────────────┘   └─────────────┘   └─────────────┘                      │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Especificaciones Cards:**
- Layout: Grid 3 columnas (2 en tablet, 1 en mobile)
- Card: Fondo blanco, border-radius 12px, sombra suave
- Ícono: 48px, color del imagotipo (variado por servicio)
- Título: Montserrat 20px SemiBold
- Descripción: Open Sans 14px

---

### 3.4 Sección 4: ¿POR QUÉ AFI?

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ ███████████████████████████ FONDO CLARO #FDFDFD ████████████████████████████│
│                                                                             │
│                         ¿Por qué elegir AFI?                                │
│                                                                             │
│   ┌─────────────────────────────────────────────────────────────────────┐  │
│   │                                                                     │  │
│   │   ┌─────────────────┐       ⚡ VELOCIDAD                            │  │
│   │   │                 │          Implementación rápida y eficiente   │  │
│   │   │   [FOTO FOUNDER]│                                              │  │
│   │   │                 │       ✓ CONFIABILIDAD                        │  │
│   │   │                 │          Resultados comprobados              │  │
│   │   │                 │                                              │  │
│   │   └─────────────────┘       👥 EQUIPO EXPERTO                      │  │
│   │   "Yessica Vasquez"            Multidisciplinario: Contaduría,    │  │
│   │   CEO                           Derecho, Administración, Ingeniería│  │
│   │                                                                     │  │
│   │                             🤝 ACOMPAÑAMIENTO                       │  │
│   │                                Desde diagnóstico hasta auditoría   │  │
│   │                                                                     │  │
│   └─────────────────────────────────────────────────────────────────────┘  │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Especificaciones:**
- Layout: 2 columnas (foto founder izq, beneficios der)
- Foto founder: `https://i.ibb.co/8LPs3XC4/Gemini-Generated-Image-zfsvnuzfsvnuzfsv.png`
- Foto con border-radius circular o suave, tamaño ~200px
- Nombre y cargo debajo de la foto en texto centrado
- Checkmarks/íconos: Color `#CE114E`
- Imagen secundaria (equipo): `https://images.unsplash.com/photo-1552664730-d307ca884978` (opcional como fondo sutil)

---

### 3.5 Sección 5: CLIENTES

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ █████████████████████████ FONDO GRIS #F5F7FA ███████████████████████████████│
│                                                                             │
│                    Empresas que confían en nosotros                         │
│                                                                             │
│   ┌─────────────────────────────────────────────────────────────────────┐  │
│   │                                                                     │  │
│   │   [Logo 1]  [Logo 2]  [Logo 3]  [Logo 4]  [Logo 5]  [Logo 6]       │  │
│   │                                                                     │  │
│   │   [Logo 7]  [Logo 8]  [Logo 9]  [Logo 10] [Logo 11] [Logo 12]      │  │
│   │                                                                     │  │
│   │   [Logo 13] [Logo 14] [Logo 15] [Logo 16] [Logo 17] [Logo 18]      │  │
│   │                                                                     │  │
│   └─────────────────────────────────────────────────────────────────────┘  │
│                                                                             │
│              "Experiencia diversificada en sectores público,                │
│               financiero, transportes, construcción e inversiones"          │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Especificaciones:**
- Grid: 6 columnas (4 tablet, 3 mobile)
- Logos: Escala de grises con hover a color (opcional)
- Altura logos: 60px máximo
- Gap: 40px entre logos

---

### 3.6 Sección 6: ALIADO (MéTRIK)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ ███████████████████████████ FONDO CLARO #FDFDFD ████████████████████████████│
│                                                                             │
│                    ALIADO EN INTELIGENCIA DE DATOS                          │
│                                                                             │
│   ┌─────────────────────────────────────────────────────────────────────┐  │
│   │                                                                     │  │
│   │                       [LOGO MéTRIK]                                 │  │
│   │                                                                     │  │
│   │   MéTRIK transforma datos operativos en claridad financiera        │  │
│   │   para PYMEs colombianas.                                          │  │
│   │                                                                     │  │
│   │   Con más de 10 años de experiencia en gestión de operaciones      │  │
│   │   y especialización en Business Intelligence, MéTRIK desarrolla    │  │
│   │   los tableros de control que permiten a los CDAs aliados de AFI   │  │
│   │   visualizar su cumplimiento en tiempo real.                       │  │
│   │                                                                     │  │
│   │   ✓ Dashboards funcionales en 10 días                              │  │
│   │   ✓ Integración con sistemas existentes                            │  │
│   │   ✓ Soporte continuo                                               │  │
│   │                                                                     │  │
│   │   "Tus números claros, decisiones seguras"                         │  │
│   │                                                                     │  │
│   │              ┌────────────────────────┐                             │  │
│   │              │  Conocer más →         │                             │  │
│   │              │  metrik.com.co         │                             │  │
│   │              └────────────────────────┘                             │  │
│   │                                                                     │  │
│   └─────────────────────────────────────────────────────────────────────┘  │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Especificaciones:**
- Logo MéTRIK: `https://i.ibb.co/sdb3Bpq5/M-trik-logo-iso.png`
- Centrado, con card suave de fondo
- Botón: Estilo outline, color primario MéTRIK
- Eslogan en itálica

---

### 3.7 Sección 7: CTA FINAL

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ ████████████████████████████ FONDO OSCURO #0A1628 ██████████████████████████│
│                                                                             │
│                                                                             │
│                    ¿Listo para fortalecer el                                │
│                    cumplimiento de tu empresa?                              │
│                                                                             │
│                    Agenda una consulta gratuita                             │
│                    con nuestros expertos                                    │
│                                                                             │
│                  ┌──────────────┐  ┌──────────────┐                        │
│                  │ 📅 Agendar   │  │ 💬 WhatsApp  │                        │
│                  │   llamada    │  │              │                        │
│                  └──────────────┘  └──────────────┘                        │
│                                                                             │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Especificaciones:**
- Padding: 100px vertical
- Texto: Blanco, centrado
- Título: Montserrat 36px Bold
- Botones: Mismo estilo que hero

---

### 3.8 Sección 8: FOOTER

```
┌─────────────────────────────────────────────────────────────────────────────┐
│ ███████████████████████████ FONDO #050A12 ██████████████████████████████████│
│                                                                             │
│   [LOGO AFI]                                                                │
│                                                                             │
│   Contacto:                                                                 │
│   📧 afisarlaft@gmail.com                                                   │
│   📞 317 718 9028 – 300 358 5020                                           │
│   🌐 afiinternationalgroup.com                                             │
│                                                                             │
│   ─────────────────────────────────────────────────────────────────────    │
│                                                                             │
│                         powered by                                          │
│                        [LOGO MéTRIK]                                        │
│                                                                             │
│   © 2026 AFI International Group. Todos los derechos reservados.           │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Especificaciones:**
- "powered by" en gris claro `#6B7280`, texto pequeño 12px
- Logo MéTRIK: Tamaño reducido (80px ancho)
- Copyright: 14px, gris medio

---

## 4. ESPECIFICACIONES RESPONSIVE

### 4.1 Breakpoints

```css
/* Mobile First */
--breakpoint-sm: 640px;
--breakpoint-md: 768px;
--breakpoint-lg: 1024px;
--breakpoint-xl: 1280px;
```

### 4.2 Desktop (>1024px)

- Hero: 2 columnas (texto + imagen founder)
- Servicios: Grid 3 columnas
- Clientes: Grid 6 columnas
- ¿Por qué AFI?: 2 columnas
- Max-width contenedor: 1200px

### 4.3 Tablet (768px - 1024px)

- Hero: 2 columnas (proporciones ajustadas)
- Servicios: Grid 2 columnas
- Clientes: Grid 4 columnas
- ¿Por qué AFI?: Stack vertical

### 4.4 Mobile (<768px)

- Hero: Stack vertical (texto arriba, imagen abajo o hidden)
- Servicios: 1 columna
- Clientes: Grid 3 columnas (logos más pequeños)
- CTAs: Full width, stack vertical
- Padding lateral: 20px

---

## 5. COMPONENTES

### 5.1 Botón Primario

```css
.btn-primary {
  background-color: #CE114E;
  color: #FDFDFD;
  font-family: 'Montserrat', sans-serif;
  font-weight: 600;
  font-size: 16px;
  padding: 16px 32px;
  border-radius: 8px;
  border: none;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-primary:hover {
  background-color: #A00D3D;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(206, 17, 78, 0.3);
}
```

### 5.2 Botón Secundario (Outline)

```css
.btn-secondary {
  background-color: transparent;
  color: #FDFDFD;
  font-family: 'Montserrat', sans-serif;
  font-weight: 600;
  font-size: 16px;
  padding: 16px 32px;
  border-radius: 8px;
  border: 2px solid #FDFDFD;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn-secondary:hover {
  background-color: rgba(255, 255, 255, 0.1);
}
```

### 5.3 Card de Servicio

```css
.service-card {
  background-color: #FFFFFF;
  border-radius: 12px;
  padding: 32px;
  text-align: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  transition: all 0.3s ease;
}

.service-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
}

.service-card .icon {
  font-size: 48px;
  margin-bottom: 16px;
}

.service-card h3 {
  font-family: 'Montserrat', sans-serif;
  font-weight: 600;
  font-size: 20px;
  color: #0C0D0C;
  margin-bottom: 12px;
}

.service-card p {
  font-family: 'Open Sans', sans-serif;
  font-size: 14px;
  color: #5C8891;
  line-height: 1.6;
}
```

---

## 6. INTERACCIONES

### 6.1 Hover Estados

| Elemento | Efecto Hover |
|----------|--------------|
| Botones | Cambio de color + elevación |
| Cards | Elevación + sombra más pronunciada |
| Links | Underline + color primario |
| Logos clientes | Escala de grises → color (opcional) |

### 6.2 Scroll Animations (Sugerido)

- Fade in desde abajo para secciones
- Stagger en grid de servicios
- Parallax suave en hero (opcional)

---

## 7. ASSETS REQUERIDOS

### 7.1 Imágenes Confirmadas

| Asset | URL/Ubicación |
|-------|---------------|
| Logo AFI | `https://i.ibb.co/jZzy6pD6/descarga-2-e1759514991690-png-2.webp` |
| Logo MéTRIK | `https://i.ibb.co/sdb3Bpq5/M-trik-logo-iso.png` |
| Founder | `https://i.ibb.co/8LPs3XC4/Gemini-Generated-Image-zfsvnuzfsvnuzfsv.png` |
| Oficina 1 | `https://images.unsplash.com/photo-1497366216548-37526070297c` |
| Equipo | `https://images.unsplash.com/photo-1552664730-d307ca884978` |

### 7.2 Pendientes

- [ ] Logos de clientes (PNG) - Usar placeholders hasta recibir

---

## 8. LINKS Y CTAs

### 8.1 Calendly

```
URL: https://calendly.com/afisarlaft/30min
Texto: "Agendar llamada"
```

### 8.2 WhatsApp

```
URL: https://wa.me/573177189028?text=Hola,%20quiero%20información%20sobre%20implementación%20SARLAFT
Texto: "WhatsApp"
```

### 8.3 MéTRIK

```
URL: https://metrik.com.co
Texto: "Conocer más →"
```

---

## 9. TONO DE COMUNICACIÓN

Del manual de marca:
- **Corporativo:** Lenguaje formal pero accesible
- **Técnico:** Uso correcto de terminología del sector
- **Claro:** Mensajes directos sin ambigüedad
- **Preventivo:** Enfocado en protección y riesgos
- **Estratégico:** Orientado a resultados y valor

---

## 10. QUALITY GATE 2

```
✅ GATE 2: DESIGN SYSTEM APROBADO

Checklist de validación:
[x] Paleta de colores extraída del manual de marca
[x] Tipografías definidas (Montserrat + Open Sans)
[x] Estructura de 8 secciones definida
[x] Mockups ASCII de todas las secciones
[x] Especificaciones responsive
[x] Componentes CSS documentados
[x] Assets de imágenes identificados
[x] Links y CTAs confirmados

¿Aprobado para continuar a CODE AGENT?

[✓] SÍ - Generar código
[ ] SÍ con ajustes - Especificar
[ ] NO - Revisar pendientes
```

---

**PRÓXIMO PASO:** Activar CODE AGENT para desarrollar la landing page.

---

**FIN DEL DESIGN SYSTEM**
