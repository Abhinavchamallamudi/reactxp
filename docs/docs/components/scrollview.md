---
id: components/scrollview
title: ScrollView
layout: docs
category: Components
permalink: docs/components/scrollview.html
next: components/text
---

Like a View, this component is a container for other components. However, it supports scrolling (panning) and zooming so it is possible to view larger contents. 

ScrollViews must have a bounded height (or width, if it scrolls horizontally) since its children are of unbounded height (or width). To bound the dimensions of a ScrollView, either set the height/width directly or make sure that its parent&apos;s height/width is bounded.

## Props
``` javascript
// Should scroll bar bounce when user hits the bounds?
bounces: boolean = true; // iOS only

// Style applied to the scroll view content container,the view that wraps the children
contentContainerStyle: RX.ViewStyleRuleSet | RX.ViewStyleRuleSet[] = [];

// Does it support scrolling in the horizontal and/or vertical directions?
horizontal: boolean = false;
vertical: boolean = true;

// If the contents are smaller than the view port, should they be justified 
// to the top of the view (i.e. flex-start) or the end (flex-end)?
justifyEnd: boolean = false;

// When the user scrolls the view, how should the on-screen keyboard react?
keyboardDismissMode: 'none' | 'interactive' | 'on-drag'; // Native only

// Should the on-screen keyboard remain visible when the user taps the scroll view?
keyboardShouldPersistTaps: boolean = false; // Native only

// Maximum scale factor
maximumZoomScale: number = 1.0;

// Minimum scale factor
minimumZoomScale: number = 1.0;

// Invoked when the contents of the scroll view change
onContentSizeChange: (width: number, height: number) => void = undefined;

// Invoked when view dimensions or position changes
onLayout: (e: ViewOnLayoutEvent) => void = undefined;

// Called when the scroll position changes
onScroll: (newScrollTop: number, newScrollLeft: number) => void = undefined;

// Android only property to control overScroll mode
overScrollMode?: 'always' | 'always-if-content-scrolls' | 'never';

// Snap to page boundaries?
pagingEnabled: boolean = false; // iOS only
snapToInterval: number = undefined; // iOS only

// Is scrolling enabled?
scrollEnabled: boolean = true;

// how often (in milliseconds) between scroll events?
scrollEventThrottle: number = undefined;

// If true, this scroll bar scrolls to the top when the user
// taps on the status bar.
scrollsToTop: boolean = false; // iOS only

// Should the indicator be displayed?
showsHorizontalScrollIndicator: boolean = [same as horizontal];
showsVerticalScrollIndicator: boolean = [same as horizontal];

// See below for supported styles
style: RX.ViewStyleRuleSet | RX.ViewStyleRuleSet[] = [];
```

## Styles
[**Flexbox Styles**](/reactxp/docs/styles.html#flexbox-style-attributes)

[**View Styles**](/reactxp/docs/styles.html#view-style-attributes)

[**Transform Styles**](/reactxp/docs/styles.html#transform-style-attributes)

## Methods
TODO: Document measurement and scroll Methods

