# Turn value for rotate property

The rotate property in CSS turns an element around one or more axes. Think of it like poking one or more pins into an element and spinning the element around those points in clockwise and counter-clockwise directions measured in degree, gradian, radian, and turn values.

```
.element {
  rotate: 45deg;
}
```

The angle values are expressed in degrees, gradians, radians, or turns.

```
/* Keyword values */
rotate: none;

/* Angle values */
rotate: 45deg;
rotate: 0.35turn;
rotate: 1.27rad;
rotate: -50grad;

/* x, y, or z-axis name plus angle */
rotate: x 45deg;
rotate: y 0.35turn;
rotate: z 1.27rad;

/* Vector plus angle values */
rotate: 1 0.5 1 45deg;

/* Global values */
rotate: inherit;
rotate: initial;
rotate: revert;
rotate: unset;
```