def repo_url = 'https://github.com/memsharded/example-boost-poco.git'
def repo_branch = master

node {
    stages {
        stage('Get project') {
            git branch: repo_branch, repo: repo_url
        }
        stage('Install dependencies on ubuntu') {
            sh '''sudo apt-get install python-pip
                  sudo apt-get install libglew-dev libxrandr-dev libxcursor-dev libxinerama-dev libxi-dev cmake
                  sudo pip install PySide2 PyOpenGL
            '''
        }
        stage('Build') {
            sh 'cmake ../'
        }
    }
}
