# Units
Units refer to any numeric value with an affix, for example **px**,**pt**,**mm**.

```
body {
  font-size: 12px;
  line-height: 20pt;
}
```

## Absolute length units
They are similar to [CSS Lengths](http://www.w3.org/TR/css3-values/#absolute-lengths). For operations all of these must be converted to pixel. These are:
  * in: inches
  * cm: centimeters
  * mm: millimeters
  * pt: points
  * pc: picas
  * px: pixel

```
body {
  line-height: 30px;
}
```

## Time length units
They are similar to [CSS Time values](http://www.w3.org/TR/css3-values/#time-value). For operations all of these must be converted to millisecond. These are:
  * s: second
  * ms: millisecond
  * m: minute
  * h: hour

```
body {
  transition-duration: 3s;
}
```
