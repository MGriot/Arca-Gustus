```dataview
table dish-type as "Dish Type", rating, difficulty, file.cday as "Creation Date"
from "Recipes"
where file.name!= "template"
```
