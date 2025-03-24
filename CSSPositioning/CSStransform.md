# transform property
- The transform property allows you to modify the shape, position, and size of an element without changing the layout or affecting the surrounding elements. 
- It has functions such as `translate()`, `rotate()`, `scale()`, `skew()`, and` matrix()`.
- Common use cases:
	- translate: Centering elements, animations
	- rotate: Icons, buttons, animations
	- scale: Hover effects, emphasis
	- skew: Creative effects, text styling
	- matrix: Complex animations

### translate()
- Moves
```css
.move {
    transform: translateX(100px);    /* move right 100px */
    transform: translateY(50px);     /* move down 50px */
    transform: translate(100px, 50px); /* move right and down */
    transform: translate(-50%, -50%); /* common for perfect centering */
}
```

### rotate()
- Spins
```css
.spin {
    transform: rotate(45deg);     /* clockwise rotation */
    transform: rotate(-90deg);    /* counter-clockwise */
    transform: rotate(0.5turn);   /* can also use 'turn' unit */
}
```

### scale()
- Resizes
```css
.resize {
    transform: scale(2);          /* doubles size */
    transform: scale(0.5);        /* halves size */
    transform: scale(2, 1.5);     /* width 2x, height 1.5x */
    transform: scaleX(2);         /* only width */
    transform: scaleY(0.5);       /* only height */
}
```

### skew()
- Tilts
```css
.tilt {
    transform: skewX(20deg);      /* horizontal tilt */
    transform: skewY(20deg);      /* vertical tilt */
    transform: skew(20deg, 10deg); /* both directions */
}
```

# matrix()
- Combines transforms
```css
.complex {
    transform: matrix(1, 0, 0, 1, 50, 50); /* advanced usage */
}
```
- Or combines multiple transforms
```css
.combined {
    transform: translate(100px, 0) rotate(45deg) scale(1.5);
}
```