# AWS CloudFormation を IaC ツールとして使用する

[AWS CloudFormation](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/Welcome.html)は、テンプレートファイルを使用して AWS リソースのプロビジョニングを自動化する AWS サービスです。デプロイするすべての AWS リソースを記述したテンプレートを作成すると、CloudFormation がそれらのリソースをプロビジョニングして構成します。

CloudFormation テンプレートは、JSON または YAML を使用して記述されます。CloudFormation スタックは、テンプレートで定義されたリソースの実装です。CloudFormation スタックは、AWS マネジメントコンソール、CloudFormation SDK によるプログラム、または AWS コマンドラインインターフェイス (AWS CLI) を通じて管理できます。CloudFormation の仕組みの詳細については、CloudFormation ドキュメントの「[AWS CloudFormation の概念](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/cfn-whatis-concepts.html)」および「[AWS CloudFormation の仕組み](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/cfn-whatis-howdoesitwork.html)」を参照してください。

### CloudFormation を使用する利点:

- CloudFormation の[変更セット](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/cfn-whatis-concepts.html#cfn-concepts-change-sets)を使用すると、実行中のスタックへの変更をデプロイする前にプレビューできます。変更セットは、既存のスタック内の実行中のリソースへの提案された変更をまとめたものです。これにより、デプロイ前に競合や予期しない結果を特定できます。たとえば、Amazon Relational Database Service (Amazon RDS) データベースインスタンスの名前を変更すると、CloudFormation は新しいデータベースを作成し、古いデータベースを削除します。古いデータベースをバックアップしていない限り、古いデータベースのデータは失われます。変更セットを生成すると、変更によってデータベースが置き換えられることがわかり、スタックを更新する前にそれに応じて計画を立てることができます。
- 変更セットのデプロイ中にエラーが発生した場合、CloudFormation は最後に確認された動作状態に自動的にロールバックします。
- CloudFormation[スタックセット](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html)を使用して、複数の AWS アカウントと AWS リージョンにリソースをデプロイできます。
- AWS::_、Alexa::_、Custom::\* の名前空間のリソースプロバイダーで CloudFormation を使用する場合、追加料金は発生しません。これらの場合、手動でプロビジョニングした場合と同様に、プロビジョニングした AWS リソースに対してのみ料金が発生します。
- CloudFormation は状態を管理します。つまり、CloudFormation は AWS に対して基盤となるサービス呼び出しを行い、CloudFormation テンプレートで定義されているとおりにリソースをプロビジョニングおよび構成します。
- CloudFormation は、設定のドリフトを検出して修正するためのツールを提供します。詳細については、CloudFormation ドキュメントの「[スタックとリソースに対する管理されていない設定変更の検出](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift.html)」を参照してください。
- CloudFormation を使用して[カスタムリソース](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/template-custom-resources.html)を作成できます。スタックを作成、更新、または削除するたびに CloudFormation が実行するテンプレートにカスタムプロビジョニングロジックを記述できます。
- CloudFormation は、 [CloudFormation レジストリ](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/registry.html)を使用してサードパーティのアプリケーション リソースのモデリング、プロビジョニング、管理をサポートします。
- CloudFormation は、[既存のリソース](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/resource-import.html)を CloudFormation 管理にインポートすることをサポートしています。

### CloudFormation を使用する場合の欠点:

- JSON や YAML の構文に慣れていない場合は、慣れるまでに時間がかかるかもしれません。JSON は人間が読めるように設計されておらず、インライン コメントを作成できません。YAML ではコメントを作成でき、読みやすくなります。ただし、その構文はタブとスペースに基づいているため、インデントを間違えやすい場合があります。
- CloudFormation はマルチクラウドのデプロイメントをサポートしていません。
- 再利用可能な構造やその他のモジュール化されたコードを作成するには、AWS クラウド開発キット (AWS CDK) などの高レベルの実装を使用する必要があります。

---

- [導入](./introduction.md)
- [IaC の利点](./benefits.md)
- [IaC ツール](./iac-tools.md)
  - [**AWS CloudFormation**](./cloudformation.md)
  - [AWS SAM](./aws-sam.md)
  - [AWS CDK](./aws-cdk.md)
  - [Terraform](./terraform.md)
  - [Pulumi](./pulumi.md)
- [ツールの選択](./choose-tool.md)
- [次のステップ](./next-steps.md)
