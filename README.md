# Postman API Automation integration with Github Actions #

This repository is demonstration for POC for integrating postman tests with Github actions.The tests are written in Postman and they are executed on VMs with the help of newman and newman-reporter-htmlextra
Github actions will trigger the project execution on every push to main branch.You can also execute project manually using workflow_dispatchThis project runs on schedule time with the help of cron job

The HTML report is archived and kept in the artifact section for the team to download it. Along with that they can view report directly from the github page: https://karthiksantosh1993.github.io/Phoenix-Inwarranty-Flow.
The latest report is mailed to the team membersusing GMAIL SMTP.

## About me ## 

Hi I am Karthik Duruvasula. I have 6 Years of experience in Automation Testing. My skillset includes Selenium webdriver, playwright. For api testing I use Rest assured and postman 

You can connect with me over: (https://www.linkedin.com/in/karthik-duruvasula-b6972974/)

## Tech stack ##
1. Postman
2. Node.js 22v
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Github Pages
7. Gmail SMTP
8. CSV for Data Driven Testing
9. AWS EC2 instance for self hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman test at the Github Pages https://karthiksantosh1993.github.io/Phoenix-Inwarranty-Flow/

## Testing coverage ##

1. Positive flow Testing
2. Negative flow Testing and Edge case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets managements with github secrets

## Project Structure ##

```
Phoneix-Inwarrentyflow
├─ Inwarranty-Flow Collection.postman_collection.json
├─ QA.postman_environment.json
└─ testdata.csv

```

## How to run the project ? ##

Steps to run the projecton your local machine:
1. Clone the project on local system from the link: https://github.com/KarthikSantosh1993/Phoenix-Inwarranty-Flow.git
2. Install NodeJS and NPM from the link
   ```https://nodejs.org/en/download```
4. Install newman using
   ```npm install -g newman ```
6. Install newman-reporter-htmlextra
   ```npm install -g newman-reporter-htmlextra```
8. run the Newman Command
   ```
          newman run 'Inwarranty-Flow Collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
   ```

## HTML Report ##
The report will be created in newman folder 
![POSTMAN REPORT](https://github.com/KarthikSantosh1993/Phoenix-Inwarranty-Flow/blob/static-resources/newman-report.png)


