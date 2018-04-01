# jakedvpTutorial
[Jake Vanderplas Data Analysis Tutorial](https://www.youtube.com/watch?v=_ZEWDGpM-vM)

The link above is an excellent tutorial by Jake Vanderplas to create a Notebook for Data Analysis. It captures the entire flow from a concept to coding, testing, and code refactoring. Along the way pytest framework and working with github is introduced. I have followed through the entire tutorial. And I have retained the scratch areas to make sure that the read understands the process and followed through the entire series. They scratch notebooks are names as scratch and some of them will have versions (example: Jvander-1.ipynb, Jvander-2.ipynb, etc)

I will try and writeup as much as possible to make the **self-explanatory tutorial** by Jake easier. That said, it is ideal that everyone follow through the entire process and create the notebooks and the process from scratch.

This is intended for someone who is an expert on Notebook based Data Analysis and want to quickly reference Jakes' tutorial without creating the Notebooks.

### Organization of folders

Jvander-1.ipynb: Introduction to data analysis with an example. It shows the basic principle of extracting data from internet and displaying data using urllib, Pandas and Matplotlib. The file uploaded from the internet is saved locally (fremont.csv) to prevent the costly roundtrip.  
  
Jvander-2.ipynb: In this notebook the disparate data methods are captures as a single function title get_fremont_data. This shows how to abstract a read function. The read function is called by the display functions including pivoted plot.  

Jvander-3.ipynb: Now the function is copied into a file called data.py under the directory jupyterworkflow. And will use the standard import function to import our refactored coded in data.py (get_fremont_data function). 


scratch.ipynb: In this module we create a test framework to test get_fremont_data function. And a function called test_fremont_data is created. It is testing with a few assert statements to check the correctness of our function. A folder called tests is created under jupyterworkflow. The code from notebook (test_fremont_data) is copied to a file tests/test_data.py. 

To test the data function: python -m pytest jupyterworkflow

pytest will gather all the tests and run the test. If the test is succesfull the output shoudl be:

```python -m pytest jupyterworkflow
============================= test session starts =============================
platform win32 -- Python 3.6.4, pytest-3.5.0, py-1.5.3, pluggy-0.6.0
rootdir: C:\cygwin64\home\cjaga\Development\DataAnalysis\jakedvpTutorial, inifile:
collected 1 item
```
A Make file is created to call the above command.

At every step with commit the code to local git repository and also to github so that the work is backed up
