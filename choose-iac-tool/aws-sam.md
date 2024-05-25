# AWS サーバーレスアプリケーションモデル (AWS SAM) を IaC ツールとして使用する

AWS サーバーレスアプリケーションモデル([AWS SAM](https://docs.aws.amazon.com/ja_jp/serverless-application-model/latest/developerguide/what-is-sam.html)) は、 AWS CloudFormation を拡張するツールキットです。サーバーレスアプリケーションをより迅速に作成できるように設計された追加機能が含まれています。AWS SAM テンプレートをデプロイすると、定義されたリソースを作成するために CloudFormation に変換されます。AWS SAM は、[AWS SAM テンプレート仕様](https://docs.aws.amazon.com/ja_jp/serverless-application-model/latest/developerguide/what-is-sam.html#what-is-sam-template)と [AWS SAM コマンドラインインターフェイス (AWS SAM CLI)](https://docs.aws.amazon.com/ja_jp/serverless-application-model/latest/developerguide/what-is-sam.html#what-is-sam-cli) の 2 つの部分で構成されます。AWS SAM テンプレートでは CloudFormation 構文を直接使用できますが、AWS SAM では、サーバーレス開発の高速化に特に重点を置いた独自の構文を提供しています。この短縮構文により、Amazon API Gateway、AWS Lambda、AWS Step Functions リソースなどのサーバーレスリソースの IaC を最適化して定義できます。AWS SAM CLI は、AWS Lambda 関数をローカルでテストしたり、継続的インテグレーションと継続的デリバリー (CI/CD) パイプラインを作成したり、サーバーレスアプリケーションをデプロイするためのコマンドを実行したりするのに役立つ機能を備えた開発者ツールです。

### AWS SAM を使用する利点:

- AWS SAM には CloudFormation と同じ利点があります。
- CloudFormation と比較すると、AWS SAM を使用すると、AWS Lambda を基盤とする Amazon API Gateway などのサーバーレスアプリケーションやリソースをより簡単に作成できます。
- AWS SAM CLI を使用すると、AWS Lambda 関数をローカルでテストできます。デバッグモードで Lambda 関数をローカルで呼び出すと、デバッガーをアタッチできます。デバッガーを使用すると、他のアプリケーションと同じように、コードを 1 行ずつ実行し、さまざまな変数の値を確認し、問題を修正できます。

### AWS SAM を使用する場合のデメリット:

- AWS SAM には CloudFormation と同じ欠点があります。
- AWS SAM は AWS 外では使用できません。

---

- [導入](./introduction.md)
- [IaC の利点](./benefits.md)
- [IaC ツール](./iac-tools.md)
  - [AWS CloudFormation](./cloudformation.md)
  - [**AWS SAM**](./aws-sam.md)
  - [AWS CDK](./aws-cdk.md)
  - [Terraform](./terraform.md)
  - [Pulumi](./pulumi.md)
- [ツールの選択](./choose-tool.md)
- [次のステップ](./next-steps.md)
