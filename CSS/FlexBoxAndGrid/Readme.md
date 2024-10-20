# FlexBox

* **FlexBox** : It CSS layout model designed to help you align and distribute space among items within a container, even when their sizes are unknown or dynamic. It makes it easier to create flexible and responsive layouts.

* **FlexBox Container :** The element on which ```display: flex (or inline-flex)``` is applied. This container becomes a flex container, and its direct children (flex items) are laid out along a flex line (which can be a row or a column, depending on the direction).
* **FlexItems :** The immediate children of a flex container. These items will align and adjust their sizes based on the flex properties applied to both the container and the items themselves.

* ## FlexBox Properties
* 1. On FlexContainer
       1. **display** :
          - *flex or inline-flex* : Defines a flex container.
          - *flex* makes the container a block-level flex container.
          - *inline-flex* makes the container inline but still flex-enabled.
          - ```css
                .container{
                  display : flex;
                  // display : inline-flex;
                }
            ```
       2. **flex-direction** :
          - Determines the direction of the flex items inside the flex container.
          - *row* (default): Items are placed in a horizontal line, left to right.
          - *row-reverse* : Items are placed in a horizontal line, right to left.
          - *column* : Items are placed in a vertical line, top to bottom.
          - *column-reverse* : Items are placed in a vertical line, bottom to top.
          - ```css
              .container{
                flex-direction : column; 
              }
            ```
            
       3. **flex-wrap** :
          - Controls whether flex items should wrap to the next line if there's not enough space.
          - *nowrap* (default): All flex items are placed on one line.
          - *wrap* : Flex items wrap onto multiple lines from top to bottom.
          - *wrap-reverse* : Flex items wrap onto multiple lines from bottom to top.
          - ```css
              .container{
                  flex-wrap: wrap;
                }
            ```


* 2. On FlexItems
     1. **flex-grow** : Defines how much a flex item should grow relative to the other flex items in the container when extra space is available. Default is 0.
        - If all items have flex-grow: 1, they will take up the available space equally.
        - If one item has flex-grow: 2, it will take up twice as much space as an item with flex-grow: 1.
     2. **flex-shrink** : Defines how much a flex item should shrink relative to the other flex items in the container when space is tight. Default is 1 (items will shrink if needed).
        - If an item has flex-shrink: 0, it will not shrink.
     3. **flex-basis** : Defines the initial size of a flex item before any growing or shrinking happens. It can be a length (e.g., 200px) or auto (the default).
        - When set, it acts as the item's preferred size, with space being adjusted afterward if there's extra or less room.
     4. **flex** : A shorthand property for flex-grow, flex-shrink, and flex-basis.
        - The typical format is flex: [grow] [shrink] [basis];.  
        - ```css
              .item {
                flex: 1 0 150px; /* grow: 1, shrink: 0, basis: 150px */
              }
          ```
