# Unexpected :has() Selector Behavior in CSS

This repository demonstrates an uncommon bug related to the CSS `:has()` pseudo-class.  Specifically, the issue arises when using `:has()` to target parent elements based on nested children.

## Problem

The `:has()` selector in CSS is designed to style a parent element if it contains a specific child element. However, its behavior when dealing with deeply nested children isn't always intuitive.

The provided CSS aims to style `.parent` only if it directly contains a `.child-element`, but the implementation affects the parent even when `.child-element` is a descendant.  This creates unexpected styling, potentially leading to maintenance issues.

## Solution

The solution utilizes a more targeted selector to explicitly ensure that only direct children are considered.  This avoids the unexpected behavior caused by the broader scope of `:has()` when applied to nested structures.

## Usage

1. Clone this repository.
2. Open `bug.html` in your browser to see the unexpected behavior.
3. Open `solution.html` to see how the issue is resolved.

This example highlights a subtlety in CSS that can be easily overlooked, leading to unexpected visual outcomes.