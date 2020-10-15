## What is clamp function in CSS?

Hi everyone, today I going to explain the importance of an inbuilt CSS function called `clamp()` which can be used most of the time in building responsive web pages without the need of media queries.

### What is a clamp function?

The `clamp()` CSS function clamps a value between an upper and lower bound. clamp() enables selecting a middle value within a range of values between a defined minimum and maximum. 

While it’s a related idea to min() and max() it is different in specific ways:

- Order matters
- It only takes 3 parameters

- Those 3 parameters are

   1.The minimum

   2.The target value (ideally a relative unit)

   3.The maximum

```css
 clamp(MIN, VAL, MAX)
```

- `clamp()` can be used for any of the following data types:

    - [`<length>`](https://developer.mozilla.org/en-US/docs/Web/CSS/length)
    - [`<frequency>`](https://developer.mozilla.org/en-US/docs/Web/CSS/frequency)
    - [`<angel>`](https://developer.mozilla.org/en-US/docs/Web/CSS/angle)
    - [`<time>`](https://developer.mozilla.org/en-US/docs/Web/CSS/time)
    - [`<percentage>`](https://developer.mozilla.org/en-US/docs/Web/CSS/percentage)
    - [`<number>`](https://developer.mozilla.org/en-US/docs/Web/CSS/number)
    - [`<integer>`](https://developer.mozilla.org/en-US/docs/Web/CSS/integer)


### Clamp function in action:

- Font size control using a `clamp()` with using a single media query

<iframe height="318" style="width: 100%;" scrolling="no" title="fontSize-control-with-clamp()" src="https://codepen.io/sridhar-katta/embed/NWrxvXo?height=318&theme-id=dark&default-tab=html,result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/sridhar-katta/pen/NWrxvXo'>fontSize-control-with-clamp()</a> by Sridhar Katta
  (<a href='https://codepen.io/sridhar-katta'>@sridhar-katta</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

- `Clamp()` for controlling Image width

<iframe height="500" style="width: 100%;" scrolling="no" title="clamp-function-css" src="https://codepen.io/sridhar-katta/embed/gOMPxro?height=500&theme-id=dark&default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href='https://codepen.io/sridhar-katta/pen/gOMPxro'>clamp-function-css</a> by Sridhar Katta
  (<a href='https://codepen.io/sridhar-katta'>@sridhar-katta</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

## Resources:
 
- [Mozilla Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp)


> If you have any doubts related to this article or anything related to tech or software-engineering in general, drop a comment here or you can message me on twitter [@ksridhar02](https://twitter.com/ksridhar02).
