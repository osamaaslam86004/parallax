### Horizontal parallax (enhanced-horizontal.html)

1. What is layer?
   The term layer refers to each <img> element selected using the querySelectorAll(".ukiyo") statement.
   These are the elements that have the ukiyo class applied (e.g., class="ukiyo layer1").
   In simpler terms, layer is a single parallax image from the list of all .ukiyo elements.

2. What is index?
   The index is the position of the current layer in the NodeList returned by querySelectorAll.
   The forEach loop provides the index as the second parameter, starting from 0 for the first element.
   For example:

```
const layers = document.querySelectorAll(".ukiyo");

layers.forEach((layer, index) => {
  console.log(layer, index); // Logs each <img> element and its position in the list
});
```

If there are three <img> elements in the .ukiyo list:

For the first <img> (with class="ukiyo layer1"), index will be 0.
For the second <img> (with class="ukiyo layer2"), index will be 1.
For the third <img> (with class="ukiyo layer3"), index will be 2.
How layer and index are used:
In the forEach loop:

```
new Ukiyo(layer, {
  scale: 1.5 + index * 0.5, // Adjust the zoom based on the index
  speed: 2 - index * 0.5,  // Adjust the speed based on the index
  willChange: true,
});
```

#### scale:

The zoom effect for each image (layer) increases with its index.
For the first layer (index = 0), the scale is 1.5 + 0 _ 0.5 = 1.5.
For the second layer (index = 1), the scale is 1.5 + 1 _ 0.5 = 2.0.
For the third layer (index = 2), the scale is 1.5 + 2 \* 0.5 = 2.5.

#### speed:

The parallax speed for each image decreases with its index.
For the first layer (index = 0), the speed is 2 - 0 _ 0.5 = 2.0.
For the second layer (index = 1), the speed is 2 - 1 _ 0.5 = 1.5.
For the third layer (index = 2), the speed is 2 - 2 \* 0.5 = 1.0.
By varying these values, you achieve distinct effects for each parallax layer, creating a more dynamic and immersive visual experience.

#### Summary

1. layer: Refers to each parallax <img> element.
2. index: Represents the position of the current layer in the list, starting from 0.
3. Using index, you can adjust properties (like scale and speed) dynamically to create unique effects for each layer.
