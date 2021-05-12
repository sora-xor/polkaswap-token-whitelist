@Library('jenkins-library') _

def pipeline = new org.js.LibPipeline(
    steps: this,
    test: false,
    dockerImageName: 'soramitsu/polkaswap-token-whitelist-js-library',
    buildDockerImage: 'build-tools/node:14-ubuntu',
    buildCmds: ['yarn', 'NODE_ENV=production yarn build'],
    pushCmds: ['npm publish'],
    npmRegistries: ['': 'npm-soramitsu-admin'],
    npmLoginEmail:'admin@soramitsu.co.jp')
pipeline.runPipeline()