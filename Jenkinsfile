pipeline{
  agent any 
  stages{
    stages('1.checkout'){
      steps{
        git url:'https://github.com/Pooja1234866/Dockerbb3',branch:'main'
        }
        }
        stages('2,Build Image'){
          steps{
            bat 'docker build -t Mywebsite .'
          }
        }
        stage('3.stop/Remove old Containers'){
          steps{
            bat'docker stop mycount || exit 0'
            bat'docker rm mycount || exit 0'
          }
        }
        stage('4.run the Image- containerize'){
        step{
          bat'docker run -d -p 5000:80 --name mycount mywebsite'
        }
        }
        }
        }
