# Logistic Regression

Logistic Regression is a Machine Learning classification algorithm that is used to predict the probability of a categorical dependent variable. In logistic regression, the dependent variable is a binary variable that contains data coded as 1 (yes, success, etc.) or 0 (no, failure, etc.). In other words, the logistic regression model predicts P(Y=1) as a function of X.

Logistic Regression Assumptions
Binary logistic regression requires the dependent variable to be binary.
For a binary regression, the factor level 1 of the dependent variable should represent the desired outcome.
Only the meaningful variables should be included.
The independent variables should be independent of each other. That is, the model should have little or no multicollinearity.
The independent variables are linearly related to the log odds.
Logistic regression requires quite large sample sizes.
Keeping the above assumptions in mind, let’s look at our dataset.

Data
The dataset comes from the UCI Machine Learning repository, and it is related to direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict whether the client will subscribe (1/0) to a term deposit (variable y). The dataset can be downloaded from <a href="https://raw.githubusercontent.com/madmashup/targeted-marketing-predictive-engine/master/banking.csv"> here.</a>

The dataset provides the bank customers’ information. It includes 41,188 records and 21 fields.

Input variables

age (numeric)
<br>
job : type of job (categorical: “admin”, “blue-collar”, “entrepreneur”, “housemaid”, “management”, “retired”, “self-employed”, “services”, “student”, “technician”, “unemployed”, “unknown”)
<br>
marital : marital status (categorical: “divorced”, “married”, “single”, “unknown”)
<br>
education (categorical: “basic.4y”, “basic.6y”, “basic.9y”, “high.school”, “illiterate”, “professional.course”, “university.degree”, “unknown”)
<br>
default: has credit in default? (categorical: “no”, “yes”, “unknown”)
<br>
housing: has housing loan? (categorical: “no”, “yes”, “unknown”)
<br>
loan: has personal loan? (categorical: “no”, “yes”, “unknown”)
<br>
contact: contact communication type (categorical: “cellular”, “telephone”)
<br>
month: last contact month of year (categorical: “jan”, “feb”, “mar”, …, “nov”, “dec”)
<br>
day_of_week: last contact day of the week (categorical: “mon”, “tue”, “wed”, “thu”, “fri”)
<br>
duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y=’no’). The duration is not known before a call is performed, also, after the end of the call, y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model
<br>
campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
<br>
pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
<br>
previous: number of contacts performed before this campaign and for this client (numeric)
<br>
poutcome: outcome of the previous marketing campaign (categorical: “failure”, “nonexistent”, “success”)
<br>
emp.var.rate: employment variation rate — (numeric)
<br>
cons.price.idx: consumer price index — (numeric)
<br>
cons.conf.idx: consumer confidence index — (numeric)
<br>
euribor3m: euribor 3 month rate — (numeric)
<br>
nr.employed: number of employees — (numeric)
<br>
Predict variable (desired target):
y — has the client subscribed a term deposit? (binary: “1”, means “Yes”, “0” means “No”)
