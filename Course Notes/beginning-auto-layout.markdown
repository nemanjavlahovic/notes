## Beginning Auto Layout

by Jerry Beers on raywenderlich.com


### Chapter 2: Autoresizing Masks
	* Autoresizing masks define the relationship between a view and its superview, by defining 6 attributes: left, right, top and bottom margins, and width and height. Each can be defined as fixed or flexible.
	* Behind the scenes auto layout translates autoresizing masks to constraints.
	* UIView property translatesAutoresizingMaskIntoConstraints is by default set to true, if a view is added in code. However, if you configure a view in IB, this property will be set to true or false depending on whether it has constraints or not.
	* In attributes inspector section in IB, autoresizing shows you red/white views, red being your view and white superview.
	* Use assistant editor and preview for checking multiple device sizes at once.
	* When running your app, you can run view debugger and see view hierarchy clearly in left navigation section.

### Chapter 3: Introducing Stack views
	* Stack views can arrange its subviews and align either horizontally or vertically.
	* In the direction of an axis (X/Y), there are two properties that control how subviews are positioned: spacing and distribution.
	* Spacing is just the minimum spacing between views.
	* Distribution is how the views are arranged along the axis.
	* Alignment is a property that determines how subviews are aligned.
	* You can drag & drop items in a stack view to change order of subviews, which is one of the greatest things about stack views. Doing this with constraints is painful.
	*  Xcode 8 note: don't worry about the IB warning for subviews in stack view; this is a known Xcode bug.

### Chapter 4: Intrinsic Content Size
	* Content hugging: don't want to grow.
	* Content compression resistance: don't want to shrink.

### Chapter 5: Nesting Stack Views
	* Default value is fill. This will use intrinsic content size of views but grow/shrink one depending on compression resistance priority.
	* Fill equally makes all the subviews in stack view equal along the axis.
	* Fill proportionally starts with intrinsic content size, but grows/shrinks in proportion with their intrinsic content size.
	* Equal spacing, obviously, makes spacing between views equal.
	* Equal centering makes spacing from center to center equal.
	* Alignment specifies how to align subviews along the axis (leading/center/trailing).

### Chapter 6: Introducing Constraints
	* Auto Layout Formula: attribute1 = multiplier x attribute2 + constant
	* Leading and trailing are used as left and right to support right to left languages.
