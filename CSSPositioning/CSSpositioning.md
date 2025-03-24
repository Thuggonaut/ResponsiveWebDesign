# CSS Positioning
- Mastering CSS positioning is essential for creating visually appealing and responsive web layouts
	- absolute positioning
	- the z-index property
	- the transform property.

# position property
- Lets you set how you want an element to be positioned in the browser. 
- You can set it to `static`, `absolute`, `relative`, `sticky` or `fixed`.
- Once you set the `position` property of the element, you can move the element around by setting a pixel or a percentage value for one or more of the `top`, `right`, `left`, or `bottom` properties.

# position attributes
- `static` is the default positioning for all elements. 
	- If you assign it to an element, you won't be able to move it around with `top`, `right`, `left`, or `bottom`.

### relative
	- Stays in normal flow
	- Can be offset from its normal position
	- Creates a positioning context for absolute children
```css
.relative {
    position: relative;
    top: 10px;    /* moves down 10px from normal position */
    left: 20px;   /* moves right 20px from normal position */
}
```

### absolute
	- removed from normal flow
	- Positioned relative to nearest positioned ancestor (or body)
	- 
	- Other elements act like it doesn't exist
```css
.absolute {
    position: absolute;
    top: 0;       /* positions from top of nearest positioned parent */
    right: 0;     /* positions from right of nearest positioned parent */
}
```

### fixed
	- Removed from normal flow
	- Positioned relative to viewport
	- Stays in place during scrolling - makes an element fixed to the page no matter where the user scrolls to on the page.
```css
.fixed {
    position: fixed;
    bottom: 20px;  /* always 20px from bottom of screen */
    right: 20px;   /* always 20px from right of screen */
}
```

### sticky
	- Hybrid of relative and fixed
	- It allows an element to stick to a specific position within its containing element or viewport, based on the scroll position.
```css
.sticky {
    position: sticky;
    top: 0;       /* sticks to top when scrolled to this position */
}
```

- Common use cases:
	- `relative`: Slight adjustments or parent for absolute elements
	- `absolute`: Modals, tooltips, badges
	- `fixed`: Navigation bars, chat widgets, "back to top" buttons
	- `sticky`: Section headers, navigation elements that stick while scrolling


# z-index property
- `z-index` is a property you can use to define the order of overlapping HTML elements.
- Any element with a higher `z-index` will always be positioned over an element with a lower `z-index`.