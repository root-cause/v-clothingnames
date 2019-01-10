# v-clothingnames

GXT entries and human readable names of GTA V clothing items.

Many items have "NO_LABEL" and "NULL" as their names, which probably means they aren't available for purchase in GTA Online clothes shops OR they're old enough to have their names hardcoded in game scripts.

Files without a prefix (e.g. masks.json) are the clothing items for both **mp_m_freemode_01** and **mp_f_freemode_01** models. (aka for SET_PED_COMPONENT_VARIATION)

Files prefixed with **male_** are the clothing items for **mp_m_freemode_01** model. (aka for SET_PED_COMPONENT_VARIATION)

Files prefixed with **female_** are the clothing items for **mp_f_freemode_01** model. (aka for SET_PED_COMPONENT_VARIATION)

Files prefixed with **props_male_** are the props for **mp_m_freemode_01** model. (aka for SET_PED_PROP_INDEX)

Files prefixed with **props_female_** are the props for **mp_f_freemode_01** model. (aka for SET_PED_PROP_INDEX)

Visit https://wiki.rage.mp/index.php?title=Clothes for preview images.

# JS Example

```js
// Getting the name of https://wiki.rage.mp/images/c/c2/Clothing_M_11_70.jpg
const maleTops = require("./male_tops.json");
const clothingID = 70;
console.log(`Name of the item: ${maleTops[clothingID][0].Localized}`); // Outputs: "Name of the item: Brown Leather Fur Jacket"

// List all variation names of the clothing above
Object.keys(maleTops[clothingID]).forEach(variation => {
    console.log(`Variation ${variation} - ${maleTops[clothingID][variation].Localized}`)
});

/*
    Outputs:
    Variation 0 - Brown Leather Fur Jacket
    Variation 1 - Tan Leather Fur Jacket
    Variation 2 - Black Leather Fur Jacket
    Variation 3 - Ochre Leather Fur Jacket
    Variation 4 - White Leather Fur Jacket
    Variation 5 - Leopard Leather Fur Jacket
    Variation 6 - Fall Leather Fur Jacket
    Variation 7 - Hunter Leather Fur Jacket
    Variation 8 - Gray Leather Fur Jacket
    Variation 9 - All Black Leather Fur Jacket
    Variation 10 - Burgundy Leather Fur Jacket
    Variation 11 - Dark Gray Leather Fur Jacket
*/
```
