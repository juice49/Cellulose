# Cellulose

Cellulose is a small, mixin based grid system made with the [Stylus CSS preprocessor](http://learnboost.github.io/stylus).

### Why Mixins?

Typically CSS grid systems will provide `.span*` classes that are applied to an element's class attribute. These columns will fold to a single column at a width specified by the framework. Using mixins means that we can treat all components independently. Not only do components fold at a width defined by the developer, they can switch to different spans at varying widths.

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
    		

## Cellulose?

*An insoluble substance that is the main constituent of plant cell walls, a tough, usually flexible but sometimes fairly rigid layer that surrounds some types of cells.*
