# ColorToRgbTriplet

## Table of Contents

1. [Acknowledgements](#acknowledgements)
2. [Description](#description)
3. [Syntax](#syntax)
4. [Examples](#examples)
5. [References](#references)

## Acknowledgements

Based on the work of [Yasin Zamani](https://www.mathworks.com/matlabcentral/profile/authors/14373174-yasin-zamani). See reference implemention [here](https://www.mathworks.com/matlabcentral/fileexchange/71273-color).

## Description

Converts **color name** or **hexadecimal color code** to an **rgb triplet**. Optionally a second argument can be passed defining the desired opacity level within `[0,1]`.

A **rgb triplet** is a three-element row vector whose elements specify the intensities of the red, green, and blue components of the color. The intensities are in the range `[0,1]`; for example, `[0.4 0.6 0.7]`.

A *hexadecimal color code* is a character vector or a string scalar that starts with a hash symbol (`#`) followed by three or six hexadecimal digits, which can range from `0` to `F`. The values are not case sensitive. Thus, the color codes `'#FF8800'`, `'#ff8800'`, `'#F80'`, and `'#f80'` are equivalent.

## Syntax

```matlab
color % shows color picker.
% without transparency
rgb = color(name) % converts color name to an rgb triplet.
rgb = color(hex) % converts hexadecimal color code to an rgb triplet.

% with transparency
rgbo = color(name, 0.3) % converts color name to an rgb triplet plus opacity.
rgbo = color(hex, 0.3) % converts hexadecimal color code to an rgb triplet plus opacity.
```

## Examples

```matlab
figure('Color', color('ghost'));
fplot(@(x) sin(x), 'Color', color('royal'), 'LineWidth', 7);
hold('on');
fplot(0, 'Color', color('fire', 0.2), 'LineWidth', 3, 'LineStyle', '--');
hold('off');
axis('off');
title('Sin(x)', 'Color', color('golden'), 'FontSize', 20);
```

## References

- [w3schools.com/colors/colors_names.](w3schools.com/colors/colors_names.asp)
- [w3schools.com/colors/colors_picker.asp](https://www.w3schools.com/colors/colors_picker.asp)
