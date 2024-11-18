pipeline {
    agent any

    stages {
        stage("Use func") {
            steps {
                myMegaEcho("Hello Dolly");
            }
        }
    }

}

def myMegaEcho(String myString) {
    echo "My string is: ${myString}"
}
