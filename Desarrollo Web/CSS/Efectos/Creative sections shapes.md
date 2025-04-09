---
tags:
  - css
  - efectos
---
## Diagonal

```css
.diagonal {
    --skew-angle: -2deg;
    --bg: linear-gradient(
        45deg,
        #12c2e9,
        #c471ed,
        #f64e60
    );

    position: relative;
    isolation: isolate;
}

.diagonal::after {
    content: "";
    background-image: var(--bg);
    position: absolute;
    inset: 0;
    transform: skewY(var(--skew-angle));
    z-index: -1;
}
```

## Spikes

```css
.spikes {
	--spike-color: var(--body-bg);
	--spike-width: 30px;
	--spike-height: 30px;
	position: relative;
	background-image: linear-gradient(to right, #fdc830, #f37335);
}
.spikes::before,
.spikes::after {
	content: "";
	position: absolute;
	width: 100%;
	height: var(--spike-height);
	background-color: var(--body-bg);
	mask-image: url("assets/triangle.svg");
	mask-size: var(--spike-width) var(--spike-height);
	mask-repeat: repeat-x;
}
.spikes::before {
	top: 0;
}
.spikes::after {
	bottom: 0;
	transform: rotate(0.5turn);
}
```

## Wavy

```css
.wavy {
	position: relative;
	background-image: linear-gradient(to right, #00f260, #0575e6);
	--mask: radial-gradient(44.6px at 50% 63px, #000 99%, #0000 101%)
			calc(50% - 60px) 0/120px 51% repeat-x,
		radial-gradient(44.6px at 50% -33px, #0000 99%, #000 101%) 50% 30px/120px
			calc(51% - 30px) repeat-x,
		radial-gradient(44.6px at 50% calc(100% - 63px), #000 99%, #0000 101%) 50%
			100%/120px 51% repeat-x,
		radial-gradient(44.6px at 50% calc(100% + 33px), #0000 99%, #000 101%)
			calc(50% - 60px) calc(100% - 30px) / 120px calc(51% - 30px) repeat-x;
	-webkit-mask: var(--mask);
	mask: var(--mask);
}
```