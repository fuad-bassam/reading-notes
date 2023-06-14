# CSS

| Section                                     | Link                                                          |
| ------------------------------------------- | ------------------------------------------------------------- |
| important video reference                     | [Link](#css-selectors)                                        |
| CSS Selectors                               | [Link](#css-selectors)                                        |
| Summary of CSS Properties                   | [Link](#summary-of-css-properties)                            |
| Summary of Properties Used with `display`    | [Link](#summary-of-properties-used-with-display-property)      |
| Summary of Properties Used with `display: flex`    | [Link](#summary-of-properties-used-with-display-flex)      |
| Summary of Properties Used with `display: grid`    | [Link](#summary-of-properties-used-with-display-grid)      |
| Summary of Measurement Units in CSS         | [Link](#summary-of-measurement-units-in-css)                   |

## Important video reference:

  1. [Learn CSS Display Property In 4 Minutes](https://www.youtube.com/watch?v=Qf-wVa9y9V4)
  2. [Learn Flexbox in 15 Minutes](https://www.youtube.com/watch?v=fYq5PXgSsbE)
  3. [Learn CSS Grid in 20 Minutes](https://www.youtube.com/watch?v=9zBsdzdE4sM)  


## CSS Selectors:
- Selectors are used to target specific HTML elements and apply styles to them.
- Common selectors include element selectors, class selectors, ID selectors, and attribute selectors.
- CSS Selector Combinations:
  1. If there are no spaces between selectors, it means we are applying styles to multiple selectors on the same element.
     ```css
     div p {
         color: red;
     }
     ```
  2. If there is a space between selectors, it means one selector is nested inside another selector.
     ```css
     .ancestor .child {
         property: value;
     }
     ```

## Summary of CSS Properties:

| Category              | Properties                                                                                         |
| --------------------- | ------------------------------------------------------------------------------------------------- |
| Box Model             | `width`, `height`, `margin`, `padding`, `border`, `box-sizing`, `overflow`                         |
| Typography            | `color`, `font-family`, `font-size`, `font-weight`, `text-align`, `text-decoration`, `text-transform`, `line-height` |
| Background and Borders| `background-color`, `background-image`, `background-repeat`, `background-position`, `border-color`, `border-width`, `border-style`, `border-radius` |
| Layout and Positioning | `display`, `position`, `float`, `clear`, `z-index`, `visibility`, `overflow-x`, `overflow-y`       |
| Flexbox               | `flex-direction`, `justify-content`, `align-items`, `flex-wrap`, `flex-grow`, `flex-shrink`, `flex-basis` |
| Grid                  | `grid-template-columns`, `grid-template-rows`, `grid-gap`, `grid-column-start`, `grid-column-end`, `grid-row-start`, `grid-row-end` |
| Transforms and Animations | `transform`, `transition`, `animation`, `keyframes`                                              |
| Box Shadow and Text Shadow | `box-shadow`, `text-shadow`                                                                     |
| Miscellaneous         | `cursor`, `opacity`, `outline`, `pointer-events`, `user-select`                                   |
| Responsive Design     | `media queries`, `viewport units (vw, vh)`, `responsive units (rem, em)`, `@media rule`            |
| Pseudo-classes and Pseudo-elements | `:hover`, `:active`, `:focus`, `:first-child`, `:last-child`, `::before`, `::after`           |
| Lists and Tables      | `list-style-type`, `list-style-image`, `table-layout`, `border-collapse`, `caption-side`          |
| Transitions and Animations | `transition-property`, `transition-duration`, `transition-timing-function`, `animation-name`, `animation-duration`, `animation-delay` |

## Summary of Properties Used with `display` Property:

| Property           | Description                                                                                        |
| ------------------ | -------------------------------------------------------------------------------------------------- |
| `flex-direction`    | Specifies the direction of the flex container's main axis, determining how flex items are laid out |
| `justify-content`    | Aligns flex items along the main axis of the flex container                                        |
| `align-items`        | Aligns flex items along the cross axis of the flex container                                       |
| `align-content`      | Aligns multiple lines of flex items along the cross axis when there's extra space                  |
| `flex-wrap`          | Specifies whether flex items should wrap or remain on a single line                               |
| `flex-grow`          | Determines how flex items grow to fill the remaining space along the main axis                    |
| `flex-shrink`        | Controls how flex items shrink if there's not enough space available                              |
| `flex-basis`         | Specifies the initial size of flex items before any remaining space is distributed                |
| `order`              | Specifies the order in which flex items appear within the flex container                          |

![img](../css%26JS/flexboxVSgrid.PNG)

## Summary of Properties Used with `display: flex`:

| Property           | Description                                                                                   |
| ------------------ | --------------------------------------------------------------------------------------------- |
| `flex-direction`    | Specifies the direction of the flex container's main axis.                                   |
| `justify-content`    | Aligns flex items along the main axis of the flex container.                                 |
| `align-items`        | Aligns flex items along the cross axis of the flex container.                                |
| `align-content`      | Aligns multiple lines of flex items along the cross axis.                                    |
| `flex-wrap`          | Specifies whether flex items should wrap or remain on a single line.                         |
| `flex-grow`          | Determines how flex items grow to fill the remaining space.                                  |
| `flex-shrink`        | Controls how flex items shrink if there's not enough space.                                  |
| `flex-basis`         | Specifies the initial size of flex items before any remaining space is distributed.          |
| `order`              | Specifies the order in which flex items appear within the flex container.                    |

## Summary of Properties Used with `display: grid`:

| Property                  | Description                                                                                   |
| ------------------------- | --------------------------------------------------------------------------------------------- |
| `grid-template-columns`     | Defines the number and size of columns in a grid container.                                    |
| `grid-template-rows`        | Defines the number and size of rows in a grid container.                                       |
| `grid-gap`                  | Specifies the size of the gap between grid rows and columns.                                   |
| `grid-column-start`         | Determines the starting position of a grid item along the horizontal axis.                    |
| `grid-column-end`           | Determines the ending position of a grid item along the horizontal axis.                      |
| `grid-row-start`            | Determines the starting position of a grid item along the vertical axis.                      |
| `grid-row-end`              | Determines the ending position of a grid item along the vertical axis.                        |
| `justify-items`             | Aligns grid items along the horizontal axis within their grid cells.                          |
| `align-items`               | Aligns grid items along the vertical axis within their grid cells.                            |
| `justify-content`           | Aligns grid items along the horizontal axis within the grid container.                        |
| `align-content`             | Aligns grid items along the vertical axis within the grid container.                          |
| `grid-auto-columns`         | Sets the size of implicitly-created grid tracks when new grid items are added.                |
| `grid-auto-rows`            | Sets the size of implicitly-created grid tracks when new grid items are added.                |
| `grid-auto-flow`            | Controls the placement of grid items that are not explicitly placed.                          |

## Summary of Measurement Units in CSS:

| Unit            | Description                                                                                        |
| --------------- | -------------------------------------------------------------------------------------------------- |
| `px`            | Represents pixels, which is a fixed unit of measurement.                                           |
| `%`             | Represents a percentage of the parent element's size or value.                                    |
| `em`            | Represents the computed font-size of the element or the font-size of its parent element.          |
| `rem`           | Represents the computed font-size of the root element (`<html>`).                                 |
| `vh`            | Represents a percentage of the viewport height.                                                   |
| `vw`            | Represents a percentage of the viewport width.                                                    |
| `vmin`          | Represents a percentage of the smaller dimension between viewport width and height.               |
| `vmax`          | Represents a percentage of the larger dimension between viewport width and height.                |
| `ex`            | Represents the height of the lowercase letter "x" within the current font.                        |
| `ch`            | Represents the width of the "0" (zero) character within the current font.                         |
| `rem`           | Represents the computed font-size of the root element (`<html>`).                                 |
| `pt`            | Represents points, which are commonly used in print media.                                        |
| `cm`, `mm`, `in`| Represents centimeters, millimeters, and inches, respectively.                                    |
| `pc`            | Represents picas, where 1 pica is equal to 12 points.                                             |