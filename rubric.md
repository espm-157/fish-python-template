# Climate Module: Detailed Rubric

Total: 20 points (of 24 available -- this allows multiple paths through the module)

## 1. Data Reading and Preprocessing (**5 points**)

**5 points**: The notebook correctly reads in the data, handles missing or incorrect data appropriately, and clearly documents these steps.
 
## 2. Data Visualization (**5 points**)

**5 points**: The data analysis is thorough, appropriate for the data, and well-executed. Plots are clear, well-labeled, and enhance understanding of the data. Figures are clearly labeled with legends, titles and axes labels.

## 3. Code Quality and Documentation (**5 points**)

**5 points**: The code should be concise, semantically meaningful. The code does not introduce additional libraries or methods not necessary for the task or beyond the scope of basic data analysis methods covered in the course so far.   

Avoid common LLM-based code-junk that does not follow best practices in data science notebooks:
  - Do not use `print` statements in code cells.  Cells should do one clear isolated task.  The final value on a cell is auto-printed by Jupyter without needing a `print` statement -- this should be used appropriately (e.g. to display small tables or plots).  
  - Code should not include unnecessary error handling, such as `try` statements.  Use concise, working code for the data.  
  - Code should not create function definitions unless they serve a clear use in making the code more concise and readable. 
  - Do not include code comments in most cases.  Codes should be *self-documenting*, with clear variable names and structure.  Comments should be brief and only to clarify technical details.  Use markdown cells to explain the overall logic and flow of the notebook.
  - avoid long chunks of code that are not broken up into smaller, logical steps.  Each code cell should do one thing, and be clearly labeled with a markdown cell above it to explain what it does.

AVOID the failure condition of fabricated data. LLMs will sometimes fail to read data in from authorative sources becuase as we see in this assignment, 'parsing' data is hard!  LLMs can get desperate and will then make up data that roughly matches the pattern the expect.  Sometimes they are transparent about this ("I cannot read the file, but if you imagine the file gave you these numbers than this is what you would do...") and sometimes less so.  Regardless, plotting made up or fictious generated data instead of numbers from authorative data sources could be considered fraud and get you fired in real-world employment.  For us, it is a "failure condition", **-10 points**. 

## 5. Narrative (**5 points**)

**5 points**: The notebook makes good use of markdown chunks to tell a clear story.  Instructor-provided headings like "exercise II" are replaced by topical headings like "Global Temperature".  Data used and plots generated are clearly described ("the plot shows...") to help a reader understand what they are seeing, where the data comes from, key take-aways.  <https://climate.nasa.gov/vital-signs> is a great example of supporting narrative describing the data and results, but tell the story in your own words.  


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

The notebook fabricates data, or presents fictious, made-up, or "example" numbers in tables or charts as if they are real instead of reading data from the canonical data sources indicated. (Automatic fail)


