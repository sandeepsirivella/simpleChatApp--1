pipeline{
  agent any
  stages{
    stage('checkout SCM'{
      steps{
        branch:'master' ,url:'https://github.com/sandeepsirivella/simpleChatApp--1.git'
      }
    }
    stage('build'){
      steps{
        npm install
        
