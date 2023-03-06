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

```mermaid
graph LR
    A[Make a program that plays any song]
    style A fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
```

Let's say when you try to solve the problem with AI, the program plays only simple songs. It does not play complex songs. You would color the box grey, as this problem was not solved with AI.

```mermaid
graph LR
    A[Make a program that plays any song]
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
```

To get to the point where you can solve this problem, you can "break down" this ent (Note: You can either break down the ent by yourself or with AI assistance).

Let's say you got to the point where you created the followings ents "Provide a WAV file" and "Program plays a WAV file". Let's add these ents to the diagram.  

```mermaid
graph LR
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    A[Make a program that plays any song]
    B[Provide a WAV file]
    C[Program plays a WAV file]
    A --> B
    A --> C
```

Let's say you decide to solve "Provide a WAV file" without AI assistance, you would color this box light-green (as shown in the key above).

Let's say you try to make a "Program that plays a WAV file" with AI assistance, and it works! Let's color this box green (as shown in the key above).

```mermaid
graph LR
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#ADFF2F,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#32CD32,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    A[Make a program that plays any song]
    B[Provide a WAV file]
    C[Program plays a WAV file]
    A --> B
    A --> C
```

Now you have solved these ents, let's try to solve the original ent. Let's say you simply put the two solutions together, and you confirm the problem is solved! You can also update the diagram.

```mermaid
graph LR
    style A fill:#ADFF2F,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#ADFF2F,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#32CD32,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    A[Make a program that plays any song]
    B[Provide a WAV file]
    C[Program plays a WAV file]
    A --> B
    A --> C
```

Note: In another scenario, you could have put the two solutions together with AI assistance to solve the problem, and you confirm it works! It would make this diagram.

```mermaid
graph LR
    style A fill:#32CD32,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#ADFF2F,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#32CD32,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    A[Make a program that plays any song]
    B[Provide a WAV file]
    C[Program plays a WAV file]
    A --> B
    A --> C
```

## Example 2 (Play any spreadsheet)

Let's use a harder and more innovative example. This example is based on a real life problem and solution! 

Imagine you want to play a CSV file (spreadsheet file), where that CSV contains a representation of a song. Let's create the following ent.

```mermaid
graph LR
    A[Make a program that plays a song from a spreadsheet]
    style A fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
```

Let's say you try to solve this problem directly with an AI, and it doesn't work. Furthermore, you have no idea how you can even represent a music file using CSV. 

```mermaid
graph LR
    A[Make a program that plays a song from a spreadsheet]
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
```

Let's break down this ent into two ents "Convert a song into CSV" and "Play CSV"

```mermaid
graph LR
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    A[Make a program that plays a song from a spreadsheet]
    B[Convert a song into CSV]
    C[Play CSV]
    A --> B
    A --> C
```

Let's say you want to solve "Convert a song into CSV" first. You try to solve this problem with AI assistance, but you have no solution here. You come up with the following ents "Provide a WAV file" and "Convert WAV to CSV" to CSV.

```mermaid
graph LR
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style D fill:#fff,stroke:#4d4d4,stroke-width:2px,rounded:10px
    style E fill:#fff,stroke:#4d4d4,stroke-width:2px,rounded:10px
    A[Make a program that plays a song from a spreadsheet]
    B[Convert a song into CSV]
    C[Play CSV]
    D[Provide a WAV File]
    E[Convert WAV to CSV]
    A --> B
    A --> C
    B --> D
    B --> E
```

Similar to Example 1, you provide the CSV file manually. Also, you have performed some excellent prompting, your AI assistant was able to solve the problem of converting a WAV to CSV. Here is the updated EDD diagram.

```mermaid
graph LR
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style D fill:#ADFF2F,stroke:#4d4d4,stroke-width:2px,rounded:10px
    style E fill:#32CD32,stroke:#4d4d4,stroke-width:2px,rounded:10px
    A[Make a program that plays a song from a spreadsheet]
    B[Convert a song into CSV]
    C[Play CSV]
    D[Provide a WAV File]
    E[Convert WAV to CSV]
    A --> B
    A --> C
    B --> D
    B --> E
```

With these two solutions, you now solve "Convert a song into CSV".

```mermaid
graph LR
    style A fill:#A9A9A9,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style B fill:#ADFF2F,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style C fill:#fff,stroke:#4d4d4d,stroke-width:2px,rounded:10px
    style D fill:#ADFF2F,stroke:#4d4d4,stroke-width:2px,rounded:10px
    style E fill:#32CD32,stroke:#4d4d4,stroke-width:2px,rounded:10px
    A[Make a program that plays a song from a spreadsheet]
    B[Convert a song into CSV]
    C[Play CSV]
    D[Provide a WAV File]
    E[Convert WAV to CSV]
    A --> B
    A --> C
    B --> D
    B --> E
```

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

#### Q: Does EDD replace microservices or bounded contexts?

A: EDD can work with microservice and bounded contexts. Similar to how TDD and BDD works with these concepts.

P: EDD is going to change how people think about microservice and bounded contexts, especially with how focused EDD is on composables pieces of value delivery

<br>

#### Q: Does EDD replace TDD or BDD?

A: EDD is another option, it doesn't replace TDD or BDD directly (Reminder: EDD is a new way of solving problems in a post AI assistant world).

P: EDD starts with a summarization of the answer, so you will see pros/cons compared to BDD or TDD. In any case, EDD creates new advancements, when taking the best approach to solve a problem
