### Selectors

* Selector ```select:not([multiple])``` targets *select* elements that do not have the multiple attribute
    -   ```css
        select:not([multiple]){
          display:block;
          -webkit-appearance: none;
          appearance: none;
        }
        ```
* Selector ```button span``` targets any <span> element that is inside a <p> (paragraph) element.
    -   ```css
        button span{
          color: green;
          font-style: italic;
        }
        ```
* Selector ```#styled input, #styled button``` targets two specific types of elements:    
    - Any ```<input>``` element that is inside an element with the ID styled.
    - Any ```<button>``` element that is inside an element with the ID styled.
    - ```css
      #styled input,#styled button {
          background-color: lightgray;
          border: 1px solid #000;
          padding: 10px;
      }
      ```
* Selector ```#styled input[type="submit"]:focus``` :
    - ```#styled```: Targets an element with the ID styled.
    - ```input[type="submit"]```: Targets any ```<input>``` element with type="submit" inside the ```#styled``` element.
    - ```button[type="submit"]```: Targets any ```<button>``` element with type="submit" inside the ```#styled``` element.
    - The ```:focus``` pseudo-class applies when the input or button is focused (for example, when clicked or tabbed into)
    - ```css
          #styled input[type="submit"]:focus,#styled button[type="submit"]:focus
          {
              border: 4px solid green;
          }  
        ```
