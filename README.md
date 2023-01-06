# ps_Test_AzDo

## What's it all about
This project is a demonstration of deploying a PowerShell script using AzureDevOps - the PowerShell file ps_Test_AzDo itself doesn't do anything fancy - it just writes a test file containing a timestamp to a file called ps_Test_AzDo.txt within the %temp% folder. The main detail contained with this project are:

* azure-pipelines.yml - this is the pipeline instruction set that is trigger by the Azure DevOps pipeline project <br><br>
* Invoke-ScriptAnalyzerTest.ps1 - this is called by a Azure Devops pipeline stage to initialise the PowerShell script analyzer against the code in the project. <br><br>
* Invoke-UnitTest.ps1 - this is called by a Azure Devops pipeline stage to initialise Pester tests against the code

IMPORTANT: To run this pipeline you must have an agent pool called "VMAgentPool" or change line 9 of the yaml pipeline to reflect the pool to run the job against.