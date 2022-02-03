pipeline{
  agent{
    docker{
      image "gcc-format"
      args "-v /home/talha/docker/gcc-format/:/home/gcc-format/"
    }
  }
  stages{
    stage("c-control"){
      steps{
        sh "clang-format --dry-run --Werror /home/gcc-format/fibo-true.c"
        echo "$?"
      }
    }
  }
}
