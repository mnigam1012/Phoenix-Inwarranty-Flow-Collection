# Postman API Automation Integration with GitHub Actions #

This repository is a demonstration for PoC for integrating Postman tests with GitHub Actions. The tests are written in Postman and they are executed on the VM with the help of Newman and newman-reporter-htmlextra.
GitHub Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a scheduled time with the help of a cron job.

The HTML report is archived and kept in the artifact section for the team to download it. Along with that, they can view the report directly from the GitHub page:https://mnigam1012.github.io/Phoenix-Inwarranty-Flow-Collection/
The latest report is mailed to the team members using Gmail SMTP.

## About me ##
__

## Testing Coverage ##
1. Happy flow Testing
2. Negative testing and edge cage testing
3. Token Testing
4. Data Driven testing with CSV
5. Schema Validataion
6. Secrets maangement with Github Secrets

## Tech Stack ##
1. Postman
2. Node.js (>= v20)
3. Newman
4. newman-reporter-htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV (for Data-Driven Testing)
9. AWS EC2 instance for self-hosted GitHub runner

## GitHub Pages ##
You can directly view the latest test report of the Postman test at the GitHub Page link:https://mnigam1012.github.io/Phoenix-Inwarranty-Flow-Collection/

## HTML Report ##
The Report will be created in the Newman folder:
![Postman Report](https://raw.githubusercontent.com/mnigam1012/Phoenix-Inwarranty-Flow-Collection/static-content/html-report.jpg)

## Project Structure ##
```
Phoenix Inwarranty Flow Collection
├─ Inwarranty-flow Collection by jatin Copy.postman_collection.json # Collection file
├─ QA.postman_environment.json # Environment File
└─ testData.csv # TestData File

```

## How to Run the Project? ##
You can run the project on your local system. For that:
1. Clone the Project on Local System: https://github.com/mnigam1012/Phoenix-Inwarranty-Flow-Collection.git
2. Install Node.js and NPM from:https://nodejs.org/en
3. Install Newman using NPM: ```npm install -g newman```
4. Install newman-reporter-htmlextra using NPM: ```npm install -g newman-reporter-htmlextra```
5. Run the Newman Command:
   
 ```
newman run 'Inwarranty-flow Collection.postman_collection.json' \
  -e QA.postman_environment.json \
  -d testdata.csv \
  -r cli,htmlextra \
  --reporter-htmlextra-export ./newman/index.html

```


 
