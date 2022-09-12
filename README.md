# Detroit_Blight_Ticket_Compliance
This notebook is based on "Detroit Blight Ticket Compliance" competition on Kaggle. The authorities in Detroit issue blight tickets every year to individuals who let their properties remain in deteriorated condition. However, a large number of these blight tickets remain unpaid every year. Enforcing these unpaid blight tickets is a costly affair and authorities want to find ways to maximize compliance with issued blight tickets. The goal of this notebook is to train a model to predict if a blight ticket will be complied with.
"train.csv" contains information about the issued blight tickets. Each row has fields which tell us when, why and to whom was the ticket issued. The compliance field is true if the fine is paid before hearing date or within one month after hearing date and false if fine is paid after one month of hearing date or not paid at all. "addresses.csv" maps from ticket ids to addresses and "latlons.csv" maps from addresses to latitude and longitude of the location of property.
The important columns in training dataset are as follows:
ticket_id 
agency_name - Name of agency that issued ticket
inspector_name  
violator_name 
violation_street_number, violation_street_name, violation_zip_code - Address of property for which ticket was issued
mailing_address_str_number, mailing_address_str_name, city, state, zip_code, non_us_str_code, country - Violator's mailing address
ticket_issued_date 
hearing_date 
violation_code, violation_description - Violation type
disposition - Judgment and its type
fine_amount 
admin_fee - $20 fee assigned for responsible judgments only
state_fee - $10 fee assigned for responsible judgments only
late_fee - 10% fee assigned for responsible judgments only
discount_amount 
clean_up_cost - Cost of clean-up or graffiti removal
judgment_amount - Total fines and fees
grafitti_status - graffiti-violation flag
Area under the ROC curve is used as evaluation metric in this notebook
