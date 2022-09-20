![Zillow-Group-Brand-Logos_010422-01.png](attachment:Zillow-Group-Brand-Logos_010422-01.png)


# <hr style="border-bottom: 10px groove brown; margin-top: 1px; margin-bottom: 1px"></hr>

# Zillow_ Project
by cristian ibarra 

# Project Goals:

Find drivers for single families house on what effect the amount of log error?

Deliver a report that a non-data scientist can read through and understand what steps were taken, why and what was the outcome?



# Project steps:

Step 1: Understanding the Problem.

Step 2: Data Extraction.

Step 3: Data Cleaning.

Step 4: Exploratory Data Analysis.

Step 5: Feature Selection.

Step 6: Testing the Models.

Step 7: Deploying the Model.
# Project Planning:

•Create README.md with data dictionary, project and business goals, come up with initial hypotheses.

•Acquire data from the Codeup Database and create a function to automate this process. Save the function in an acquire.py file to import into the Final Report Notebook.

•Clean and prepare data for the first iteration through the pipeline, MVP preparation. Create a function to automate the process, store the function in a prepare.py module, and prepare data in Final Report Notebook by importing and using the funtion.

•Clearly define four hypotheses, set an alpha, run the statistical tests needed, reject or fail to reject the Null Hypothesis, and document findings and takeaways.

•Establish a baseline accuracy and document well.

•Evaluate models on train and validate datasets.

•Choose the model with that performs the best and evaluate that single model on the test dataset.

•Document conclusions, takeaways, and next steps in the Final Report Notebook.

#  Hypotheses:
`Hypothesis(1)-Does Los angelos county effect log error more the orange county?:`

Ho-Los angelos has a higer log error  then Orange county

Ha-Orange county has a higher log error then Los Angelos

`Hypothesis(2)-Does Ventura county effect log error more then Orange county?:`

Ho-Ventura county has a higher log error then Orange county 

Ha-Ventura county has a lower log error then Orange county


`Hypothesis(3)-Do Bedrooms have a big effect on log error:`

Ho-Does more Bed rooms increase the log error?

Ha-Bed rooms has no effect on log error 

`Hypothesis(4)-Do Bathrooms have a big effect on Log error:`

Ho-Does more bathrooms increase the amount of log error?

Ha-Bathrooms has no effect on the amount of log error

`Hypothesis(5)-Does logerror and squarefeet have a relationship?:`

Ho-Does Squarefeet effect log error ?

Ha-Squarefeet doesnt effect log error

# Goal:
Find what're key drivers of `log error` for single family properties???

# Questions:

• What effect log error on single families houses/properties?

• How does log error increase?

• Can we lower the chance of log error happening with single families properties?

# <hr style="border-bottom: 10px groove brown; margin-top: 1px; margin-bottom: 1px"></hr>

# Data Dictionary/Findings:

### # Data Used-Zillow

|Attribute|Old keys|        Data type   |       Definition   |
| -------- |-------- | -------- | -------- | 
|Bedrooms |bedroomcnt|float |  Number of bedrooms in home |
|Bathrooms |bathroomcnt|float | Number of bathrooms in home including fractional bathrooms|
|Squarefeet |calculatedfinishedsquarefeet|float | Calculated total finished living area of the home |
|TaxesTotal |taxvaluedollarcnt|float|The total property tax assessed for that assessment year 
|Year |yearbuilt|float |The Year the principal residence was built  |
|county |regionidcounty |float |The total tax assessed value of the parcel|
|Zip|regionidzip|object | Federal Information Processing Standard code |
|latitude|latitude|float|cordinates
|longitude|longitude|float|cordinates
|TotalRooms|N/A|float|bathrooms and bedrooms combined 
|location|N/A|object|area houses are located in 
|Decade|N/A|int   |Years slice into half a centary|
|Fips|fips|float|area code
|Taxamount|taxcnt|float|total taxes value
|Log_error|logerror|float|error

# Modeling:

|Model|Train_rmse|Train_r2|Val_rmse|Val_r2|
| ----- | ----- | ----- |----- |----- |
|baseline_mean|0.169201|0.000000|0.155290|0.000000
|Lars_alpha(2)|0.169201|0.000000|0.155290|0.000000
|Depth(1)|0.169032|0.001990|0.155020|0.003439
|Depth(2)|0.168615|0.006912|0.158486|-0.041656
|Depth(3)|0.167665|0.018067|0.826171|-27.312878
|Depth(4)|0.167879|0.015562|0.240463|-1.398220

---
# VALIDATE:
|MODEL | Val_rmse| Val_r2 |
| ----- | ----- | ----- |
|Lars_alpha(2)|0.155290|0.000000
|Depth(1) |0.155020|0.003439
|Depth(2) |0.158486|-0.041656
|Depth(3)|0.826171|-27.312878
|Depth(4)|0.240463|-1.398220


# TRAIN:
|MODEL | Train_rmse |Train_r2|
| ----- | ----- | ----- |
|Lars_alpha(2)|0.169201|0.000000
|Depth(1)|0.169032|0.001990
|Depth(2)|0.168615|0.006912
|Depth(3)|0.167665|0.018067
|Depth(4)|0.167879|0.015562


# Test: 
|MODEL | Test_rmse |Test_r2|
| ----- | ----- | ----- |
|Depth(2)|0.170413|0.002540|

<hr style="border-bottom: 10px groove brown; margin-top: 1px; margin-bottom: 1px"></hr>

# Project description
1)Why this project-
This project would help determind what're the main key aspect of Log error in single family properties thru out the centuries.

2)Why is important-
So we could predict the log error of single family properties and decrease the amount of error made.

3)How does this help you- 
This would help all of us on understanding how and why our single family properties have so much log error.

# Conclusion/Recommnedations/Next Steps:
`Conclusion:`

• We could conclude that bedrooms,bathrooms,decade,county,location,squarefeet have a effect on log error

• In conclusion log error could be effect by many columns and many things so what should we do ?

• We could conclude that the `Polynomial Modellinear regression model` perform the best with a Test_rmse	0.170413



`Recommendations:`

•Addding more data about the areas surronding the houses for example School,Malls,parks,rivers,lakes,hills,views, and much more so would could obtain a more accurate model.

•Would love to keep the cost of something the same but when something is in high demand usually means more houses would sell meaning more log error to happened. 

`Next Steps:`

• I would love to dive into more column in the zillow data set. How a room squarefeet could effect log error more then a basic rooom or how a garage could add more log error then a pool??. This data has so much potential but i would just be digging myself into a rabbit hole.

• I would check 2018 and see how much log error has change from the 2017 data of single families houses

# Steps to reproduce finalnotebook:
zillow data set was collected from codeup server.Using this data to find key driver for log error while using clusters 

1)Download the following files 

• Acquire.py

• Prepare.py

• Modeling.py

• Cluster.py

• finalnotebook.pynd

2) After downloading files make sure all files are in the same folder or location 

3) Onces step two and step one are done you would be able to run finalnotebook without errors and on your own 


# Deliverables:
To access the correct MySQL database, you will need credentials to access to the CodeUp database. This database is accessed in this project via an env.py file. Add the below to your env.py and fill in your individual access information as strings:

user = 'your_user_name'
password = 'your_password'
host = 'the_codeup_db'

1-Readme (.md)-uses as a guide 

2-Acquire (.py)-download

3-Modeling (.py)-download

4-Prepare (.py)-download

5-Final Report (.ipynb)-download 

