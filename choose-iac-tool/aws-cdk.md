# AWS CDK を IaC ツールとして使用する

AWS クラウド開発キット ([AWS CDK](https://docs.aws.amazon.com/ja_jp/cdk/v2/guide/home.html)) は、使い慣れたプログラミング言語を使用してクラウド アプリケーション リソースを定義できるオープンソースのソフトウェア開発フレームワークです。AWS CDK は、JavaScript、TypeScript、Python、Java、C#、Go をサポートしています。AWS CDK は、AWS CloudFormation を通じて、安全で繰り返し可能な方法でリソースをプロビジョニングします。AWS CDK コードを合成すると、CloudFormation テンプレートが作成されます。AWS CDK は、AWS リソースの定義プロセスを簡素化する高レベルの抽象化を提供します。

AWS CDK は、[コンストラクト](https://docs.aws.amazon.com/ja_jp/cdk/v2/guide/constructs.html)の概念を使用します。コンストラクトは 、Amazon Simple Storage Service (Amazon S3) バケットなど、1 つ以上の CloudFormation リソースとその構成を表すアプリケーション内のコンポーネントです。コンストラクトは、より複雑なインフラストラクチャを作成するために、構成およびカスタマイズできます。詳細については、 AWS CDK ドキュメントの「[コンストラクト レベル](https://docs.aws.amazon.com/ja_jp/cdk/v2/guide/constructs.html#constructs_lib_levels)」を参照してください。AWS CDK は、開発者が記述したコードに基づいて CloudFormation テンプレートを生成します。これにより、手動で CloudFormation テンプレートを作成する必要がなくなります。多くの組織は、他のソフトウェア ライブラリと同様に、コミュニティ内でコンストラクトをカスタマイズ、共有、再利用します。コンストラクトを共有することで、開発者はより速くコーディングし、デフォルトでベストプラクティスを組み込むことができます。

AWS CDK [アスペクト](https://docs.aws.amazon.com/ja_jp/cdk/v2/guide/aspects.html)は、組織が特定のスコープ内のすべての構成要素に標準を適用するのに役立ちます。アスペクトは、タグを追加するなどして構成要素を変更できます。または、構成要素の状態について何かを検証することもできます。

AWS CDK を使用すると、開発者は既存のプログラミング スキルと知識を使用してクラウド インフラストラクチャを定義できます。使い慣れたプログラミング言語を使用することで、開発者は専門知識を AWS リソースの記述に適用でき、アプリケーション開発からインフラストラクチャのプロビジョニングへの移行が容易になります。また、AWS CDK を使用すると、AWS インフラストラクチャの作成を迅速化できます。これにより、CloudFormation テンプレートを手動で記述する場合と比較して、開発ライフサイクルが加速されます。

### AWS CDK を使用する利点:

- AWS CDK は、よく知られたプログラミング言語をサポートしています。
- 汎用言語では、for ループ、オブジェクト、強力な型、その他のプログラミング手法などの論理構造を使用できます。これにより、開発者はインフラストラクチャを簡潔かつエラーのない方法で宣言できます。このアプローチにより、統合開発環境 (IDE) と関連ツールを使用して、多数のリソースの宣言に伴う複雑さを管理することも可能になります。
- AWS CDK コンストラクトは共有可能であり、ガバナンスとコンプライアンスの要件を満たすのに役立ちます。
- AWS CDK コンストラクトを使用すると、開発にかかる時間と労力を削減できます。詳細については、[コンストラクトライブラリ API リファレンス](https://docs.aws.amazon.com/cdk/api/v2/docs/aws-construct-library.html)を参照してください。
- AWS CDK は CloudFormation に基づいています。CloudFormation とその概念に精通していれば、AWS CDK の概念を理解しやすくなります。
- AWS CDK は、[ユニットテストとスナップショットテスト](https://docs.aws.amazon.com/ja_jp/cdk/v2/guide/testing.html)の実行に役立ちます。
- 機能が AWS CDK でネイティブにサポートされていない場合は、[レベル 1 コンストラクト](https://docs.aws.amazon.com/ja_jp/cdk/v2/guide/constructs.html#constructs_lib_levels_one)と [raw overrides](https://docs.aws.amazon.com/ja_jp/cdk/v2/guide/cfn_layer.html#cfn_layer_raw) を使用できます。または、API を直接呼び出す [CloudFormation カスタムリソース](https://docs.aws.amazon.com/ja_jp/AWSCloudFormation/latest/UserGuide/template-custom-resources.html)を使用することもできます。
- CloudFormation スタックを削除することで、リソースを効率的にクリーンアップできます。

### AWS CDK を使用する場合の欠点:

- AWS CDK では、各 AWS アカウントに[ブートストラップされた環境](https://docs.aws.amazon.com/ja_jp/cdk/v2/guide/bootstrapping.html)が必要です。ブートストラップは、リソースをデプロイする環境ごとに実行する必要がある 1 回限りのアクションです。
- AWS CDK は、AWS クラウドにのみ IaC をデプロイするために使用できます。

---

- [導入](./introduction.md)
- [IaC の利点](./benefits.md)
- [IaC ツール](./iac-tools.md)
  - [AWS CloudFormation](./cloudformation.md)
  - [AWS SAM](./aws-sam.md)
  - [**AWS CDK**](./aws-cdk.md)
  - [Terraform](./terraform.md)
  - [Pulumi](./pulumi.md)
- [ツールの選択](./choose-tool.md)
- [次のステップ](./next-steps.md)
