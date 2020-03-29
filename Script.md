## Funny intro (33s)

> Display first vide of trapped man/woman then short clip of a feast

These quarantined days the only thing that's keeping my hopes up is food. So Juli and I decided that after all this is over we shall throw a feast for everyone to celebrate. 

> Play music

But what should we cook we pondered?

To answer this question we set ourselves on a path to create the best recipe to ever exist. As soon to be data scientists we knew if we wished to suceed in our quest we shall seek the power of data. 

> Display video of going to kaggle and searching 'recipes'

To find said data we used our extremely thorough and advanced research skills that we've only been able to master through years of practice.

Aha, there it is, just what we wanted. A dataset with lots of recipes.

## Outline (9s)

To build this perfect recipe we had to determine the following: 

* A type of cuisine
* A name for the recipe
* Ingredients for the recipe
* The steps to follow to cook this recipe

## Type of cuisine (13s)

In our dataset we have a number of tags for each recipe. To explore the evolution in popularity of these tags we plot the % of recipes containing each of them.

> Display `tags_yearly.png` 

We observe that `healthy` and `vegetarian` appear to show the most consistently high popularity so we decide we will use these. 

## Name for the recipe (34s)

Our next step is deciding the name. We thought about going for 'The best recipe ever' but decided to go for something a bit more descriptive. 

We  analyze the names of the most and least succesful recipes. We measured this using two metrics, popularity (measured as number of votes), and positive popularity (measured as average rating). 

> Display `boxplot.png`

We then split recipes into two groups consisting of the bottom and top quartiles for each of these metrics and explore which words are most characteristic of each.

> Display `name_popularity_good`.png, `name_popularity_bad.png`,  `name_ppopularity_bad.png` and  `name_ppopularity_bad.png`. In a grid. If you want you can point at the words I am mentioning while I do.

As we can see there are some mixed signals, positive popularity indicates we should use salad and fruit but popularity tells us those aren't good keywords. After analyzing these wordclouds thoroughly we decide our name will be 'Roasted potato with garlic and bread'.

## Ingredients (50s)

Now we need to decide which ingredients to use. Potato, garlic and bread seems to be an obvious choice. But those might not be enough since we've observed that the best recipes (with a score of at least 4.5 and at least 50 votes) tend to have 9 ingredients.

To find our next 6 ingredients we take 3 approaches. 

First we look into most popular ingredients and add the best two, salt and olive oil. 

> Display `ing_yearly.png` 

Next we look at the popularity evolution of non-condiment ingredients and decide to add tomato and onion to our recipe due to their high and continued popularity.

We also want to add non-controversial ingredients that everyone will love so we fit a logistic regression to predict the standard deviation of a recipe using its ingredients. From this we can extract high weights (controversial) and low weights (non-controversial)

> Display `reg_std_low.png` `reg_std_high.png` 

Apparently pectin is an extremely controversial ingredient, and rightfully so, what the (censored beep) is that? I swear we shouldn't have used an american dataset. 

Anyway, it seems like agave syrup and black vinegar are loved by everyone so I guess they're in. 

And the last approach was asking ourselves how we can try to fix this mess. Maybe some thyme and rosemary can round this up well. 

> Display pic of thyme and rosemary

## Steps to follow (11s)

By now we realized maybe AI isn't ready to cook yet, so we decided for the steps we'll just use the biggest Neural Network available (your brain) so just follow your instincts I guess.

> Display picture of brain

Please do not try this at home unless you're american and/or have a terrible taste for food.

> Conclusion slide
>
> Display [pic](https://www.taste.com.au/recipes/garlic-bread-potato-bake-recipe/5yfd3kim)  