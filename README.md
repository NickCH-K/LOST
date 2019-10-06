# LOST: THE LIBRARY OF STATISTICAL TECHNIQUES

Welcome to the LOST wiki!

The **Library of Statistical Techniques** (LOST) is a publicly-editable Wiki with a goal of making it easy to execute statistical techniques in statistical software. You can go to the wiki itself [here](https://github.com/NickCH-K/LOST/wiki).

Each page of the wiki contains a statistical technique - which may be an estimation method, a data manipulation or cleaning method, a method for presenting or visualizing results, or any of the other kinds of things that statistical software typically does.

For each of those techniques, the LOST page will contain code for performing that method in a variety of packages and languages. It may also contain information (or links) with thorough descriptions of the method, but the focus here is on implementation. How can you do it in your language of choice? If there are multiple ways, how are those ways different? Is the way you used to do it outdated, or does it do something unexpected? What's the `R` equivalent of that command you know about in `Stata` or `SAS`, or vice versa?

**This README file is a set of instructions for contributing to LOST**

# HOW TO CONTRIBUTE

1. [Get a GitHub account](https://github.com/join). You do not need to know Git to contribute to LOST, but you do need a GitHub account.
2. Read the [Guide to Editing Wiki Content](https://help.github.com/en/articles/editing-wiki-content) which will show the syntax that is used on GitHub Wiki pages.
3. Read the below LOST Writing Guide, which shows what a good LOST page looks like from top to bottom. Even if you are just adding another language to an existing page, be sure to read the Implementations section at the bottom.
4. Go to the [LOST Wiki](https://github.com/NickCH-K/LOST/wiki), find a page that needs to be expanded, and add more content. Or find one that doesn't exist but should, and write it yourself!

# LOST WRITING GUIDE

A LOST page is intended to be a *set of instructions for performing a statistical technique*, where "statistical technique" is broadly defined as "the things you do in statistical software", which includes everything from loading data to estimating models to cleaning data to visualization to reproducible notebooks.

After someone reads a LOST page, they should have a decent idea of:

- How to implement at least a basic version of what they want to do in the language/software they're using
- What common pitfalls there might be in what they're doing
- What are the pros and cons of meaningfully-different ways of doing the same thing, if relevant
- Given what they're doing, what else should they consider doing (for example, if they're running a regression discontinuity design, you might suggest they also run a test for bunching on either side of the cutoff)

Things to remember while writing:

- Be as clear as possible. You're writing a set of instructions, in effect. People should be able to follow them.
- The technical ability of the reader may vary by page. People reading a LOST page about how to calculate a mean probably have little experience with their software and will need a lot of hand-holding. You can assume that people reading a LOST page about Markov-Chain Monte Carlo methods probably already have a fairly solid background.

# CREATING A LOST PAGE

When starting a LOST page, you may want to copy the [New Page Template](https://github.com/NickCH-K/LOST/blob/master/NewPageTemplate). There are four main sections of a LOST page:

## Introduction

This is a *very brief* introduction to the technique. Just a few sentences about what it is and does, and perhaps why it is used. LOST is not the place for an in-depth explanation of the statistical details behind a method. Instead, for more detailed explanations link to an outside trusted source like Wikipedia or a (non-paywalled) academic paper.

Math is not supported. Generally, you can refer to terms by simply putting them in bold. If an equation is necessary, create the equation as an image on [this page](https://www.codecogs.com/latex/eqneditor.php) and include the equation as an image.

## Keep in Mind

This is a list of details and reminders for people using the method, especially if they are not yet an expert at it or if the detail is not well-known. This may include:

- Important assumptions that an estimation method makes.
- Notes about interpreting the results.
- Settings where the technique *seems* like it might be a good idea, but actually isn't.
- Features of the technique that might surprise users or be unexpected.

## Also Consider

This is a list of *other* techniques that are commonly used *in addition to* this page's technique, or *as an alternative to* this page's technique. If not obvious, include a very brief explanation of why you might want to use that other technique in addition to/instead of the current one. Note that you can link to another LOST page even if that page doesn't exist yet. Maybe it will inspite someone to write it!

For example, pages about estimation techniques might list standard robustness tests to be used in addition to the technique, or adjustments to standard errors they might want to use. A page about a data visualization technique might include a link to a page about setting color palettes to be used in addition.

Or, they might list an alternative technique that might be used if a certain assumption fails ("This estimation/data visualization technique requires continuous variables. So if your data is discrete, use this other method.").

## Implementations

Implementations contains multiple subsections, one for each piece of statistical software/programming langauge that the technique can be implemented in. 

- Any language is valid as long as it's something people actually do statistical analysis in. Don't include something just because you *can*, but because you think someone will find it useful.
- For each language, include well-commented and **brief** example code that provides an example of performing the technique. Readers should be able to copy the code and have it run the technique from beginning to end, including steps like loading in data if necessary. See existing pages for examples.
- Avoid creating a long list of examples showing every variant or optional setting of the technique. Instead, focus on one main example, with variants included only if they are especially important.
- If the technique requires that a package or library be installed, include the code for installing the package in a comment (or if you are using a language where libraries cannot be installed inside the code, include a comment directing the user to install the library).
- If a given language has *multiple ways* of performing the same technique, ideally report only one "best" method, whatever that might be. If other methods are only different in trivial ways, then you can list them as alternatives, but avoid providing their own examples. If other methods are different in important ways, then include an example for each, with text explanations of what is different about them. 
- It is fine to add implementations for software that only has a graphical interface rather than code (such as Excel). Be sure to keep images small so they don't crowd the page. If your graphical instructions are necessarily very long, consider posting them as a blog post somewhere and just put a link to that post in Implementations. How can you add these images? You can upload the images somewhere on the internet that allows image linking, and include the image in your instructions. Or, ideally, if you know how to use GitHub, you can issue a Pull Request to upload the images to the LOST/Pictures/NameofPage folder, and link to the images there. 
