node {
    checkout scm

    docker.withRegistry('http://192.168.0.157:5000') {

        def customImage = docker.build("neo:1.3")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
