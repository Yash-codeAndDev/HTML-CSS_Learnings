### Selectors

* Selector select:not([multiple]) targets *select* elements that do not have the multiple attribute
    -   ```css
        select:not([multiple]){
          display:block;
          -webkit-appearance: none;
          appearance: none;
        }
        ```
