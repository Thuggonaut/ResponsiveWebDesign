# contrast of elements
- contrast between elements is a key factor. 
- For example, the contrast between the text and the background of a heading should be at least 4.5:1.
	- 4.5: This number represents the relative luminance of the lighter color (foreground).
	- 1: This number represents the relative luminance of the darker color (background).

# Cursor styles
- Here are some common cursor styles you can use in CSS:
- default: The default arrow cursor.
- pointer: A hand cursor, typically used for links.
- crosshair: A crosshair cursor.
- move: Indicates something is movable.
- text: Indicates text can be selected (usually a text cursor).
- wait: Indicates the program is busy (usually an hourglass or spinning wheel).
- help: Indicates help is available (usually a question mark).
- not-allowed: Indicates that an action is not allowed (usually a circle with a line through it).
- progress: Indicates that a task is in progress (usually a spinning wheel).
- zoom-in: Indicates that an element can be zoomed in.
- zoom-out: Indicates that an element can be zoomed out.
- grab: Indicates that an element can be grabbed (usually a hand).
- grabbing: Indicates that an element is being grabbed (usually a hand with fingers closed)

# Smooth scrolling
- Clicking on the navigation links should jump the viewport to the relevant section However, this jumping can be disorienting for some users.
- Select all elements, and set the scroll-behavior to smooth.
```css
* {
	/*universal selector*/
	scroll-behavior: smooth;
}
```


# Motion triggers
- Certain types of motion-based animations can cause discomfort for some users. 
- In particular, people with vestibular disorders have sensitivity to certain motion triggers.
- The `@media` at-rule has a media feature called `prefers-reduced-motion` to set CSS based on the user's preferences. It can take one of the following values:
	- reduce
	- no-preference
```css
@media (feature: value) {
	selector {
		styles
	}
}
```