pipeline {
  agent {label 'master'}
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
  environment {
    GERRIT_CHANGE_NUMBER = "${ZUUL_CHANGE}"
    GERRIT_PATCHSET_NUMBER = "${ZUUL_PATCHSET}"
    GERRIT_BRANCH = "${ZUUL_BRANCH}"
    GERRIT_REFSPEC = "${GERRIT_REF}"
    GERRIT_PROJECT =  "${ZUUL_PROJECT}"
    GERRIT_USERNAME = "${ZUULEX_CHANGE_OWNER_USERNAME}"
    GERRIT_CHANGE_COMMIT_MESSAGE = "${ZUULEX_COMMIT_MESSAGE}"
    STANDARD_COVERAGE = '98.7'
    AUTO_BUILD_WORKSPACE = '/var/fpwork/workspace_trfw/auto_build'
    // SCRIPT_PATH = "${FW_AUTOMATED_SCRIPT_PATH}"
    SCRIPT_PATH = "/home/simrkaur/Projects/"
  }
  stages {
    stage('Deciding Nodes') {
      steps {
        sh 'echo "Deciding nodes"'
      }
    }
  }
}
