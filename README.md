# STAT 155 Materials


## Topics

| Topic                      | Subtopic                                                                                                                           | In-Class Activities | Relevant Homework | Datasets Used in Activities                                                                                             |
|---------------|---------------|---------------|---------------|---------------|
| Foundations                | Cases/Variables, Univariate data visualization, Intro to R                                                                         | 01 - 02             | pp1               | jhu_evals                                                                                                               |
| Simple Linear Regression   | Bivariate relationships, Correlation, Least Squares, Coefficient Interpretation, Model Evaluation, Transformations, Residual Plots | 03 - 07             | pp1, pp2          | powerlifting, anscombe (in R), bikeshare, bechdel (in fivethirtyeight package), homes, bigmac, college, diamonds (in R) |
| Multiple Linear Regression | Visualization with \> 2 variables, Confounding, Interaction, Multicollinearity, Overfitting                                        | 08 - 14             | pp3, pp4          | palmerpenguins, cps_2018, bikeshare, high_peaks, diamonds, campaign_spending, used_cars                                 |
| Logistic Regression        | Probability, Odds, 2x2 tables, Coefficient interpretation, Model statements, Prediction, Model evaluation                          | 15 - 17             | pp5               | firststeps, titanic, resume                                                                                             |
| Sampling Variability       | Sampling distributions, variability, bootstrapping, normal distribution, confidence intervals                                      | 18 - 21             | pp6               | county_complete (in usdata package), Mercury                                                                            |
| Inference                  | Hypothesis testing, F-tests, hypothesis testing pitfalls (multiple testing, practical vs. statistical significance), p-values      | 22 - 26             | pp7, pp8          | MacGrades        



## File organization

- `core`    
    The `activities > core` files include the in-class exercises. These `core` files are where edits to the material should be made.

- `activities`    
    An online course website / manual can be built from the files in the `activities` folder (eg: `L02-activity.qmd`).
    Each file in this folder...
    - can include instructor-specific material (eg: announcements, warm-up examples)
    - automatically calls up the corresponding `core` file, which populates the in-class exercises
    - includes a solutions section at the bottom
    - generates a student note template (see `template_qmd`)

- `template_qmds`   
    The `template_qmds` folder includes files with the in-class exercises, in which students can take notes.
    These are generated from the corresponding `core` files using code in the corresponding `activities` file.
    To generate these files, Render the corresponding file in the `activities` folder.
    

- The `activities > _create_student_notes.qmd` file includes code that turns the core files into templates in which students will take in-class notes.    
    **IMPORTANT:** This file specifies instructor-specific file / image paths, so be sure to update that!


## Creating a Quarto book (online manual)

The below files will help you pull the activities together into a Quarto book.

- _quarto-book.yml: Where you'll control the structure of the book, including which "chapters" / activities to pull into the book. You'll need to edit this to update the semester, your name, your github repo url, etc.
- _quarto.yml: Big picture structural stuff. You shouldn't need to edit this.

You can compile the Quarto book and host it on GitHub as follows (this is just 1 approach!):

- Start a new PRIVATE Quarto repo. Why private? This will include things like solutions and, in general, we do not want to share files broadly.
- Create a new R project with version control, and link it to your GitHub repo.
- In GitHub repo:
    - create a folder named "docs"
    - Settings > Pages > Deploy from a Branch. Select main > docs. This means that the online manual will be built from html files in the "docs" folder.
- In RStudio:
    - Render the book. This will create a "docs" folder with htmls. These are the files that will comprise the online manual.
    - Commit-push-pull the raw files and docs folder to GitHub, directly from RStudio.
      

