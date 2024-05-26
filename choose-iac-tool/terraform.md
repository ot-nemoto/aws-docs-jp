# AWS クラウドの IaC ツールとして Terraform を使用する

[HashiCorp Terraform](https://developer.hashicorp.com/terraform) は、クラウド インフラストラクチャの管理に役立つ Infrastructure as Code (IaC) ツールです。Terraform を使用すると、クラウド リソースとオンプレミス リソースの両方を構成ファイルに定義し、バージョン管理、再利用、共有することができます。その後、一貫したワークフローを使用して、ライフサイクル全体にわたってすべてのインフラストラクチャをプロビジョニングおよび管理できます。

開発者は [Terraform 言語](https://developer.hashicorp.com/terraform/language)と呼ばれる高水準の構成言語を使用する Terraform 言語のネイティブな低レベル構文は [HashiCorp Configuration Language (HCL)](https://developer.hashicorp.com/terraform/language/syntax/configuration)です。Terraform 言語は、人間が読み書きしやすいように設計されています。Terraform 言語を使用して、クラウドまたはオンプレミスのインフラストラクチャの望ましい最終状態を記述します。次に、Terraform がその最終状態に到達するための計画を生成し、その計画を実行してインフラストラクチャをプロビジョニングします。

### Terraform を使用する利点:

- Terraform はプラットフォームに依存しません。どのクラウド サービス プロバイダーでも使用できます。AWS や他の多くのクラウド プロバイダーにわたってインフラストラクチャを構成、テスト、およびデプロイできます。組織で複数のクラウド プロバイダーを使用している場合、Terraform はクラウド インフラストラクチャを管理するための単一の統合された一貫したソリューションになります。マルチクラウド サポートの詳細については、[マルチクラウド プロビジョニング](https://www.terraform.io/use-cases/multi-cloud-deployment)を参照してください。Terraform の Web サイトをご覧ください。
- Terraform はエージェントレスです。管理対象のインフラストラクチャにソフトウェアをインストールする必要はありません。
- Terraform モジュールは、コードを再利用し、 Don't Repeat Yourself (DRY)原則に従うための強力な方法です 。たとえば、Amazon Elastic Compute Cloud (Amazon EC2) インスタンス、Amazon Elastic Block Store (Amazon EBS) ボリューム、および論理的にグループ化されたその他のリソースを含むアプリケーションの特定の構成があるとします。この構成またはアプリケーションの複数のコピーを作成する必要がある場合は、コード全体を複数回コピーするのではなく、リソースを Terraform モジュールにパッケージ化し、モジュールの複数のインスタンスを作成できます。これらのモジュールは、構成を整理、カプセル化、および再利用するのに役立ちます。また、一貫性を提供し、ベストプラクティスを保証します。
- Terraform は[ドリフトを検出して管理できる](https://www.hashicorp.com/blog/detecting-and-managing-drift-with-terraform)(Terraform ブログ投稿) をインフラストラクチャで実行します。たとえば、Terraform によって管理されるリソースが Terraform の外部で変更された場合、Terraform CLI を使用してドリフトを検出し、目的の状態に復元できます。

### Terraform を使用する場合の欠点:

- クラウド プロバイダーに関連する新しい機能や新しいリソースのサポートが利用できない場合があります。
- Terraform は AWS CloudFormation のように自動的に状態を管理しません。デフォルトではローカルファイルに保存されますが、[Amazon S3 バケットにリモートで保存](https://developer.hashicorp.com/terraform/language/settings/backends/s3)することもできます。 または [Terraform Enterprise](https://developer.hashicorp.com/terraform/enterprise) を通じて。
- Terraform の状態には、データベースのパスワードなどの機密データが含まれる場合があり、セキュリティ上の懸念が生じる可能性があります。状態ファイルを暗号化し、リモートで保存し、ファイルのバージョン管理を有効にし、読み取りおよび書き込み操作に最小限の権限を使用するのがベストプラクティスです。詳細については、「[AWS Secrets Manager と HashiCorp Terraform を使用して機密データを保護する](https://docs.aws.amazon.com/ja_jp/prescriptive-guidance/latest/secure-sensitive-data-secrets-manager-terraform/introduction.html)」を参照してください。
- 2023 年 8 月、Hashicorp は [Mozilla Public License](https://www.mozilla.org/en-US/MPL/) の下でオープンソースとしてライセンスされなくなると発表した。代わりに、現在は[ビジネスソースライセンス](https://github.com/hashicorp/terraform/blob/b145fbcaadf0fa7d0e7040eac641d9aef2a26433/LICENSE)の下でライセンスされています。。

---

- [導入](./introduction.md)
- [IaC の利点](./benefits.md)
- [IaC ツール](./iac-tools.md)
  - [AWS CloudFormation](./cloudformation.md)
  - [AWS SAM](./aws-sam.md)
  - [AWS CDK](./aws-cdk.md)
  - [**Terraform**](./terraform.md)
  - [Pulumi](./pulumi.md)
- [ツールの選択](./choose-tool.md)
- [次のステップ](./next-steps.md)
