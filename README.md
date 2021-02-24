# is-platypus-mammal


This repo is created for [my medium post](https://noah992.medium.com/is-platypus-mammal-data-science-8934dd9a499c)

* [code](https://github.com/noah992/is-platypus-mammal/blob/main/code/is-platypus-mammal.ipynb)
* [data](https://github.com/noah992/is-platypus-mammal/tree/main/data)

## Summary

* Problem - Research what kind of animal cotegory a platypus is belong to
* Dataset - [Kaggle](https://www.kaggle.com/uciml/zoo-animal-classification)
* Conclusion - platypus is mammal

## Problem


Platypus is known as unique mammal. They have fluffy far and a beak so it sounds like one kind of bird? But they do not have wings but 4 legs. Are they mammal, even if most of mammals do not have a beak? Somehow, they give birth of eggs and they have cloaca which usually is shown in fish, birds, reptiles and amphibians for birth of eggs.

In recent conclusion, mammals are defined as animals which feed milk to grow up babies. Platypus has organs for milking so that they are categorized as one of mammals.

Besides that, I would like to know what category platypus is belong to in terms of data science.

I used `LogisticRegression` to make multinomial classification model and evaluated it with accuracy. This model gives you a result of what animal types an animal is with using animals features such below.

* Whether they have feather
* Whether they have eggs
* Whether they feed milk
* and more

After all I fed features of platypus then conclude what kind of animals they are.

## Dataset

I use a dataset which contains animals and its features downloaded from [Kaggle](https://www.kaggle.com/uciml/zoo-animal-classification)

Data dictionary

`animals`
|Column|Type|Description|
|-|-|-|
|animal_name|str|name of the animal|
|hair|int|whether they have hair|
|feathers|int|whether they have feather|
|eggs|int|whether they give birth of eggs|
|milk|int|whether they milk babies|
|airborne|int|whether they fly|
|aquatic|int|whether they live in water|
|predator|int|whether they eat other animals|
|toothed|int|whether they have teeth|
|backbone|int|whether they have backbone|
|breathes|int|whether they breathes|
|venomous|int|whther they have poison|
|fins|int|whether they have fins|
|legs|int|how many legs they have|
|tail|int|whether they have a tail|
|domestic|int|whether they make family|
|catsize|int|whether their size is close to a cat|
|class_type|int|animal class|

`animal_class`
|Column|Type|Description|
|-|-|-|
|Class_Number|int|animal class|
|Number_Of_Animal_Species_In_Class|int|see left|
|Class_Type|str|class of the animals|
|Animal_Names|str|name of the animal|

`animals` contains animals and its features. I used these features to train mutlinomial `LogisticRegression`. `animal_calss` contains actual categories for each animal.

I added unique features for platypus, which are `cloaca`, `webbed`, `beak`.

* `cloaca` - Organ which defecates eggs, urine and feces. This is usually found among fish, birds, reptiles, amphibians
* `webbed` - Webbed feet. Mostly found among birds, reptiles and amphibians
* `beak` - The one all birds have

I made 2 `DataFrame`. I used these to determine whether a platypus is mammal. I separated platypus by gender because only male platypus has poison on its claws. Venomous mammal is not common so that this might have significant effect.

* `platypus_female`
* `platypus_male`

### Result

Model
```lr = LogisticRegression(multi_class='multinomial', solver='newton-cg')```
This model make predictions between 1 and 7, and you can get the animal class from below table.

|Class_Number|Class_Type|
|-|-|
|1|Mammal|
|2|Bird|
|3|Reptile|
|4|Fish|
|5|Amphibian|
|6|Bug|
|7|Invertebrate|

My predicts at 96% accuracy with unseen data. I assume this is trustworthy.



|Platypus|Class Number|
|-|-|
|female|1|
|male|1|

## Conclusion

They both got `1` and which means they are mammal. `cloaca`, `webbed feet`, `beak`, and `venomous` are not so strong characteristics that they can determines wheter the animal is mammal.

In terms of data science, they are identified as mammal however this dataset was not very big so it could give different result with bigger dataset.

