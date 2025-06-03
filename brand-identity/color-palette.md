# EduBox Brand Colors

## Official Logo Colors

These are the exact colors used in the Central E Network logo:

### Core Logo Palette

#### EduBox Blue (Primary)
- **HEX**: #2C5AA0
- **RGB**: 44, 90, 160
- **CMYK**: 73, 44, 0, 37
- **HSL**: 214°, 57%, 40%
- **Usage**: Central E box, primary brand element
- **Logo element**: Main box containing the "E"

#### Network Orange (Accent)
- **HEX**: #F39C12
- **RGB**: 243, 156, 18
- **CMYK**: 0, 36, 93, 5
- **HSL**: 37°, 90%, 51%
- **Usage**: Primary network nodes (cardinal points)
- **Logo element**: Four main connection points

#### Connection Blue (Secondary)
- **HEX**: #3498DB
- **RGB**: 52, 152, 219
- **CMYK**: 76, 31, 0, 14
- **HSL**: 204°, 70%, 53%
- **Usage**: Secondary nodes, connection lines
- **Logo element**: Corner nodes and network lines

### Supporting Palette

#### Growth Green
- **HEX**: #27AE60
- **RGB**: 39, 174, 96
- **CMYK**: 78, 0, 45, 32
- **HSL**: 145°, 63%, 42%
- **Usage**: Success states, sustainability messaging
- **Note**: Not used in logo, but complements brand

### Neutral Palette

#### Deep Gray (Text)
- **HEX**: #2C3E50
- **RGB**: 44, 62, 80
- **CMYK**: 45, 23, 0, 69
- **Usage**: Primary text, headers

#### Medium Gray
- **HEX**: #7F8C8D
- **RGB**: 127, 140, 141
- **CMYK**: 10, 1, 0, 45
- **Usage**: Secondary text, captions

#### Light Gray
- **HEX**: #ECF0F1
- **RGB**: 236, 240, 241
- **CMYK**: 2, 0, 0, 5
- **Usage**: Borders, dividers, subtle backgrounds

#### Off White
- **HEX**: #F8F9FA
- **RGB**: 248, 249, 250
- **CMYK**: 1, 0, 0, 2
- **Usage**: Page backgrounds, cards

### Semantic Colors

#### Success Green
- **HEX**: #27AE60
- **Usage**: Success messages, positive stats

#### Warning Orange
- **HEX**: #F39C12
- **Usage**: Important notices, warnings

#### Error Red
- **HEX**: #E74C3C
- **Usage**: Error states only (sparingly)

#### Info Blue
- **HEX**: #3498DB
- **Usage**: Informational messages

## Color Accessibility

### WCAG AA Compliance
- **EduBox Blue on White**: ✅ Pass (5.07:1)
- **Sunrise Orange on White**: ⚠️ Use for large text only (3.13:1)
- **Deep Gray on White**: ✅ Pass (12.63:1)
- **White on EduBox Blue**: ✅ Pass (5.07:1)

### Logo-Based Color Hierarchy

1. **Primary Applications**
   - EduBox Blue (#2C5AA0): Headers, buttons, main UI elements
   - White: E letterform, reversed applications

2. **Accent Applications**
   - Network Orange (#F39C12): CTAs, highlights, primary interactions
   - Connection Blue (#3498DB): Links, secondary buttons, info elements

3. **Supporting Applications**
   - Growth Green (#27AE60): Success messages, positive indicators
   - Neutrals: Text, backgrounds, borders

### Accessible Combinations
1. **From Logo**
   - White on EduBox Blue (#2C5AA0) - ✅ Used in logo
   - EduBox Blue on white - ✅ High contrast
   - Connection Blue (#3498DB) on white - ✅ Good for links

2. **Supporting**
   - Deep Gray (#2C3E50) on Off White (#F8F9FA)
   - Growth Green (#27AE60) on Off White (#F8F9FA)

3. **Do Not Use**
   - Network Orange on white for body text (contrast too low)
   - Light colors on light backgrounds
   - Multiple bright colors together

## CSS Variables
```css
:root {
  /* Logo Colors */
  --edubox-primary: #2C5AA0;    /* E box */
  --edubox-accent: #F39C12;     /* Primary nodes */
  --edubox-connection: #3498DB; /* Secondary nodes & lines */
  
  /* Supporting Colors */
  --edubox-green: #27AE60;      /* Success, growth */
  
  /* Neutrals */
  --edubox-dark: #2C3E50;
  --edubox-gray: #7F8C8D;
  --edubox-light: #ECF0F1;
  --edubox-white: #F8F9FA;
  
  /* Semantic (matching logo) */
  --edubox-success: #27AE60;
  --edubox-warning: #F39C12;
  --edubox-error: #E74C3C;
  --edubox-info: #3498DB;
}
```

## Tailwind Config
```javascript
colors: {
  'edubox': {
    'blue': '#2C5AA0',
    'orange': '#F39C12',
    'green': '#27AE60',
    'sky': '#3498DB',
    'dark': '#2C3E50',
    'gray': '#7F8C8D',
    'light': '#ECF0F1',
    'white': '#F8F9FA'
  }
}
```