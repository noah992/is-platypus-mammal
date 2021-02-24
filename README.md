# is-platypus-mammal


This repo is created for [my medium post](https://noah992.medium.com/is-platypus-mammal-data-science-8934dd9a499c)

* [code](https://github.com/noah992/is-platypus-mammal/blob/main/code/is-platypus-mammal.ipynb)

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
|animal_name|int|name of the animal|
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
