# Purpose of each workflow

## dependent-jobs.yml
This workflow has the main purpose of running actions on a step basis, here, jobs will be run only after the previous job is completed successfully, this is very useful as it allows us to build, test and deploy projects automatically, although this is an example, it can be applied on a real scenario with a real project

## multi-platform.yml
This is a really useful workflow as it allows us to perform work on different OS at the same time, this is a really useful thing specially when working on applications that run directly on the machine like Java projects, this lets us know if our application runs properly on the three main OS without the need to create a specific job or workflow for each one. Really useful when we want to deploy to different OS at the same time

# Key concepts demonstrated
The main concepts demonstrated in the exercise are
  - Running on different OS at the same time using runs-on, this is really useful to perform the same, or similar actions on Windows, Linux or MacOS at the same time, and simplifies the need for different projects of workflows as they can be simplified to one project and file
  - Branches and triggers, this is really useful to perform a specific workflow when a certain condition is met, such as what brach is the new code being committed to, if it is a pull request or a commit 
  - Needs, this is really useful, specially when running workflows that need something to be done or executed beforehand to work, this is really useful when performing a build, test and deploy action as it will run everything in steps and will only run the actions if the needed action was completed successfully
  - Environmental variables, this gives us a great level of access to the runner that our code is being run on, it is really useful when it comes to run the application and we need to save important information like keys, or access system information such as the OS version 

# Challenges faced
The only challenge faced on this process was accessing the environmental variables of the runner in the second workflow, at first it seemed difficult to access this data, but after using the RUNNER_OS environmental variable, accessing the data was much easier and similar to a local environment