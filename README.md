# Postman API Automation Integration With GitHub Actions #

This repositary is a demonstration for poc for integrating postman tests with github actions. The tests are writtern in postman and they are executed on the virtual machine with the help of Neman and newman-reporter-htmlextra. 
Github action will trigger on evry main branch push. You can also execute the project manually using workflow_dispatch. The projects runs on schedule time with the help of cron job.

The html report is archived and kept in the artifect section for the team to downloads along with that they can view the report directly from the github page.
The latest report is made to the team members using Gmail SMTP.

## Aboout Me ##
Hi My Name is Ronak Patel. I have 4 years and 11 months of experience in Automation Testing. My skill sets include UI automation with Selenium webdriver and for API testing I used restassured and postman.

You can connect with me over LinkedIn : https://www.linkedin.com/in/ronakpatel07/


## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation Testing
6. Secrets Management With Github Secretes

## Tech Stack ##
1. Postman
2. Newman
3. Node.js 23.6.1v
4. Github Actions
5. Gmail SMTP
6. Newman-Reported-Htmlextra
7. Github Pages
8. CSV for Data Driven Testing
9. AWS EC2 instance for Self hosted github runner

## GitHub Pages ##
You can directly view the latest test report of the Postman test at the Github page : https://rnk07.github.io/APITesting-Postman/

## HTML Report ##
The Report will be created in the newman folder.
![Postman Report](https://github.com/rnk07/APITesting-Postman/blob/static-contant/NewmanReport.PNG)

## Project Structure ##

```
API Testing Collection
├─ collectionCSV.json # Collection File
├─ data.csv # Data File
└─ env.json # Environment File

```

## How To Run The Porject ##
You can run the project on your local system for that:
1. Clone the project on your local system: ```https://github.com/rnk07/APITesting-Postman.git```
2. Then Install Node.js and NPM from ``` https://nodejs.org/en ```
3. Install Newman using : ``` npm install -g newman ```
4. Instal Newman-reported-htmlextra using : ``` npm install -g newman-reporter-htmlextra ```
5. Run the newman Command :
```
   newman run collectionCSV.json \
                            -e env.json \
                            -d data.csv \
                            -r cli,htmlextra \
                            --reporter-htmlextra-export newman/index.html ```
