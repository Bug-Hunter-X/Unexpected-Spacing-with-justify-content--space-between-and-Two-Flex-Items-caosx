# Unexpected Spacing with justify-content: space-between and Two Flex Items

This repository demonstrates a subtle but significant issue that can arise when using `justify-content: space-between` in CSS Flexbox layouts, specifically when dealing with only two flex items.  The problem is that the spacing is not evenly distributed in this case.

## The Problem

The `space-between` property distributes space *between* items but doesn't consider spacing at the start and end. This is fine with 3 or more items, but with 2, one large gap appears, and one item is flush to the edge.  See `bug.css` for the example code that produces this unexpected spacing.

## The Solution

The solution depends on your desired behavior. One solution, as in `bugSolution.css`, would be to adjust your layout or to check the number of items before applying the style. Consider using `justify-content: space-around` or `justify-content: space-evenly`  to achieve more even spacing for a variable number of items, or use a conditional approach in your javascript code to set styling for the elements based on their number.