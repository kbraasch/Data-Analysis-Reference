# Python Data Fundamentals

## Data Types

<!-- prettier-ignore -->
| Category | Name | Data Type | Description |
| --- | --- | --- | --- |
| Text | String | str | Immutable sequences of Unicode code points |
| Numeric | Integer <br> Floating Point <br> Complex | int <br> float <br> complex | Whole number, positive or negative, without decimals, of unlimited length <br> A number, positive or negative, containing one or more decimals <br> Complex number written with a "j" as the imaginary part |
| Logical | Boolean | bool | A 'True' or 'False' value |

<br>

## Data Structures

<!-- prettier-ignore -->
| Category | Data Type | Syntax | Description |
| --- | --- | --- | --- |
| Sequence | list <br> tuple <br> range | \[ , \] <br> ( , ) <br> range(s,e,i) | Mutable sequence to store collection of homogeneous data <br> Immutable sequence to store collection of heterogeneous data <br> Immutable sequence of numbers |
| Mapping | dict | { key: val , } | Stores values in a key : value pair dictionary | 
| Set | set <br> frozenset | \{ , \} <br> frozenset( , ) | Stores multiple items in a single variable (unordered and no duplicates) <br> Immutable set |

[NumPy](https://numpy.org/) adds support for large, multi-dimensional arrays and matrices as well as mathematical functions for array operations. It also extends the available (data types)[https://numpy.org/doc/stable/user/basics.types.html].  
[Pandas](https://pandas.pydata.org/) expands the available [data structures](https://pandas.pydata.org/docs/getting_started/overview.html) and improve processing those structures.

<br>

# Libraries

## Data Extraction

### Excel

[pyton-excel.org](http://www.python-excel.org/) offers library references (summarized below)

<!-- prettier-ignore-->
| File Type | Libraries |
| --- | --- |
| .xlsx | [openpyxl](https://openpyxl.readthedocs.io/en/stable/) for read/write <br> [xlsxwriter](https://xlsxwriter.readthedocs.io/)  for writing & charts <br> [Pandas](https://pandas.pydata.org/docs/reference/api/pandas.read_excel.html) for simple read/write|
| .xlsb | [pyxlsb](https://pylightxl.readthedocs.io/en/latest/) to read |
| .xlsm | [pylightxl](https://pylightxl.readthedocs.io/en/latest/) to read |
| .xls | [xlrd](http://xlrd.readthedocs.io/en/latest/) to read <br> [xlwt](http://xlwt.readthedocs.io/en/latest/) to write |

### CSV

- [Python standard library](https://docs.python.org/3/library/csv.html) csv module implements classes to read and write tabular data in CSV format.
- [Pandas](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html) allows you to read a csv into a DataFrame, and output a DataFrame to csv format.

### Text

- Python offers [file reading and writing](https://docs.python.org/3/tutorial/inputoutput.html) with a specified encoding format. Opens in text mode by default. Lines of the file can be read and written to.

Parsing

- Standard format - Manageable with [pandas](https://pandas.pydata.org/docs/reference/api/pandas.read_table.html) or [python io](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html)
- String methods (simple custom formats) - Customize your parsing with [Python String methods](https://docs.python.org/3.4/library/string.html)
- Regular expressions (complex custom formats) - Python's [regular expression module](https://docs.python.org/3/howto/regex.html) is available for identifying complex forms

Gabriele Tomassetti offers a very detailed article on [Parsing in Python](https://tomassetti.me/parsing-in-python/)

### Images

- [Pillow](https://pillow.readthedocs.io/en/stable/) offers a general image processing tool.
- [scikit-image](https://scikit-image.org/) offers algorithms for image processing.
- [OpenCV](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_setup/py_intro/py_intro.html) offers computer vision tools.

### Databases

- [Pandas](https://pandas.pydata.org/docs/reference/api/pandas.read_sql.html) is able to read a SQL query or database table into a DataFrame.
- [SQLite](https://docs.python.org/3/library/sqlite3.html) provides a lightweight disk-based database that doesn’t require a separate server process and allows accessing the database using a nonstandard variant of the SQL query language.
- [turbodbc](https://turbodbc.readthedocs.io/) offers access to relational databases via the [Open Database Connectivity (ODBC)](https://en.wikipedia.org/wiki/Open_Database_Connectivity) interface. Compliant with the [Python Database API Specification 2.0](https://www.python.org/dev/peps/pep-0249/)
- [Firebase Cloud Firestore](https://firebase.google.com/docs/firestore/quickstart#python_1) is accessible with python.
- [MongoDB has a getting-started article](https://www.mongodb.com/blog/post/getting-started-with-python-and-mongodb) on using their python driver.

### Web Scraping

- [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/) library is great for pulling data out of HTML and XML files.
  - The documentation highlights some [parser options](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#installing-a-parser)
- [Scrapy](https://scrapy.org/) framework for crawling and extracting structured data from web sites, and APIs.

### [Intake](https://github.com/intake/intake): A general interface for loading data

Uses:

- Load data from a variety of formats into Pandas dataframes, Python lists, NumPy arrays, and more.
- Convert boilerplate data loading code into reusable Intake plugins.
- Describe data sets in catalog files for easy reuse and sharing between projects and with others.
- Share catalog information (and data sets) over the network with the Intake server.

<br>

## Data Exploration

### [statsmodels](https://www.statsmodels.org/)

Provides classes and functions for the estimation of many different statistical models, as well as for conducting statistical tests, and statistical data exploration.

Offers:

- Regression and Linear Models
- Time Series Analysis
- Single and multivariate statistics
- Contingency tables
- Distributions
- Graphics
- And much more...

### [Sweetviz](https://github.com/fbdesignpro/sweetviz)

An open-source Python library that generates beautiful, high-density visualizations to kickstart EDA (Exploratory Data Analysis) with just two lines of code. Output is a fully self-contained HTML application.

Offers:

- Dataset summary display
- Categorical associations
- Target variable summary
- Numerical analysis statistics
- Textual analysis statistics
- Population comparison

### [Dora](https://github.com/NathanEpstein/Dora)

Brings automation to the painful parts of EDA. Contains convenience functions for data cleaning, feature selection & extraction, visualization, partitioning data for model validation, and versioning transformations of data.

<br>

## Cleaning Data

### [ftfy](https://github.com/LuminosoInsight/python-ftfy)

Fixes Unicode that's broken in various ways.

### [Beautifier](https://github.com/labtocat/beautifier)

Cleans url patterns, domains, unicodes, special charecters and unnecessary redirection patterns from the urls and gives you clean data.

### [scrubadub](https://scrubadub.readthedocs.io/)

Removes personally identifiable information from free text.

### [Arrow](https://arrow.readthedocs.io/)

Handles creating, manipulating, formatting and converting dates, times and timestamps.

<br>

## Data Processing and Analysis

### [Pandas](https://pandas.pydata.org/)

Provides fast, flexible, and expressive data structures designed for working with “relational” or “labeled” data. A fundamental high-level building block for doing practical, real-world data analysis in Python.

[This towards article](https://towardsdatascience.com/all-the-core-functions-of-python-pandas-you-need-to-know-d219cbd87636) about Pandas core functions gives a good overview of how to get started processing and cleaning data.

### [NumPy](https://numpy.org/)

Provides a multidimensional array object, various derived objects (such as masked arrays and matrices), and an assortment of routines for fast operations on arrays, including mathematical, logical, shape manipulation, sorting, selecting, I/O, discrete Fourier transforms, basic linear algebra, basic statistical operations, random simulation and much more.

### [SciPy library](https://www.scipy.org/)

A collection of mathematical algorithms and convenience functions built on the NumPy extension of Python. It adds significant power to the interactive Python session by providing the user with high-level commands and classes for manipulating and visualizing data.

<br>

## Data Visualization

### [Matplotlib](https://matplotlib.org/)

Create static, animated, and interactive visualizations in Python. The website [provides demonstrations](https://matplotlib.org/stable/gallery/index.html) of the available plotting functionality.

### [Seaborn](https://seaborn.pydata.org/)

Built on matplotlib, it provides a high-level interface for drawing statistical graphics. They provide an [example gallery](https://seaborn.pydata.org/examples/index.html).

### [Plotly](https://plotly.com/python/)

Makes interactive, publication-quality graphs. Plotly is partnered with [Dash](https://dash.plotly.com/) for interactive dashboarding. Offers a wide array of [professional graphics](https://plotly.com/python/plotly-fundamentals/).

### [Bokeh](https://docs.bokeh.org/)

Creates interactive visualizations for modern web browsers with JavaScript. See their [Examples](https://docs.bokeh.org/en/latest/docs/gallery.html).

<br>

## Machine Learning

### [TensorFlow](https://www.tensorflow.org/)

An end-to-end open source platform that makes it easy to build and deploy ML models.

### [Scikit-Learn](https://scikit-learn.org/)

Open source, simple, and efficient tool for predictive data analysis.

### [PyTorch](https://pytorch.org/)

Optimized tensor library for deep learning using GPUs and CPUs.

<br>

## Dashboarding

### [Panel](https://panel.holoviz.org/)

Create custom interactive web apps and dashboards by connecting user-defined widgets to plots, images, tables, or text.

### [Dash](https://dash.plotly.com/)

A productive Python framework for building web analytic applications, ideal for building data visualization apps with highly custom user interfaces in pure Python. Dash is partnered with [Plotly](https://plotly.com/python/) for visualizations. Also has an enterprise version available.

### [Viola](https://github.com/voila-dashboards/voila)

Voilà turns Jupyter notebooks into standalone web applications.

### [Streamlit](https://streamlit.io/)

Create and share beautiful, custom web apps for machine learning and data science.

<br>

# Workspace

## [Anaconda](https://www.anaconda.com/)

Python distribution platform packed with software and libraries for data science.

Comes with:

- Anaconda Navigator GUI
- Conda package manager
- JupyterLab (browser UI including notebook environment)
- Jupyter Notebook (browser notebook environment)
- Spyder (environment)

## Version Control

Backup and protect your project files.

### [Git](https://git-scm.com/)

A software for tracking changes in any set of files, useful for coordinating work among a team. Local storage, so consider making regular backups on the network.

### [GitHub](https://github.com/)

Online code hosting platform for version control and collaboration. Offers GitHub Pages, where you can generate a webpage for your organization or project from a repository.
