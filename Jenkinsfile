pipeline{
  agent{
    docker{
      image "gcc-format"
      argc "-v /home/talha/docker/gcc-format/:/home/gcc-format/"
    }
  }
  stages{
    stage("c-control"){
      steps{
        sh "clang-format --dry-run --Werror /home/gcc-format/fibo-true.c"
        sh "clang-format --dry-run --Werror /home/gcc-format/fibo-false.c"
      }
    }
  }
}
