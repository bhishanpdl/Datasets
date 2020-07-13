# Source
- https://www.kaggle.com/c/prudential-life-insurance-assessment/data

<div class="markdown-converter__text--rendered"><p>In this dataset, you are provided over a hundred&nbsp;variables describing attributes of life insurance applicants. The task is to predict the "Response" variable for each Id in the test set. "Response" is an ordinal measure of risk that has&nbsp;8 levels.</p>
<h2>File descriptions</h2>
<ul>
<li><strong>train.csv</strong> - the training set, contains the Response values</li>
<li><strong>test.csv</strong> - the test set, you must predict the Response variable for all rows in this file</li>
<li><strong>sample_submission.csv</strong> - a sample submission file in the correct format</li>
</ul>
<h2>Data fields</h2>
<table>
<tbody>
<tr>
<td><strong>Variable</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr>
<td>Id</td>
<td>A unique identifier associated with an application.</td>
</tr>
<tr>
<td>Product_Info_1-7</td>
<td>A set of normalized variables relating to the product applied for</td>
</tr>
<tr>
<td>Ins_Age</td>
<td>Normalized age of applicant</td>
</tr>
<tr>
<td>Ht</td>
<td>Normalized height of applicant</td>
</tr>
<tr>
<td>Wt</td>
<td>Normalized weight of applicant</td>
</tr>
<tr>
<td>BMI</td>
<td>Normalized BMI of applicant</td>
</tr>
<tr>
<td>Employment_Info_1-6</td>
<td>A set of normalized variables relating to the employment history of the applicant.</td>
</tr>
<tr>
<td>InsuredInfo_1-6</td>
<td>A set of normalized variables providing information about the applicant.</td>
</tr>
<tr>
<td>Insurance_History_1-9</td>
<td>A set of normalized variables relating to the insurance history of the applicant.</td>
</tr>
<tr>
<td>Family_Hist_1-5</td>
<td>A set of normalized variables relating to the family history of the applicant.</td>
</tr>
<tr>
<td>Medical_History_1-41</td>
<td>A set of normalized variables relating to the medical history of the applicant.</td>
</tr>
<tr>
<td>Medical_Keyword_1-48</td>
<td>A set of dummy variables relating to the presence of/absence of a medical keyword being associated with the application.</td>
</tr>
<tr>
<td>Response</td>
<td>This is the target variable, an ordinal&nbsp;variable relating to the final decision associated with an application</td>
</tr>
</tbody>
</table>
<p><strong>The following variables are all categorical (nominal):</strong></p>
<p>Product_Info_1, Product_Info_2, Product_Info_3, Product_Info_5, Product_Info_6, Product_Info_7, Employment_Info_2, Employment_Info_3, Employment_Info_5, InsuredInfo_1, InsuredInfo_2, InsuredInfo_3, InsuredInfo_4, InsuredInfo_5, InsuredInfo_6, InsuredInfo_7, Insurance_History_1, Insurance_History_2, Insurance_History_3, Insurance_History_4, Insurance_History_7, Insurance_History_8, Insurance_History_9, Family_Hist_1, Medical_History_2, Medical_History_3, Medical_History_4, Medical_History_5, Medical_History_6, Medical_History_7, Medical_History_8, Medical_History_9, Medical_History_11, Medical_History_12, Medical_History_13, Medical_History_14, Medical_History_16, Medical_History_17, Medical_History_18, Medical_History_19, Medical_History_20, Medical_History_21, Medical_History_22, Medical_History_23, Medical_History_25, Medical_History_26, Medical_History_27, Medical_History_28, Medical_History_29, Medical_History_30, Medical_History_31, Medical_History_33, Medical_History_34, Medical_History_35, Medical_History_36, Medical_History_37, Medical_History_38, Medical_History_39, Medical_History_40, Medical_History_41</p>
<p><strong>The following variables are continuous:</strong></p>
<p>Product_Info_4, Ins_Age, Ht, Wt, BMI, Employment_Info_1, Employment_Info_4, Employment_Info_6, Insurance_History_5, Family_Hist_2, Family_Hist_3, Family_Hist_4, Family_Hist_5</p>
<p><strong>The following variables are discrete:</strong></p>
<p>Medical_History_1, Medical_History_10, Medical_History_15, Medical_History_24, Medical_History_32</p>
<p>Medical_Keyword_1-48 are dummy variables.</p></div>
