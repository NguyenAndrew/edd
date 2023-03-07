# EDD - Ent Driven Development

EDD is a problem solving process using ChatGPT (and any other future AI assistant). The 'E' in EDD stands for "ent", the core topic used in this process.

More clarifications can be seen in the following examples and FAQ.

## Table of Contents

* [Example 1 - Play any song](#example-1-play-any-song)
* [Example 2 - Play any spreadsheet](#example-2-play-any-spreadsheet)
* [FAQ](#predictions-and-faq-qap)

## Example 1 (Play any song)

Imagine you are trying to solve the following problem **"Make a program that plays any song"**.

<br>

Let's start with a diagram that contains an ent, and assume the following:
* White Box - Unsolved
* Grey Box - Unsolved, couldn't solve with AI
* Green Box - Solved with AI
* Light Green Box - (Mostly) Solved by a Human

<img src="images/Example1-1.png">

Let's say when you try to solve the problem with AI, the program plays only simple songs. It does not play complex songs. You would color the box grey, as this problem was not solved with AI.

<img src="images/Example1-2.png">

To get to the point where you can solve this problem, you can "break down" this ent (Note: You can either break down the ent by yourself or with AI assistance).

Let's say you got to the point where you created the followings ents "Provide a WAV file" and "Program plays a WAV file". Let's add these ents to the diagram.  

<img src="images/Example1-3.svg">

Let's say you decide to solve "Provide a WAV file" without AI assistance, you would color this box light-green (as shown in the key above).

Let's say you try to make a "Program that plays a WAV file" with AI assistance, and it works! Let's color this box green (as shown in the key above).

<img src="images/Example1-4.svg">

Now you have solved these ents, let's try to solve the original ent. Let's say you simply put the two solutions together, and you confirm the problem is solved! You can also update the diagram.

<img src="images/Example1-5.svg">

Note: In another scenario, you could have put the two solutions together with AI assistance to solve the problem, and you confirm it works! It would make this diagram.

<img src="images/Example1-6.svg">

Example 1 is now solved!

## Example 2 (Play any spreadsheet)

Let's use a harder and more innovative example. This example is based on a real life problem and solution! 

Imagine you want to play a CSV file (spreadsheet file), where that CSV contains a representation of a song. Let's create the following ent.

<img src="images/Example2-1.svg">

Let's say you try to solve this problem directly with an AI, and it doesn't work. Furthermore, you have no idea how you can even represent a music file using CSV. 

<img src="images/Example2-2.svg">

Let's break down this ent into two ents "Convert a song into CSV" and "Play CSV".

<img src="images/Example2-3.svg">

Let's say you want to solve "Convert a song into CSV" first. You try to solve this problem with AI assistance, but you have no solution here. You come up with the following ents "Provide a WAV file" and "Convert WAV to CSV".

<img src="images/Example2-4.svg">

Similar to Example 1, you provide the CSV file manually. Also, you have performed some excellent prompting, your AI assistant was able to solve the problem of converting a WAV to CSV. Here is the updated EDD diagram.

<img src="images/Example2-5.svg">

With these two solutions, you now solve "Convert a song into CSV".

<img src="images/Example2-6.svg">

Let's solve "Play CSV" next. You try to solve this problem with AI assistance, but you have no solution here. You come up with the following ents "Convert CSV to WAV" and "Play WAV".

<img src="images/Example2-7.svg">

Let's say you try solve "Convert CSV to WAV" and "Play WAV" with AI assistance, and it works! Awesome, these probably worked because of the AI knowing about our prior problems and solutions! Here is the updated diagram.

<img src="images/Example2-8.svg">

Let's say you try to solve "Play CSV" with AI assistance again. Although you could have done this manually, now with the prior solution context, the AI assistance solves the problem quickly! Here is where the diagram is now.

<img src="images/Example2-9.svg">

We can now solve the original ent, which looks like the following.

<img src="images/Example2-10.svg">

Additionally, now that we have more understanding based on our EDD Diagram, we can also update the diagram to be the following.

<img src="images/Example2-11.svg">

Example 2 is now solved!

## Predictions and FAQ (QAP)
* Q: is Question
* A: is Answer
* P: is Predicion

<br>

#### Q: What is EDD?
A: EDD is Ent Driven Development.

<br>

#### Q: What is Ent?
A: Ent is a new word based on the word "Entity". Ent represents the composable blocks of value that can be delivered either with/without AI assistance.

<br>

#### Q: Why not just use the word entity?

A: Ent is shorter to say, and I didn't want to cause confusion by using the word entity, which has multiple definitions today.

<br>

#### Q: Why did you create EDD?

A: To establish a reusable way of making cool stuff in a post AI assistant world.

<br>

#### Q: What "AI assistants" do you mean here?

A: Referring ChatGPT and GitHub CoPilot, and includes any other AI assistants that help solve problems.

P: I believe there are going to be different names for the AI assistants in the future. For this reason, I wanted to keep "AI Assistant" generic.

<br>

#### Q: Why now? Surely someone would have created this before?

A: The key difference is that AI assistants can now help solve problems quickly, offsetting the costs of creating EDD diagrams and making ents. Although there wasn't a need before, going forward the identification of ents will not only solve problems quicker, but also help drive future improvement through identifing problems solved with/without AI.

<br>

#### Q: Where does refactoring and unit testing fit within EDD?

A: Refactoring and unit testing, are just additional ents that you create. Here is an EDD diagram example:

```mermaid
graph LR
    style A fill:#ADFF2F,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#ADFF2F,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#32CD32,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style D fill:#ADFF2F,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style E fill:#32CD32,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    A[Make an enterprise program that plays any song]
    B[Provide a WAV file]
    C[Program plays a WAV file]
    D[Program is Unit Tested]
    E[Program is Refactored to match best standards]
    A --> B
    A --> C
    A --> D
    A --> E
```

<br>

#### Q: If there is an API or library that solves one of my ents, can I consider it automatically solved?

A: No. You should prove your solution succesfully solves the problem, and gets the correct output. There could be a mismatch with the data you have, and the API or library you are interacting with, which is why the ent can't be considered automatically solved.

<br>

#### Q: Does EDD replace microservices or bounded contexts?

A: EDD can work with microservice and bounded contexts. Similar to how TDD and BDD works with these concepts.

P: EDD is going to change how people think about microservice and bounded contexts, especially with how focused EDD is on composables pieces of value delivery

<br>

#### Q: Does EDD replace TDD or BDD?

A: EDD is another option, it doesn't replace TDD or BDD directly (Reminder: EDD is a new way of solving problems in a post AI assistant world).

P: EDD starts with a summarization of the answer, so you will see pros/cons compared to BDD or TDD. In any case, EDD creates new advancements, when taking the best approach to solve a problem
