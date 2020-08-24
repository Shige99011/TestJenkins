node {
  stage('codebuild') {
    awsCodeBuild(
      projectName: 'sandbox',
      region: 'ap-northeast-1',
      sourceControlType: 'project',
      sourceVersion: env.BRANCH_NAME,
      // CodeBuildにブランチ名を環境変数で渡すため
      envVariables: "[{BRANCH_NAME,${env.BRANCH_NAME}}]",
    )
  }
}
