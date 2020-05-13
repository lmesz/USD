node {
    stage('Get project') {
        git branch: "master", repo: "https://github.com/memsharded/example-boost-poco.git"
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
