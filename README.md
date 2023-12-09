# learning-github-actions
A self-learning guide to using GitHub Actions

CI = Continuous Integration
CD = Continuous Deployment

Because programmers are lazy, typically they will just say CI/CD when they are not really sure which one they are doing but want to sound like they know what they are doing.

Automate building, testing and deployment of code

This field of work is known as DevOps (short for ~~Developer...wOopsiesArbitraration~~ software Development IT Operations). Professionals in this field are known for their chivalry in the battle against entropy, cold brews and tears.

# ML Project Lifecycle
![Diagram of a project life cycle courtesy of DataScientest](img.png)
1. Data preparation: Turning raw data into a form that can be used for machine learning, where the key and somewhat odd assumption common in the software community today is that we __need__ or even __want__ machines to learn from every piece of data
2. Model Training: Designing and setting an appropriate machine learning model for answering a question. Typically the responsibility of a *data scientist*
3. Model Deployment: Once the model is good enough, the model needs to get to the people who need it. This is where we put on a *data engineer* or *machine learning engineer* hard hat
4. New raw data: Very often new data comes in after deployment of the model. There's always new stuff to learn! Cue start the process again

# Automation tools for CI/CD
* GitHub Actions
* Jenkins 
* Travis
* BitBucket Pipelines
* Azure DevOps Pipelines
* GitLab Actions
* Tekton (containers) 

GitLab CI offers a free version for self-hosted deployments, and Tekton is entirely open-source and free to use.

This repo is on GitHub, so we're going to have a look at GitHub Actions [1](https://www.stakater.com/post/github-actions-vs-bitbucket-pipelines-vs-gitlab-ci-vs-tekton-bestcicdtool)

## GitHub Actions
![GitHub Actions diagram courtesy of DataScientest](https://dst-de.s3.eu-west-3.amazonaws.com/git_github_en/Github+action.jpg)

* Events: Trigger a workload
* Jobs: A set of steps that execute on a machine (aka a "runner" to our octopus friends at GitHub)
* Steps: Individual tasks that run commands on a job. Can be an action or a shell script
* Actions: A command that is executed on a runner
* Runners: A GitHub actions server. Listens for available jobs, runs them in __parallel__ and reports on progress. Each runner can run on GitHub or on a localized server