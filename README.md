# Cellulose

Cellulose is a small mixin based grid system developed to work with the [Stylus CSS preprocessor](http://learnboost.github.io/stylus). This is very early work - a foray into a "semantic" grid system that encourages the user to avoid span* classes. Minimal. Untested. Contributions welcome.


## Configuration

These configuration variables should be set before you import Cellulose. I think in the future it'd be handy to pass in these variables to each instance.

    /**
     * ColCount (required)
     *
     * How many columns should the grid span?
     */
    colCount = 12
    
    /**
     * MaxWidth (optional)
     *
     * The maximum width of the grid. Applied to
     * elements that span the full grid width - which
     * are assumed to be containers / rows.
     */
    maxWidth = 1140


## Example

    @import cellulose

    colCount = 12

    .widget-narrow
    	span(3)
    	
    	@media screen and(min-width: 400px)
    		span(4)
    		

## Cellulose?

*An insoluble substance that is the main constituent of plant cell walls, a tough, usually flexible but sometimes fairly rigid layer that surrounds some types of cells.*