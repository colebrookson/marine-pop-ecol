---
permalink: /repo-guidelines/
layout: single
title: Repository and Code Style Guidelines
author_profile: false
excerpt: "Consistent practice of how you write code and structre repositories is essential for creating easily reproducible analyses."
header:
    overlay_image: /assets/images/bamfield-3.jpg
    overlay_filter: 0.5
    author_profile: false
    caption: ""
    actions:
      - label: "Download"
        url: "https://colebrookson.github.io/marine-pop-ecol/_pages/guest-speakers.pdf"
classes: wide
sidebar:
  nav: "Course Materials"
---
# Repository Structure

In every repository, keeping things consistent will be essential. 

# Style Guide

When writing code and managing files, it's always best to use consistent style. The best way to do so is to follow a style guide as closely as possible. 

This style guide is based largely off the [Tidyverse Style Guide](https://style.tidyverse.org/), and much of the style guidelines here are copied and pasted directly. This assumes you are using the [R](https://www.r-project.org/) language and likely the [RStudio](https://www.rstudio.com/) IDE. It is recommended that you read through and follow the [Tidyverse Style Guide](https://style.tidyverse.org/) but **there are five key components of the style guide, *Files, Syntax, Functions, Pipes, `ggplot2`***, and key components of each are highlighted here: 

### **Files**
  * Organization
    * File names should be meaningful and end in .R or .RMD. Avoid using special characters in file names - stick with numbers, letters, -, and _.
    * If files should be run in a particular order, prefix them with numbers. If it seems likely you’ll have more than 10 files, left pad with zero:
    ```
    00_download.R
    01_explore.R
    ...
    09_model.R
    10_visualize.R
    ```
    * Pay attention to capitalization, since you, or some of your collaborators, might be using an operating system with a case-insensitive file system (e.g., Microsoft Windows or OS X) which can lead to problems with (case-sensitive) revision control systems. Prefer file names that are all lower case, and never have names that differ only in their capitalization.
  * Internal Structure
   * Use commented lines of - and = to break up your file into easily readable chunks.
   ```
   # Load data ===========================

   # Plot data ===========================
   ```
   * If your script uses add-on packages, load them all at once at the very beginning of the file. This is more transparent than sprinkling `library()` calls throughout your code or having hidden dependencies that are loaded in a startup file, such as .Rprofile.

### **Syntax**
  * Object Names
    * Variable and function names should use only lowercase letters, numbers, and _. Use underscores (_) (so called snake case) to separate words within a name.
    * Base R uses dots in function names (`contrib.url()`) and class names (`data.frame`), but it’s better to reserve dots exclusively for the S3 object system. In S3, methods are given the name `function.class`; if you also use . in function and class names, you end up with confusing methods like `as.data.frame.data.frame()`
    * Where possible, avoid re-using names of common functions and variables. This will cause confusion for the readers of your code.
  * Long Lines
    * Strive to limit your code to 80 characters per line. This fits comfortably on a printed page with a reasonably sized font. If you find yourself running out of room, this is a good indication that you should encapsulate some of the work in a separate function.
    * If a function call is too long to fit on a single line, use one line each for the function name, each argument, and the closing ). This makes the code easier to read and to change later.
   ```
   # Good
   do_something_very_complicated(
    something = "that",
    requires = many,
    arguments = "some of which may be long"
   )
  
   # Bad
   do_something_very_complicated("that", requires, many, arguments,
                                "some of which may be long"
                                )
  ```
  * Comments
    * Each line of a comment should begin with the comment symbol and a single space: #
    * In data analysis code, use comments to record important findings and analysis decisions. If you need comments to explain what your code is doing, consider rewriting your code to be clearer. 

### **Functions**
  * Naming
    * As well as following the general advice for object names, strive to use verbs for function names:
    ```
    # Good
    add_row()
    permute()
    
    # Bad
    row_adder()
    permutation()
    ```
  * Long lines
    * If a function definition runs over multiple lines, indent the second line to where the definition starts.
    ```
    # Good
    long_function_name <- function(a = "a long argument",
                                   b = "another argument",
                                   c = "another long argument") {
      # As usual code is indented by two spaces.
    }
  
    # Bad
    long_function_name <- function(a = "a long argument",
      b = "another argument",
      c = "another long argument") {
      # Here it's hard to spot where the definition ends and the
      # code begins
    }
    ```
  * Comments
    * In code, use comments to explain the “why” not the “what” or “how”. Each line of a comment should begin with the comment symbol and a single space: #.
    ```
    # Good

    # Objects like data frames are treated as leaves
    x <- map_if(x, is_bare_list, recurse)
    
    # Bad
    
    # Recurse only with bare lists
    x <- map_if(x, is_bare_list, recurse)
    ``` 
### **Pipes**
  * Long Lines 
    *  If the arguments to a function don’t all fit on one line, put each argument on its own line and indent:
    ```
    iris %>%
     group_by(Species) %>%
     summarise(
       Sepal.Length = mean(Sepal.Length),
       Sepal.Width = mean(Sepal.Width),
       Species = n_distinct(Species)
     )
    ```
### **`ggplot2`**
   * Whitespace
     * `+` should always have a space before it, and should be followed by a new line. This is true even if your plot has only two layers. After the first step, each line should be indented by two spaces
   * Long lines
     * If the arguments to a ggplot2 layer don’t all fit on one line, put each argument on its own line and indent:
     ```
     # Good
     ggplot(aes(x = Sepal.Width, y = Sepal.Length, color = Species)) +
       geom_point() +
       labs(
         x = "Sepal width, in cm",
         y = "Sepal length, in cm",
         title = "Sepal length vs. width of irises"
       ) 
     
     # Bad
     ggplot(aes(x = Sepal.Width, y = Sepal.Length, color = Species)) +
       geom_point() +
       labs(x = "Sepal width, in cm", y = "Sepal length, in cm", title = "Sepal length vs. width of irises") 
     ```
     * ggplot2 allows you to do data manipulation, such as filtering or slicing, within the data argument. Avoid this, and instead do the data manipulation in a pipeline before starting plotting.
     ```
     # Good
     iris %>%
       filter(Species == "setosa") %>%
       ggplot(aes(x = Sepal.Width, y = Sepal.Length)) +
       geom_point()
     
     # Bad
     ggplot(filter(iris, Species == "setosa"), aes(x = Sepal.Width, y = Sepal.Length)) +
       geom_point()
     ```
