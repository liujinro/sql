# Assignment 1: Design a Logical Model

Model-design
## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).


## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.

## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Based on the requirement, we designed the two types of tables: Type 1 and Type 2. Here are the details:
Type 1: In the type, the customer's address is updated directly in the "customer" table. In other words, the old address would be overlapped by the new address.
Type 2: In this type, a separate "customer address" is used to keep historical address information. In other words, a new customer's address would be updated with a new start date to track the validity period of each address.
As a result, type 1 would overwrite the previous address, so the method would not keep the historical address, which would be precise and decrease the possibility of privacy concerns related to storing historical data.
For type 2, the method increases the privacy implications because it would retain the historical data information. In addition, type 2 needs more data security measurement to protect the privacy of information.
```


## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)


Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
Based on the "AdventureWorks Schema," here are two differences:
1. The AdventureWorks Schema provides more details. For example, the schema uses separate "Adress," "PersonAdress," and "StateProvince" tables to manage their relationships and present the address information. However, my model only tracks historical addresses directly.
2. The schema also includes the data of "Currency" and "CurrencyRate" from the "Currency" table and "CurrencyRate" table for the Sales sector. However, my model did not include the information.
Development of my model:
1. Insert "Adress," "PersonAdress," and "StateProvince" tables.
2. Implement "Currency" and "CurrencyRate" tables to support foreign currency exchange.
```
# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `June 1, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-3-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
