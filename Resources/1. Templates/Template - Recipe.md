---
aliases: 
Created: <% tp.file.creation_date("YYYY-MM-DD") %>
Last Updated: <% tp.file.last_modified_date("YYYY-MM-DD") %>
tags:
  - recipe
Difficulty:
  - Easy
  - Medium
  - Hard
Preparation: <% tp.system.prompt("Preparation time (e.g., 30min)") %>
Cooking: <% tp.system.prompt("Cooking time (e.g., 1h 30min)") %>
Total: <% tp.system.prompt("Total time (e.g., 2h)") %>
Servings: <% tp.system.prompt("Number of servings") %>
Cost:
  - Low
  - Medium
  - High
Cuisine: <% tp.system.prompt("Cuisine (e.g., Italian, Mexican)") %>
Type:
- Vegetarian 
- Vegan 
- Gluten-free 
- Dairy-free 
- Paleo 
- Keto
Contains: 
- Beef 
- Pork 
- Poultry 
- Fish 
- Seafood 
- Other Meat # More explicit name 
- Vegetables 
- Fruit 
- Dairy 
- Eggs 
- Grains 
- Legumes 
- Nuts 
- Seeds
Dish:
 - Appetizer 
 - Main Course 
 - Side Dish 
 - Dessert 
 - Snack 
 - Breakfast 
 - Lunch 
 - Dinner
Rating:
  - ⭐
  - ⭐⭐
  - ⭐⭐⭐
  - ⭐⭐⭐⭐
  - ⭐⭐⭐⭐⭐
URL: <% tp.system.prompt("URL") %>
---
---

```
![[image]]
or
!["name"](link)
```

---

<%*
let title = tp.file.title
if (title.startsWith("Untitled")) { 
  title = await tp.system.prompt("Title"); 
}
await tp.file.rename(title);

-%>

Any preamble can go here.
## Ingredients
**Section 1**
- bulleted lists
- quantities at the start, e.g.:
- 180 grams butter
- 3 eggs

**Another section**
- Feel free to split your ingredients up
- and add notes underneath
- You don't need any bold headings if you don't want
- 15 of Another recipe, pre-made

## Kitchenware
* strumenti per la cucina
## Directions
> [!info] 
>  
To scale certain quantities in other sections e.g. in the directions, wrap them like `<span data-qty-parse>180 grams</span>`. You could also wrap a whole step in the same tags to parse all present quantities. In most recipes, quantities outside the ingredient lists don’t need to be scaled, but an example where it is useful using these `<span>` tags is shown below.
To stop a certain quantity from being scaled mistakenly, wrap it like 
`<span data-qty-no-parse>30 centimetres</span>`.

1. Numbered lists
2. Feel free to include any markdown you like in your steps
3. You can also split these up in sections, with bold or level 3+ headings

## Notes
Anything else you want can go here.

## Nutrition
Common when recipes are downloaded from the web
> [!info] 
>  prompt per Gemini/hugging face 
make a nutrient table, with micro and macro nutrient; I want a single markdown table with a division with macro and micro; based on 100g from this recipe:
## Food storage

## Source
1. <% tp.frontmatter.URL%>