<h2> 🖱 User Response Prediction what, Why and How ?</h2>
<img align='right' src='https://miro.medium.com/max/960/1*hIPMAi6s0xF23Y8GWcPWWA.gif' style='width:300px;height;160px;'></img>

- multibillion-dollar industry, internet advertising provides a shared marketing
experience when customers access online services via electronic,different types of advertisers and search engines repy on modeling to predict ad CTR accurately.

- When users click on displayed adverts, payment/revenue is made between advertisers and publishers. As a result, designing a user response-based pricing model is critical for both advertisers and publishers.

- CTR is a metric commonly used in online advertising to measure the effectiveness of an ad campaign. It represents the ratio of users who click on a specific link (such as an ad) to the number of total users who view the ad.

- we will be predicting the ad click-through rate using the machine learning approch

<h2> > ✒ Probelm statement </h2>
- Develop a machine learning algorithm that predict a particular user will click on an advertisment.

<h2> 📂 Dataset </h2>

- Dataset consist 10 attributes
- **`Daily Time Spend on Site`,`Age`,`Area Income`,`Daily internet usage`,`Ad topic line`,`City`,`Gender`,`Country`,`Timestamp` and `Clicked on Ad`**
- **`Clicked on Ad` is output attribute and rest 9 input attributes those are accuretly to predict user will click on ad or not**

<h2> 🔍 Meta information about Dataset attributes </h2>

- **`Daily Time Spend on Site`** user daily time spend on website
- **`Age`** Its denotes which age group user come on website
- **`Area Income`** user earn total money annual
- **`Daily internet usage`** Its denote user how much internet use daily
- **`Ad topic line`** The goal is to create a product to share information about a product, obtain customer information, and encourage customers to continue with the company beyond the content
- **`Gender`** Its denote user come from which categories(Male or Femele)
- **`Country`** User belong from which country
- **`Clicked on Ad`** There assign (0 or 1) user click or not on advertisment


<h2> Issues with Dataset and Solution </h2>

1. Dirty Data
- **`Daily Time Spent on Site->`** 
    - Zero null value
    - Convert datatype into float32
    - Not Normal Distribution

- **`Age`**
    - Zero null value
    - Convert datatype into int32
    - Almost Normal Ditribution

- **`Area Income`**
    - Zero null value
    - almost normal distribution

- **`Daily Internet Usage`**
    - Zero null value
    - almost normal distribution
    
- **`Ad Topic Line`**
    - Zero null value
    - there is 50 sub categores more dominate to other sub categories `Imbalanced Ad topic line attribute`
    - we will drop this atttribute bcz here 559 different vategories and it will not play a important role for prediction
    
- **`Gender`**
    - zero null value
    - `53.76%` Female and `46.24%` Male `Balanced gender Attribute`
    - onehotencoding apply convert into numerical

- **`Click on Ad`**
    - Zero null value
    - `50.83%` -> 0 and `49.17%` -> 1 `balanced click on ad attribute`


2. Messay Data

- **`Duplicate`** Drop duplicate values
- **`Transformation and scaling`**
    - **`Daily Time Spent on Site`,`Age`,`Area of Income`,`Daily Internet Usage`:-** we apply here Scaling or Transformatkion
- **`Timestamp`** Month extract from timestamp attribute and drop timestamp attribute
- **`Gender` ,`Timestamp_month`** onehotencoding apply convert into numerical 
