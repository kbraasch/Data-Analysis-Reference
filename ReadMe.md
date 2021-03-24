# Setup a Project

Start a project by selecting a methodology and setting up the structure, documentation, workflow.

## Methodology

It is important to follow one of these organizational methods to improve workflow effeciency, project success, team interactions, and more.  
[Here is a towards article introducing data science methodology](https://towardsdatascience.com/data-science-methodology-101-ce9f0d660336)  
[IBM offers a Data Science Methodology course on Coursera](https://www.coursera.org/learn/data-science-methodology)

Insert Image of methodology with reference

Methodologies for consideration:

- [IBM's Methodology in PDF](https://tdwi.org/~/media/64511A895D86457E964174EDC5C4C7B1.PDF)
- [DataScience foundation's Methodology](https://datascience.foundation/methodology)
- [CRISP-DM Data Mining Process in PDF](https://the-modeling-agency.com/crisp-dm.pdf)
- [Microsoft Team Data Science Process (TDSP)](https://docs.microsoft.com/en-us/azure/machine-learning/team-data-science-process/) (Worth a read. Very detailed, focused on teams, examples available)

I like Microsoft TDSP, so my approaches below will be based on that methodology.

## Project structure

The simplest way to setup a project structure is to clone a template repo. If you are using the Microsoft TDSP methodology, there is an archived [GitHub repo](https://github.com/Azure/Azure-TDSP-ProjectTemplate) available. [Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/) is a popular option, you can fork it and modify as needed to suit your workflow. Good software development process is also important. PilippoBovo offers a [Production Data Science Tutorial](https://github.com/FilippoBovo/production-data-science) to teach good practices and uses the Cookiecutter project template.

[My_DSP_ProjectTemplate](#) is a folder structure with report templates I generated based on the [Microsoft TDSP Template](https://github.com/Azure/Azure-TDSP-ProjectTemplate)

# Execute a Project

## Project Understanding

[Business Understanding Microsoft docs](https://docs.microsoft.com/en-us/azure/machine-learning/team-data-science-process/lifecycle-business-understanding), they have some concise but effective considerations here.

You have a project structure in place, now its time to get started! There is a question, problem or an idea you would like to explore. A project outline needs to be completed. Explore and explain the basis for the project. Specify the desired or expected outcome. Specify the scope, phases and deliverables. Identify a way to measure that outcome, and specify what type of improvements and results would be considered a success for the project and apply those to the current situation to get a baseline. Anticipate the cost and what is going to be used, consumed, or required to complete of this project. Convert the project success metrics into technical metrics. Identify the data you would need, what's available, and if there is any that needs to be collected (Is there a breakout data collection project required here?). Identify methods of analysis and/or modeling that are useful for the project. Then work out deliverables, roles, and responsibilities.

[My_DSP Project Outline Report](#)

## Data Acquisition & Understanding

- [Databases.md]() highlights database types, tools and services.
- [Data.md]() outlines different data classification, types, and storage mediums.
- [Python.md]() gives an overview of python data types and structures and libraries available for working with data.
<!-- - [StatisticalAnalysis.md]() can be used to find a starting point for the data analysis. -->
- Document each data source with a Dataset Summary Report
- Document data transformation with a Data Definition Report
- Complete an Analysis Findings Report

## Modeling

<!-- - [MachineLearning.md]() can help identify the appropriate training tool to generate a model from the data. -->

- Fill out a Model Report
- Text project metrics and model results
- Iterate if requirements not met

## Wrap-up

- Complete all deliverables
- Fill out the Deliverable Model Report
- Fill out the Project Results Report
