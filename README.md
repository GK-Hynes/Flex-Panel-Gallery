# Flex Panel Gallery

An image gallery built to practice Flexbox and vanilla JavaScript. Built for Wes Bos' [JavaScript 30](https://javascript30.com/) course.

[![Screenshot of Flex Panel Gallery](https://screenshots.firefoxusercontent.com/images/3d4e84c4-6218-4dc2-81c7-1158ee14a288.jpg)](https://gk-hynes.github.io/flex-panel-gallery/)

## Notes

An element in CSS can be both a flex item and a flex container.

Set all the panels to `display: flex;` and they will each take up only as much space as their content needs.

Set each panel to `flex: 1;` and they will divide up the extra space equally among themselves.

Set each panel to `display: flex;` and `flex-direction: column;` to vertically centre the content.

Set each panel to

```
flex: 1 0 auto;
display: flex;
justify-content: center;
align-items: center;
```

to evenly divide the panel into three sections.

Use `transform: translateY()` to push the top and bottom text content off the screen and the class `open-active` to transition them back in.

When a panel has a class of `open` set it to `flex: 5;` so it will take up five times as much of the extra room as the other panels.

By giving a panel a transition set to a cubic bezier it will transition beyond its correct size and then snap back.

Use `document.querySelectorAll()` to select all the panels. Then use a function to loop over all the panels, listen for a click, and toggle their classes.

With another function, listen for the transition end event, check if it includes the word `flex`, and toggle the class of `open-active`.
