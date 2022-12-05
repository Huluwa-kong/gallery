# ECS759P 
若您有关于此文件夹下任何作业的任何需求，可添加vx：codingtutor 或者qq：122929048

若您有关于此文件夹下任何作业的任何需求，可添加vx：codingtutor 或者qq：122929048

若您有关于此文件夹下任何作业的任何需求，可添加vx：codingtutor 或者qq：122929048


## ECS759P Artificial Intelligence:  Coursework 2
**Due date: 6 December 2022 at 10.00 am**

**最晚不超过5 December 2022 at 12.00 pm 都可接受此作业订单，保证分数、原创、唯一**

### 1 Introduction
The coursework is composed of two questions. The first is a writing exercise about logic and reasoning.
The second exercise is on classification and involves programming.
• Crystal clear (Logic problem): 50%
• Lost in the closet (Classification): 50%


### 2 Crystal clear (Logic problem)
Although you are looking for it everywhere, you cannot find your true love. A bit desperate, you
decide to see Madame Irma, the most famous (and serious) fortune teller of the city. On the entrance
you see a sign stating: Everything that I say must be proved to be believed. More perplexed than ever,
you still go inside. After glaring at you for some time, she looks into her crystal ball, which has a
strange glow, and says in a mysterious voice:
• You have a dog.
• The person you are looking for buys carrots by the bushel.
• Anyone who owns a rabbit hates anything that chases any rabbit.
• Every dog chases some rabbit.
• Anyone who buys carrots by the bushel owns either a rabbit or a grocery store.
• Someone who hates something owned by another person will not date that person.
The sentences you just heard reminds you of a person: Robin. But before you leave, she challenges
you with a conclusion:
• If the person you are looking for does not own a grocery, she will not date you.
Remembering the sentence at the entrance, you realise that what she has told you is true only if you
can prove her challenging conclusion. Since you do not want any awkward situation, you decide to
provide a proof for her conclusion before going to see Robin.
1. Express Madame Irma’s six statements into First Order Logic (FOL). Note: You can use two
constants: YOU and ROBIN.
This question carries 10% of the mark for this coursework.
2. Translate the obtained expressions to Conjunctive Normal Forms (CNFs, Steps 1-6 of Lecture
9: Logic). Show and explain your work.
This question carries 10% of the mark for this coursework.
3. Transform Madame Irma’s conclusion into FOL, negate it and convert it to CNF (Steps 1-6 of
Lecture 9: Logic). Show and explain your work.
This question carries 10% of the mark for this coursework.
4. Based on all the previously created clauses (you should have at least 7 depending on how you
split them), finalise the conversion to CNF (Steps 7-8 of Lecture 9: Logic) and provide a proof
by resolution that Madame Irma is right that you should go to see Robin to declare to her your
(logic) love. Show and explain your work, provide unifiers.
This question carries 20% of the mark for this coursework.
Note: Make sure to follow the order of steps for the CNF conversion as given in Lecture 9 and report
all the steps (state “nothing to do” for the steps where this is the case).

### 3 Lost in the closet (Classification)
You are an artist who secluded yourself for years to come up with the perfect design for a new brand
of clothes. However, your time off from civilisation was not so beneficial since you cannot distinguish
a T-shirt from a dress or a sneaker from a sandal any more. In order to address that issue, you choose
to train a Convolutional Neural Network (using PyTorch) that will help you identify each cloth to
match the perfect design you created. In order to train it, you decide to rely on the dataset fashion
MNIST (https://github.com/zalandoresearch/fashion-mnist).
You can access the data using the following lines:
...



## Artificial Intelligence: Coursework 1

Due date: 16 Nov 2022 at 10.00 am



1 Introduction
The coursework is composed of two parts, involving coding exercises:
• Agenda-based search: 60% + 2% extra
• Genetic algorithm: 40%
The total mark will be capped to 100%.
2 Agenda-based Search
This part of the coursework is intended to help you understand how the agenda-based search works
and to give you practice in its implementation.
You task is to build an AI route  nder using agenda-based search mechanism. You are given a data  le
(tubedata.csv) in CSV format with the London Tube map (which is not necessarily to be up-to-date
and complete). The Tube map is de ned in terms of a logical relation Tube \step". If you open the
data  le with any text editor, you will see the content of the  le as:
"Harrow & Wealdstone", "Kenton", "Bakerloo", 3, "5", "0"
"Kenton", "South Kenton", "Bakerloo", 2, "4", "0"
     
"Bank/Monument", "Waterloo", "Waterloo & City", 4, "1", "0"
Each row in the CSV  le represents a Tube \step" and is in the following format:
[StartingStation], [EndingStation], [TubeLine], [AverageTimeTaken], [MainZone],
