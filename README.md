# Jenkins Masterclass

UDEMY https://www.udemy.com/course/jenkins-masterclass/

All code and configuration created only in educational purposes.

## Links 
- Pipeline Syntax https://www.jenkins.io/doc/book/pipeline/syntax/
- Pipeline: Basic Steps https://www.jenkins.io/doc/pipeline/steps/workflow-basic-steps/
- Jenkins in docker https://github.com/jenkinsci/docker

## Start local Jenkins

```shell
docker compose up
```

Open http://localhost:8080/

## Tricks (Jenkinsfile peline)

### Run the command and store output in a variable

```
    def currentBranch = sh(
        script: 'git rev-parse --abbrev-ref HEAD', 
        returnStdout: true
    ).trim()
```