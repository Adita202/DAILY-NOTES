# FEATURE ENGINEERING AND VISUALIZATION

### CONTINUOUS AND DISCRETE VARIABLES
- in tabular data, they ccan be divided into two
          - numeric and non numeric

Numeric data can be continuous or discrete where, discrete data are mostly whole numbers, not fractions or floats

- input columns are know as features while predicted columns(the column that we predict) are called as labels
- textual component - categorical 
- on the basis of how output/label is continuous or discrete it can be Regression and Classification respectively.
- We can convert a regression model into a classification model if needed.
  **There are two types of data**

      -  supervised data - with label
      - unsupervised - without label

 ### Exploratory data analysis (EDA)
 - investigating and summarizing a dataset to uncover patterns, detect anomalies, test hypotheses, and check assumptions. 
 - It provides insights that guide further analysis or model building.
   -mainly two libraries used matplotlib, seaborn
    - deal with many graphs
#### TYPE OF PLOTS
- 1) **Line plot** 
	  -  How x axis change with respect to y. Time series nature of variables considered.
	  - x and y values should be ploted
	  - x and y should be related in some way. Eg: No specific relation b/w mpg and weight
                
<p>
 <img src="https://github.com/user-attachments/assets/46ed9873-f899-464a-a421-28d3af127282" width=400>
</p>

              - x = [0,1,2,3,4,5]
              - y1 = [0,3,2,22,22,10]
              - y2 = [1,7,5,4,3,8]
              - plt.plot(x, y1, c="g", label="location1") #c for colour, look documentation for more colour codes, labe for giving names to legends
              - plt.plot(x,y2, c="r", label="location2")
              - plt.xlabel("days")
              - plt.ylabel("counts")
              - plt.legend(loc="upper left") #legends will only be shown if we pass this command. The location of legend is autolocated according to the graph.
                    #Can change it if we want.
              - plt.savefig("lineplot.png")
              - plt.show()

		
- 2) **Barchart**

<p>
   <img src="https://github.com/user-attachments/assets/f0146bf1-9c2f-467f-8226-a56925e1ad01" width=400>
</p>

            - x = ["mon", "tue", "wed", "thu", "fri", "sat", "sun"]
            - y1_sales = [10,20,30,40,50,60,70]
            - y2_sales = [70,60,50,40,30,20,10]
            - plt.bar(x,y1_sales, label="item1")
            - plt.bar(x,y2_sales,  alpha = 0.2,  label="item2") #alpha given to reduce the transparency of a colour to show the overlapping. alpha=1(bold)
            - plt.xlabel("Days") 
            -  plt.ylabel("counts")
            -  plt.legend()
            - plt.savefig("barchart.png", dpi=300) #dpi is a parameter to increase the resolution of a fig
            - plt.show()

- 3) **Piechart**

<p>
  <img src="https://github.com/user-attachments/assets/980ada86-f624-4477-8832-1175ba7a48d7" width=400>
</p>

          - countries = ["India", "USA", "Bahrain", "Dubai", "Africa"]
          - population = [120, 20, 30, 40, 50]
          - plt.pie(population, labels = countries, autopct="%1.2f%%") #to indicate decimal. If we dont eed decimal, just add %d%%
          - plt.savefig("piechart.png")
          - plt.show()


- 4) **Histogram**

<p>
  <img src ="https://github.com/user-attachments/assets/16a6144a-c676-4241-8bb6-d080d413d906" width = 400>
</p>

          - import pandas as pd
          - df = pd.read_csv("C:\\Users\\hp\\Downloads\\auto-mpg (1).csv")
             
         - plt.hist(df["mpg"], color ="green", rwidth=0.8, density=True, cumulative=True) #density gives the percentage count of variable. #cumulative shows the cumulative freq of the data
          - plt.title("Histogram of MPG")
          - plt.xlabel("MPG")
          - plt.ylabel("Density")
          - plt.xticks([5,10,15,20,25,30,35,40,45,50])
          - plt.yticks()
          - plt.savefig("histogram.png")
          - plt.show()


- 5) **Scatterplot**


<p>
  <img src ="https://github.com/user-attachments/assets/aba41e90-f5d7-4e19-971d-845914824c79" width = 400>
</p>

<p>
   <img src ="https://github.com/user-attachments/assets/06ed3607-49b5-46f5-b9e7-51f1731778a8" width = 400>
</p>

##### We practiced other visualization of data
<p>
  <img src ="https://github.com/user-attachments/assets/b1e35ce4-988f-4b0a-839f-64dde5ded9fc">
</p>

<p>
 <img src ="https://github.com/user-attachments/assets/5a45db07-df33-4da0-83cb-0c79bb009a9e">
</p>
here we saw how to achieve a simple visual representation of data using pandas - doesnt give more informations


## Features Extraction and Transformation
Involve selecting, deriving, or converting raw data into meaningful and usable features for a model.
Feature Extraction
- involves reducing the dimensionality of the data while preserving its relevant information. 
- It focuses on identifying important characteristics of the data.

**Featurization**
- Text data
	- Bag of Words-Converts text into word frequency vectors.
	- TFIDF-Weighs words by their frequency and uniqueness.

### Feature Engineering
- **Feature Orthogonality**
	- orthogonality-dotpdt ()=0. Feature relations are different in direction when in 3d, in 2d they are perpendicular.
	- {eg: features1,2,3 and target}
	- cosine similarity will also be zero. Cosine sim = u.v/||u|| ||v||

- **Collinearity**
	- when some features are related, ed if f2=1.5f1, then we can rewrite it as;
	- f1, 1.5f1, f2
	- when, any features are colinear, then its combine effect will not make any specific changes in the target, or output

***Between targets there should be collinearity and between features there should be orthogonality***


- **Feature Slicing**
	- height, weight, hair color, eye color, country ----- we need to predict Gender
	- suppose we have info regarding two countries(India(majority[80%]) and USA(rest)[20%])
	- For feature slicing there are some conditions to be followed
		- there should be inequality between two data
		- even if there is inequality, the smaller data should have necessary datapoints(for say 100k)
		- This inequality is necessary to check two models. If equal data are checked, it won't give a difference in two models.

- **Feature Binning**
	- to convert certain data into categories, >150, <150, >120,<120(on multiple categories)
 - dividing continuous variables into discrete intervals or bins.

- **Indicator variable**
	- when categorization is binary {just as <150, and >150}
 - binary variable that indicates the presence (1) or absence (0) of a specific condition or category.

- **Mathematical Transformation**
	- Logarithms
		- if converting larger values into logs, we can compress histograms more to the left side(as larger values lies on the right side of the graph)
		- after that we can take the antilogs of these values to get the initial value.
	- Boxcox 
		- more sophisticated than logs

### HEAT MAPS
Get most of teh informations regarding correlation of all the parameters of teh dataset under a single graph.

<p>
  <img src ="https://github.com/user-attachments/assets/c81b09f9-b354-45c9-b22b-33c515cbfa42"> 
</p>

### BOX PLOT
Easier to find outliers

<p>
  <img src ="https://github.com/user-attachments/assets/231a0432-b403-46c7-a506-b2eb4383cd0a"> 
</p>


**we can also trasnform data and compare the old ones with transformed ones**

<p>
  <img src ="https://github.com/user-attachments/assets/54333e96-e371-459a-bde1-1580b2881bd7"> 
</p>


