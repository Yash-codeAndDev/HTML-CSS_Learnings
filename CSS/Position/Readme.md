# Position

* *position* property determines how an element is placed in the layout of the web page.
    - There are five possible position:
        1. static(default)
        2. relative
        3. absolute
        4. fixed
        5. sticky

1. **static**
   - By default, all elements in a web page are positioned statically. This means they are placed in the document flow in the order they appear in the HTML, and the layout engine positions them from top to bottom, left to right.
   -  Static elements cannot be repositioned using *top, right, bottom, or left* properties because those properties do not apply.
   -  ```css
          div{
            position : static;
          }
      ```
2. **relative**
   - When an element is positioned as relative, it behaves similarly to static but with one key difference: you can modify its position relative to its original place using top, right, bottom, or left.
   - Even though the element is visually moved, its original space in the layout is still reserved, which means other elements around it will behave as though the element is still in its original position.
    - ```css
          div {
              position: relative;
              top: 20px;  /* Moves the element 20px down */
              left: 10px; /* Moves the element 10px to the right */
            }
      ```

3. **Absolute**
   - An element with position: absolute is removed entirely from the document flow, meaning other elements will behave as if it does not exist.
   - The element is positioned relative to the nearest positioned ancestor (i.e., the closest ancestor element with a position other than static). If there is no such ancestor, the element will be positioned relative to the document body.
   - ```css
         div {
          position: absolute;
          top: 50px;  /* Moves the element 50px down from the nearest positioned ancestor */
          right: 20px; /* Moves the element 20px from the right */
        }
     ```
4. **Fixed**
   - A fixed element is also removed from the document flow, but unlike absolute positioning, it is always relative to the viewport (the visible portion of the web page). This means it stays in the same position even when the page is scrolled.
   - It is locked in position and will not move regardless of user scrolling.
   - ```css
         div {
              position: fixed;
              top: 0;
              right: 0;
         }
     ```
5. **Sticky**
   - Sticky positioning is a mix of relative and fixed positioning. An element is positioned relative to its container (like relative) but becomes fixed at a specified position (like fixed) when the user scrolls past a certain point.
   - Before the element reaches the specified scroll position, it behaves like a relatively positioned element. Once it crosses the threshold, it becomes fixed to the defined position in the viewport until its container is out of view.
   - ```css
         div {
          position: sticky;
          top: 10px; /* Becomes fixed when it scrolls 10px from the top */
        }
     ```
