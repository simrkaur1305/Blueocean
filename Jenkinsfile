pipeline {
  agent {
    label 'master'
  }
  stages {
    stage('Deciding Nodes') {
      steps {
        sh 'echo "Deciding nodes"'
      }
    }

    stage('build') {
      steps {
        mail(subject: 'Blueocean Mail', body: 'hgnmbbchkgkh', from: 'sandhaysimran@gmail.com', to: 'sandhaysimran@gmail.com')
      }
    }

  }
  options {
    buildDiscarder(logRotator(daysToKeepStr: '7', numToKeepStr: '50'))
  }
  parameters {
    string(name: 'ZUUL_CHANGE', defaultValue: '')
    string(name: 'ZUUL_PATCHSET', defaultValue: '')
    string(name: 'ZUUL_BRANCH', defaultValue: '')
    string(name: 'ZUUL_PROJECT', defaultValue: '')
    string(name: 'GERRIT_REF', defaultValue: '')
    text(name: 'ZUULEX_COMMIT_MESSAGE', defaultValue: '')
    string(name: 'ZUULEX_CHANGE_OWNER_USERNAME', defaultValue: '')
    string(name: 'TRIGGER_EVENT_TYPE', defaultValue: '')
    string(name: 'CHECKOUT_DIR', defaultValue: 'trs')
    string(name: 'FTP_DIR', defaultValue: '/home/users/trfw')
    string(name: 'FW_CONTACT_EMAIL', defaultValue: 'I_MN_BTS_TRS_FWDEV_BLR@internal.nsn.com')
  }
}