# Company Matching
For a project with Consumer Reports, we are sending data access requests to companies on behalf of consumers. Some of the consumers are customers of the companies, some are not. For sending Data Access Requests, we want to send two DARs for each person, distributed evenly among companies. We prefer to send DARs for customers. Use graph theory to match people to companies!

## Input
* a list of people
* a list of companies
* a matrix of whether a person is a customer of a company
* a max number of DARs to send

## Output
A matrix that matches people to companies. 
(1 match = 1 DAR)

Notes:
* it's better to match people who are customers
* all companies should get roughly the same number of matches
* all people should get roughly the same number of matches
* the average person isn't a customer of B2B companies such as data brokers.

