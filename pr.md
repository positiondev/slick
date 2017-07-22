https://github.com/kenwheeler/slick/compare/master...positiondev:master

This code adds a new customization called `slidesPerDot` that causes the system to display fewer dots that skip more slides, while the arrows still go one slide at a time. So the dots provide a sort of summary or pagination.

The motivation for this was that we want to use slick for a feed of updates where there would be a large number of updates, but the most recent (left most) are most relevant. We want the user to land on the page and be able to swipe one slide at a time, but then they should be able to page through at a much faster rate with the dots.

To use, you can configure slick something like this:

```
$(".summaryDots").slick({
  dots: true,
  infinite: false,
  centerMode: false,
  slidesToShow: 3,
  slidesPerDot: 3
});
```

See these jsfiddles for some examples:

http://jsfiddle.net/7mdeo2pm/2/
http://jsfiddle.net/7mdeo2pm/3/