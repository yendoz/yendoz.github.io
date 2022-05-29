---
title:  "More CSS. Flexbox"
categories: CSS
tags: [flexbox, MoreCSS]
toc: true
sidebar:
    nav: docs
---

# Further Study: [align-items VS align-content][1]

> Studying React Native from the App development course, I wanted to know the difference between `alignItems` and `alignContent`, because it seemed similar to me. To understand the idea, I looked through CSS documents and decided to organize the concepts of Flexbox.

<br>

## 1. Understanding concepts: links to read

+ [A Complete Guide to Flexbox][1]
<br>

+ [CSS Reference: Flexbox][2]
<br>

+ [Flexbox: align-items and align-content][3]

<br>

## 2. How to define `flex`

I can create a flex container, by setting `display` property into `flex`- creating block-level flex container- or `inline-flex` - creating inline-level flex container. The flex container becomes a **flex context** for its direct descendants. **Only the children** of a flex container are laid out by the Flexbox layout.

<br>

## 3. Flex axes

I can set `flex-direction` to determine the direction along which flex items are laid. The flex items will be laid out inside a flex container, following either the **main axis** or the **cross axis**. The cross axis is the axis perpendicular to the main axis. `flex-direction` can have `row`, `row-reverse`, `column`, `column-reverse` values, and each sets the direction of the flex container's main axis.

<br>

## 4. Flex lines

Flex items in a flex container are laid out and aligned within flex lines, a hypothetical line used for grouping and alignment of flex items inside their container. Flex lines follow the main axis. A flex container can be either **single-line** or **multi-line**, depending on the `flex-wrap` property:

+ A **single-line** flex container lays out all of its children in a single line, even if that would cause its contents to overflow.
<br>

+ A **multi-line** flex container **breaks** its flex items across multiple lines, similar to how text is broken onto a new line when it gets too wide to fit on the existing line. When additional lines are created, they are stacked in the flex container along the cross axis according to the `flex-wrap` property. Every line contains at least one flex item, unless the flex container itself is completely empty.

<br>

## 4. `flex-wrap`

[flex-wrap property][4] can have three values: `nowrap`, `wrap`, and `wrap-reverse`. It determines whether the flex container is single-line(`nowrap`) or multi-line(`wrap` or `wrap-reverse`). The difference between `wrap` and `wrap-reverse` is the direction that new lines are stacked in. Using `wrap` means the items are stacked along the cross axis, whereas `wrap-reverse` means that the items are stacked in the opposite direction of the cross axis. 

<br>

## 5. `justify-content`, `align-items`

[justify-content property][5] can have `flex-start`, `flex-end`, `center`, `space-between`, `space-around`. It aligns the items along the **main axis**.
<br>

[align-items property][6] can have `flex-start`, `flex-end`, `center`, `baseline`, `stretch`. It aligns the items along the **cross axis**. The `baseline` value aligns items according to its baseline.

<br>

## 6. `align-content`

[align-content property][7] **aligns a flex container’s lines within**, when there is extra space in the cross-axis, similar to how `justify-content` aligns individual items within the main-axis. This property has no effect when the flex container has only a single line.

<br>

## 7. `align-self`

[align-self property][8] can have `auto`, `flex-start`, `flex-end`, `center`, `baseline`, `strecth`. The `align-self` property allows the alignment specified by `align-items` to be **overridden** for individual flex items, along the cross axis. Note that the `baseline` value is identical to `flex-start` if the flex item’s inline axis is the same as the cross axis.

<br>

## 8. `flex-grow`

[flex-grow property][9] takes a number value, and it determines the proportion of how much the flex item will grow relative to the rest of the flex items in the flex container, when positive free space is distributed. The initial value is zero(0), and negative numbers are invalid. It's similar to React native's `flex` property in `StyleSheet` in that it sets the proportion of the space. Using `flex-grow`, I can expand the flex items so that those items could fill up the entire space.

<br>

## 9. `flex-shrink`

[flex-shrink property][10] also takes a number value, and it determines how much the flex item will shrink relative to the rest of the flex items in the flex container, when negative free space is distributed. The initial value is zero(1), meaning that the items don’t shrink by default, and negative numbers are invalid.

<br>




[1]: https://css-tricks.com/snippets/css/a-guide-to-flexbox/
[2]: https://tympanus.net/codrops/css_reference/flexbox/
[3]: https://betterprogramming.pub/flexbox-align-items-and-align-content-a60b6f8451e3
[4]: https://tympanus.net/codrops/css_reference/flexbox/#section_flex-wrap
[5]: https://tympanus.net/codrops/css_reference/flexbox/#section_justify-content
[6]: https://tympanus.net/codrops/css_reference/flexbox/#section_align-items
[7]: https://tympanus.net/codrops/css_reference/flexbox/#section_align-content
[8]: https://tympanus.net/codrops/css_reference/flexbox/#section_align-self
[9]: https://tympanus.net/codrops/css_reference/flexbox/#section_flex-grow
[10]: https://tympanus.net/codrops/css_reference/flexbox/#section_flex-shrink
