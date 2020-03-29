## Funny intro

Covid has us all enclosed at home and for me personally, the only thing that's keeping my hopes up is food. So Juli and I decided that after all this is over we shall throw a feast for everyone to celebrate. 

But what should we cook we pondered?

To answer this question we set ourselves on a path to create the best recipe to ever exist. As soon to be data scientists we knew if we wished to suceed in our quest we shall seek the power of data. 

> Display video of going to kaggle and searching 'recipes'

For this we used our extremely thorough and advanced research skills that we've only been able to master through years of practice.

Aha, there it is, just what we wanted. A dataset with 180k recipes with around 700k recipe reviews from Food.com let's dive right in.

## Outline

To build this perfect recipe we had to determine the following: 

* A type of cuisine
* A name for the recipe
* Ingredients for the recipe
* The steps to follow to cook this recipe

## Type of cuisine

In our dataset we have a number of tags for each recipe. These tags can mean many different things, there's some that seem to be mostly just keywords to receive more searches online (`preparation`,  `cuisine`, `main-ingredient`) while others did convery some information about the recipe (`vegetarian`, `healthy`, `italian`). We decided to focus on this second group and specifically on the most popular out of these: `vegetarian`, `healthy`, `italian`, `begginer-cook`, `inexpensive` and `european`.

> Display `tags_yearly.png` 

To explore the evolution in popularity of these tags we plot the % of recipes containing each of them. We observe that `healthy` and `vegetarian` appear to show the most consistently high. We can also observe however a sharp decrease in popularity for most tags on the later years.

However, if we plot the total number of recipes and number of tags per recipe over time.

> Display `tags_per_recipe.png` and `tags_yearly_total.png` 

We can observe a sharp drop off in both of these values which is probably the reason all tags seem to reduce in popularity. As `healthy` and `vegetarian` show the most constant and high popularity we decide to focus on these two.

## Name for the recipe

Our next step is deciding the name for our recipe. We thought about going for 'The best recipe ever' but decided to go for soemthing more descriptive. 

For this we decided to analyze the names of the most succesful and least succesful recipes. We measured this using two metrics, popularity (measured as number of votes), and positive popularity (measured as average rating). 

> Display `boxplot.png`

We then split into two groups consisting of the bottom and top quartiles for each of these metrics and explore which words are most characteristic of each of these groups. This means we substracted the relative frequency of words in bad recipes from good recipes and the other way around and came up with the following wordclouds.

For popularity:

> Display `name_popularity_good`.png, `name_popularity_bad.png`,  `name_ppopularity_bad.png` and  `name_ppopularity_bad.png`. In a grid. If you want you can point at the words I am mentioning while I do.

As we can see there are some mixed signals, positive popularity indicates we should use salad and fruit but popularity tells us those aren't good keywords. After analyzing these wordclouds we decide our name will be 'Roasted potato and garlic with bread'.

## Ingredients

Now we need to decide which ingredients to use for our 'Roasted potato and garlic with bread recipe'. Potato, garlic and bread seems to be an obvious choice. But those might not be enough since we've observed that the best recipes (with a score of at least 4.5 and at least 50 votes) have an average of 9 ingredients so that's the number we're going for.   

To find our next 6 ingredients we take 3 approaches. First we look into most popular ingredients and add two of them, salt and olive oil. Next we 