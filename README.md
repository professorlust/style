# Coding project style guide
Guidelines on code and coding projects for the NY Daily News newsroom.

## Religious battles

### Spaces vs. tabs

Spaces, four of them.

### CamelCase vs. underscore_each_word

Underscores, please. The one exception: When naming classes, use camelCase.

## Other naming conventions

### File and directory names
Naming files and directories consistently will make certain things in your world a little bit easier.

Some basics:
* All names should be lower-case, always. Keeping file and directory names lower-case makes one less thing you have to think about when typing in URLs and when creating file / directory names.
* Use hyphens in directories, use underscores in file names. Never use spaces.
* Keep directory names for directories that store assets as short as can be while still being clear.
* Image file names should be as clear as possible. If the image is a photo, make sure you can tell what the photo is of from the file name.

### Variable names

See camelCase vs. underscores.

#### Constant names

Constants act like a variable but once a constant is set it doesn't change. Often these are used as environment vars used to configure a particular app on a particular server / computer. Constants have an explicit place in PHP and environment vars have a defined place in the shell, and this ALLCAPS style can be used in Python and Javascript with no side effects.

Constant names should be UPPERCASE_WITH_UNDERSCORES.

### What about when I'm importing code that uses its own style?

Let it be.

## HTML style

Markup should be readable when viewed. Also, when stylesheets are disabled, the markup of the document should still make sense.

### When to add classes, when to add id's, and when to use markup

## Javascript style

Writing a bunch of functions with loose javascript in between is the enemy. Organizing your javascript into discrete objects is a solid first step toward code maintainability and test-ability. I would write more but [Clean Code: Javascript](https://github.com/ryanmcdermott/clean-code-javascript) has already written it. Read that.

## CSS style

Four-space tabs, if it's a one-line declaration keep it on one line, ala
```css
ul.emphasis li { font-size: 4em; }
```
Otherside declare styles like
```css
article > p {
    line-height: 1em;
    color: #333;
}
```

## Python style

[PEP8 is the Python style guide and is worth reading](https://www.python.org/dev/peps/pep-0008/).

## PHP style

### Braces and if / foreach / loop syntax

PHP lends itself to piles of hard-to-decipher close-braces. Here are some preferred techniques to avoid tag soup:

#### if / endif

Instead of `if ( clause ) { some_code(); }`, do `if ( clause ): some_code(); endif;`. Same for `foreach`'s.

## Project management

### Committing to repo

#### When to commit

Commit early and often. You don't need to push with every commit, but incremental commits will allow you to retrace the decisions you made should you need to do that.

#### How to write an adequate commit message

Start your commit message with a verb. Describe what changed. If you made a decision you'd like to remember later, mention that and explain it.

Bad commit message:
```
It's fixed.
```

Better commit message:
```
Fixed the inaccurate markup in index.html.
```

Best commit message:
```
Fixed the inaccurate markup in index.html. Using <p>'s instead of <br>'s improves the document's accessibility.
```

### Creating repositories vs. creating snippets vs. actually making something


### When to use a database vs. when to not use a database

Most of the time you don't need a database for your project. Even many of the times you think you need a database, you don't. Places you might need a database include interactives that record user data (though you don't always need a db for that), gigantic multi-join table situtations, you have a data dump in sql format, you want to try sqlite out for something and you promise it won't become a deal.
