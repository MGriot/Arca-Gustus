---
date: <% tp.date.now("YYYY-MM-DD") %>
---

## Ingredient Information
* **Type:** <%* let ingredientType = await tp.system.prompt("Ingredient Type (e.g. spice, herb, dairy, etc.)") %>
* **Description:** <%* let ingredientDescription = await tp.system.prompt("Brief description of the ingredient") %>
* **Substitutions:** <%* let ingredientSubstitutions = await tp.system.prompt("List of possible substitutions for this ingredient") %>
* **Allergens:** <%* let ingredientAllergens = await tp.system.prompt("List of common allergens associated with this ingredient") %>
* **Storage:** <%* let ingredientStorage = await tp.system.prompt("Instructions for storing this ingredient") %>
* **Shelf Life:** <%* let ingredientShelfLife = await tp.system.prompt("Typical shelf life of this ingredient") %>
## Nutrition Information
* **Calories per 100g:** <%* let ingredientCalories = await tp.system.prompt("Calories per 100g of this ingredient") %>
* **Macronutrient Breakdown:**
    + Protein: <%* let ingredientProtein = await tp.system.prompt("Protein content per 100g of this ingredient") %>
    + Fat: <%* let ingredientFat = await tp.system.prompt("Fat content per 100g of this ingredient") %>
    + Carbohydrates: <%* let ingredientCarbohydrates = await tp.system.prompt("Carbohydrate content per 100g of this ingredient") %>
* **Micronutrient Information:**
    + Vitamin A: <%* let ingredientVitaminA = await tp.system.prompt("Vitamin A content per 100g of this ingredient") %>
    + Vitamin C: <%* let ingredientVitaminC = await tp.system.prompt("Vitamin C content per 100g of this ingredient") %>
    + Calcium: <%* let ingredientCalcium = await tp.system.prompt("Calcium content per 100g of this ingredient") %>
    + Iron: <%* let ingredientIron = await tp.system.prompt("Iron content per 100g of this ingredient") %>

## Sources
* <%* let ingredientSources = await tp.system.prompt("List of sources for this ingredient information") %>

## Notes
* <%* let ingredientNotes = await tp.system.prompt("Any additional notes about this ingredient") %>