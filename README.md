# Bank_Marketing_Campaign
Completed the Cleaning Bank Marketing Campaign Data with Python project on Datacamp. 
For the project, I was asked to work with a bank to clean the data they collected as part of a recent marketing campaign, which aimed to get customers to take out a personal loan. They plan to conduct more marketing campaigns going forward so I needed to ensure it conforms to the specific structure and data types that they specify so that they can then use the cleaned data I provide to set up a PostgreSQL database, which will store this campaign's data and allow data from future campaigns to be easily imported.

I was supplied with a csv file called "bank_marketing.csv", which needed to be cleaned, reformatted, and split the data, saving three final csv files. 
# Cleaning requirements for client.csv
| column name   | data type  | description   | cleaning requirements |
|------------|------------|------------|------------------------|
| job        | object     | Clients type of job | Change "." to "_" |
| education  | object     | Clients level of education | Change "." to "_" and "unknown" to np.NaN |
| credit_default | bool   | Whether the client's credit is in default | Convert to boolean data type: 1 if "yes", otherwise 0 |
| mortgage | bool | Whether the client has an existing mortgage (housing loan) | Convert to boolean data type: 1 if "yes", otherwise 0 |

# Cleaning requirements for campaign.csv
| column name   | data type  | description   | cleaning requirements |
|------------|------------|------------|------------------------|
| previous_outcome | bool | Outcome of the previous campaign | Convert to boolean data type: 1 if "success", otherwise 0. |
| campaign_outcome | bool | Outcome of the current campaign | Convert to boolean data type: 1 if "success", otherwise 0. |
| credit_default | bool   | Whether the client's credit is in default | Convert to boolean data type: 1 if "yes", otherwise 0 |
| last_contact_date | datetime | Last date the client was contacted | Create from a combination of day, month, and a newly created year column (which should have a value of 2022); Format = "YYYY-MM-DD" |

