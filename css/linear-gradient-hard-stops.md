# Linear gradient hard stops

I tried out a css battle today and decided to use `linear-gradient` and `repeating-linear-gradient` to get the job done - it may not have been the shortest solution, or even the cleanest, but I hadn't used this technique before and wanted to try it out.

Here are the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/linear-gradient#gradient_with_multi-position_color-stops) on the subject.

Essentially instead of a smooth gradient with one color fading into the next, you can specify how long to hold the color:

```css
div {
  background: linear-gradient(
    /* default direction is top to bottom */ red 20%,
    blue 20% 50%,
    green 50% 75%,
    yellow 75%
  );
}
```

This will yield a swatch of colors that don't blend together at all - the background will be red from 0-20%, blue from 20-50%, green from 50-75%, and yellow from 75% through the end. You can get a striped effect like this:

```css
div {
  background: linear-gradient(
    red 20%,
    blue 20% 40%,
    red 40% 60%,
    blue 60% 80%,
    red 80%
  );
}
```

or using `repeating-linear-gradient`:

```css
div {
  background: repeating-linear-gradient(red 20%, blue 20% 40%, red 40% 60%);
}
```

Note that you do have to include the first of the repeating cycle, so in this case it only saves two lines to do repeating - you aren't able to just leave it at red -> blue because CSS doesn't know what to repeat.
