1. How long did you spend on the coding test? What would you add if you had more time? If you didn't spend much time on it, use this to explain what you would have done.

I spent 1hr30m on the coding test. I was in the process of adding filter views, to sort by attributes, although I am not sure how you could sort by attribute as the types aren't easily sorted, I would have to assess when you click on color, does it only show the ones that contain the attribute color? how is this sorted, Alphabetically. I would've set the type value and looped through the mapped list to only show the products with that attribute present. Furthermore I would have made the the pricing dynamic - by checking to see whether the original price is less than the final price, this indicates the item is on sale, you would either conditionally render the price regarding this, meaning that the product list doesn't have to be specific to sale items. Add a hamburger menu although this isn't specified. Pagination would be done by replacing the page number at the end of the url and loading the content.

2. How would you trackdown a JS performance issue in production? Have you ever had to do this?

If you're using a framework there are various dev tools you can utilise in chrome to show you performance specific issues regarding various languages. Outside of this the performance & network tab allow you to pinpoint where you are suffering from jank. You can also use fps trackers that show you in realtime when framerates may drop.

3. What is your favourite feature of any of the lanuguages you used? Describe a situation where you have used this feature.

CSS transitions - They are very powerful when creating simple or even fairly complicated transitions, they usually don't suffer from performance issues (depending on what you're trying to transition) and allow you to perform a variety of animations with little input.

4. Describe yourself in JSON.

{
"eik_torben_hunter": [
    {
      "id": "22",
      "name": "Eik Hunter",
      "childhood_nickname": "Spikey",
      "gender": "Male",
      "height": "5ft11"
      "weight": "78"
      "description": "A Straight-talking, fun and caring person with a very creative and attention to detail orientated ethos",
      "personality": [
        "careful",
        "caring",
        "kind",
        "brave"
      ]
    }
  ]
}
