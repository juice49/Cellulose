# Cellulose

Cellulose is a small, mixin based grid system made with the [Stylus CSS preprocessor](http://learnboost.github.io/stylus).

## Configuration

Before using Cellulose, you must pass a configuration to the `Cellulose` function.

	Cellulose({
		colCount: 12,
		maxWidth: 1140px
	})

## Usage

	@import cellulose
	
	Cellulose({
		colCount: 12,
		maxWidth: 1140px
	})
	
	.widget-narrow
		cellulose_span(6)
	
		@media screen and (min-width: 400px)
			cellulose_span(12)

## Why Mixins?

Typically CSS grid systems will provide `.span*` classes that are applied to an element's class attribute. These columns will fold to a single column at a width specified by the framework. Using mixins means that we can treat all components independently. Not only do components fold at a width defined by the developer, they can switch to different spans at varying widths.

## Why inline-block?

There are a handful of reasons to use inline-block for columns rather than floats.

- Elements of varying height can be positioned alongside each other nicely using the `vertical-align` property (Cellulose sets this to `top` by default).

- No need to worry about clearing floats. This makes 'columnising' elements at varying widths more straight forward.

### What about those pesky gaps between inline-block elements?

Personally I use [Jade](http://jade-lang.com). It's a beautiful and, in my opinion, more efficient way of authoring HTML that has the additional benefit of compiling to compacted whitespace-less HTML - leaving inline-block elements flush.

If you write your HTML neat (as in Vodka), you'll need to put your column elements on the same line OR comment out the whitespace between them. Cellulose won't work otherwise. I'm sorry.

## Cellulose?

*An insoluble substance that is the main constituent of plant cell walls, a tough, usually flexible but sometimes fairly rigid layer that surrounds some types of cells.*