pipeline {
  agent any
  stages {
    stage('Versioning & Tag') {
      parallel {
        stage('Versioning & Tag') {
          steps {
            echo 'version and tagging to repo is done'
          }
        }
        stage('Label Stories') {
          steps {
            echo 'Labeled stories'
          }
        }
      }
    }
    stage('Unit Testing') {
      parallel {
        stage('Unit Testing') {
          steps {
            echo 'Unit testing is successful'
          }
        }
        stage('Code Analysis') {
          steps {
            echo 'Sonar Code Analysis is completed'
          }
        }
        stage('Security Tests') {
          steps {
            echo 'Security Tests are completed'
          }
        }
      }
    }
    stage('Build & Artifact') {
      steps {
        echo 'Artifacts are stored'
      }
    }
    stage('Deploy to QA') {
      steps {
        echo 'QA is deployed '
      }
    }
    stage('Functional Tests') {
      parallel {
        stage('Functional Tests') {
          steps {
            echo 'Functional Tests are completed'
          }
        }
        stage('Results to Quality Hub') {
          steps {
            echo 'Results are posted to Quality Hub'
          }
        }
      }
    }
    stage('Integration Tests') {
      parallel {
        stage('Integration Tests') {
          steps {
            echo 'Integration Tests are completed'
          }
        }
        stage('Results to Quality Hub') {
          steps {
            echo 'Results are posted to Quality Hub'
          }
        }
      }
    }
    stage('API Testing') {
      parallel {
        stage('API Testing') {
          steps {
            echo 'API tests are completed'
          }
        }
        stage('Results to Quality Hub') {
          steps {
            echo 'Results are posted to Quality Hub'
          }
        }
      }
    }
    stage('Create RFC') {
      parallel {
        stage('Create RFC') {
          steps {
            echo 'RFC is created'
          }
        }
        stage('RFC Apporval') {
          steps {
            echo 'RFC approved'
          }
        }
      }
    }
    stage('Production Deployment') {
      parallel {
        stage('Production Deployment') {
          steps {
            echo 'Production deployment is completed'
          }
        }
        stage('Smoke Testing') {
          steps {
            echo 'Smoke Testing is completed'
          }
        }
      }
    }
    stage('Close CR') {
      steps {
        echo 'CR Is closed'
      }
    }
  }
}