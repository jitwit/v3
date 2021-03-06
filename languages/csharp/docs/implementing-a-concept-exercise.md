# How to implement a C# concept exercise

This document describes how to implement a concept exercise for the C# track. As this document is generic, the following placeholders are used:

- `<SLUG>`: the name of the exercise in kebab-case (e.g. `anonymous-methods`).
- `<NAME>`: the name of the exercise in PascalCase (e.g. `AnonymousMethods`).

Before implementing the exercise, please make sure you have a good understanding of what the exercise should be teaching (and what not). This information can be found in the exercise's GitHub issue. Having done this, please read the [C# concept exercises introduction][docs-exercises-concept].

To implement a concept exercise, the following files must be created:

<pre>
languages
└── csharp
    └── exercises
        └── concept
            └── &lt;SLUG&gt;
                ├── .docs
                |   ├── instructions.md
                |   ├── introduction.md
                |   ├── hints.md
                |   └── after.md (optional)
                ├── .meta
                |   ├── config.json
                |   └── Example.cs
                ├── &lt;NAME&gt;.cs
                ├── &lt;NAME&gt;.csproj
                └── &lt;NAME&gt;Test.cs
</pre>

## Step 1: adding track-specific files

These files are specific to the C# track:

- `<NAME>.cs`. the stub implementation file, which is the starting point for students to work on the exercise.
- `<NAME>.csproj`: the C# project file.
- `<NAME>Test.cs`: the test suite.
- `.meta/Example.cs`: an example implementation that passes all the tests.

## Step 2: adding common files

How to create the files common to all tracks is described in the [how to implement a concept exercise document][docs-general-how-to-implement-a-concept-exercise].

## Step 3: add analyzer (optional)

Some exercises could benefit from having an exercise-specific [analyzer][csharp-analyzer]. If so, please check the [analyzer document][csharp-analyzer] for details on how to do this.

## Step 4: custom representation (optional)

Some exercises could benefit from having an custom representation as generated by the [C# representer][csharp-representer]. If so, please check the [representer document][csharp-representer] for details on how to do this.

## Inspiration

When implementing an exericse, it can be very useful to look at already implemented C# exercises like the [strings][concept-exercise-strings], [dates][concept-exercise-dates] or [floating-point numbers][concept-exercise-floating-point-numbers] exercises. You can also check the exercise's [general concepts documents][reference] to see if other languages that have already an exercise for that concept.

## Help

If you have any questions regarding implementing this exercise, please post them as comments in the exercise's GitHub issue.

[docs-analyzer]: ./analyzer.md
[docs-representer]: ./representer.md
[docs-reference]: ./reference.md
[docs-exercises-concept]: ../exercises/concept/README.md
[docs-general-concept-exercises]: ../../../docs/concept-exercises.md
[docs-general-how-to-implement-a-concept-exercise]: ../../../docs/maintainers/generic-how-to-implement-a-concept-exercise.md
[concept-exercise-strings]: ../exercises/concept/strings
[concept-exercise-dates]: ../exercises/concept/dates
[concept-exercise-floating-point-numbers]: ../exercises/concept/numbers-floating-point
[reference]: ../../../reference
