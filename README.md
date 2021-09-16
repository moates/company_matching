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

## Approach
Model this as a flow network with costs. Maximize the flow of people to companies, minimize the cost of the match. The 'cost' is how much you care about matching customers over non-customers.
https://networkx.org/documentation/stable/reference/algorithms/generated/networkx.algorithms.flow.max_flow_min_cost.html

## How to run
1. Download Jupyter, Python3
2. Install the Python packages: networkx, pandas (python -m pip install networkx)
3. Clone this repository.
4. In the folder, run jupyter notebook

