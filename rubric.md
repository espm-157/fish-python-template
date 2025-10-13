# Fish Module: Detailed Rubric

Total: 20 points (of 24 available -- this allows multiple paths through the module)

## 1. Data manipulation tasks (**5 points**)

**5 points**: The notebook demonstrates clear understanding of core ibis data manipulation tasks: `select`, `filter`, `join`, `distinct`, and `group_by`+`agg` patterns.  
 
## 2. Data Visualization (**5 points**)

**5 points**: The data analysis is thorough, appropriate for the data, and well-executed. Plots are clear, well-labeled, and enhance understanding of the data. Figures are clearly labeled with legends, titles and axes labels.

## 3. Code Quality and Documentation (**5 points**)

**5 points**: The code should be concise, semantically meaningful. The code does not introduce additional libraries or methods not necessary for the task or beyond the scope of basic data analysis methods covered in the course so far.   Pay attention to clean formatting of ibis pipe commands. Do not include any unnecessary exploratory code in the main notebook -- consider using an appendix.ipynb or explaining reasoning using markdown cells instead.  

_Avoid "magic values" in code_ without any other documentation.  For example, if your markdown cells describe the task as being about selecting the Atlantic Cod from other species, it is reasonable to have code like `filter(_.commonname == "Atlantic cod")` but not acceptable to have code like `filter(_.stockid == "COD2J3KL")`.  The latter is a 'magic value' -- how do we know that stock is an Atlantic cod stock? Why select that one stock of cod while ignoring other stocks that are also Atlantic cod?  

Avoid common LLM-based code-junk that does not follow best practices in data science notebooks:
  - Do not use `print` statements in code cells.  Cells should do one clear isolated task.  The final value on a cell is auto-printed by Jupyter without needing a `print` statement -- this should be used appropriately (e.g. to display small tables or plots).  
  - Code should not include unnecessary error handling, such as `try` statements.  Use concise, working code for the data.  
  - Code should not create function definitions unless they serve a clear use in making the code more concise and readable. 
  - Do not include code comments in most cases.  Codes should be *self-documenting*, with clear variable names and structure.  Comments should be brief and only to clarify technical details.  Use markdown cells to explain the overall logic and flow of the notebook.
  - avoid long chunks of code that are not broken up into smaller, logical steps.  Each code cell should do one thing, and be clearly labeled with a markdown cell above it to explain what it does.

AVOID the failure condition of fabricated data. **-10 points**. 

## 5. Narrative (**5 points**)

**5 points**: The notebook makes good use of markdown chunks to tell a clear story. All code chunks should be supported by markdown text explaining the reasoning and process expressed in the code.   

_Compare results to published literature_ in your closing discussions!  Do you find the same overall conclusion? How is it similar, how is it different?  What are the likely explanation(s) for any differences? 


## 5. Use of GitHub (**4 points**)

**4 points**: 

README file is updated with:
  - Authorship information
  - GitHub Actions badge, with correct link to repository
  - Updated description of repository overview.

Repository passes the auto-check on GitHub Actions.

Repository is clearly organized with logical filenames.

Clear, clean record of GitHub commits, appropriate git log messages. 
Appropriate use of branches and pull requests if indicated by the instructor.


## Failure conditions

The notebook fabricates data, or presents fictious, made-up, or "example" numbers in tables or charts as if they are real instead of reading data from the canonical data sources indicated. **-10 points**

