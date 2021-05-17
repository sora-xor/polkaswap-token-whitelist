@Library('jenkins-library')

def pipeline = new org.js.LibPipeline(
    steps: this,
    test: false,
    buildDir: './polkaswap-token-whitelist-js',
    buildDockerImage: 'build-tools/node:14-ubuntu',
    buildCmds: ['yarn', 'NODE_ENV=production yarn build'],
    npmRegistries: ['': 'npm-soramitsu-admin'],
    npmLoginEmail:'admin@soramitsu.co.jp',
    gitUpdateSubmodule: true)
pipeline.runPipeline()