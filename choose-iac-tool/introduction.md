# 組織に適したコードツールとしてのインフラストラクチャの選択

Infrastructure as Code (IaC) は、一連の構成ファイルを通じてアプリケーションのインフラストラクチャをプロビジョニングおよび管理するプロセスです。IaC は、インフラストラクチャ管理の一元化、リソースの標準化、迅速な拡張を実現して、新しい環境が繰り返し可能で信頼性が高く、一貫性のあるものになるように設計されています。これは、バージョン管理、継続的インテグレーション、継続的デプロイメントなどの Agile および DevOps プラクティスの重要なコンポーネントです。

インフラストラクチャ アズ コード (IaC) ツールの選択は、組織にとって戦略的な決定と見なされます。この決定は、会社のインフラストラクチャ、アプリケーション、およびサービスを構築するすべてのチームに影響します。各ツールには長所と短所があるため、万能のモデルはありません。

これまで、インフラストラクチャの管理とプロビジョニングは、エラーの多い手動のプロセスでした。IaC は、コードを通じてこれらのタスクを効率化し、インフラストラクチャを展開するための信頼性の高いソリューションになりました。IaC ツールにより、開発者はプログラミング言語を使用してインフラストラクチャを定義および展開できます。これにより、ビジネスの俊敏性が向上するだけでなく、成長とイノベーションのスピードも加速します。さらに、IaC により、組織は展開前にコードをスキャンしてインフラストラクチャの信頼性とセキュリティを確認できるため、セキュリティが大幅に向上します。結局のところ、適切な IaC ツールは、単なる技術的な決定ではなく、ビジネス全体の成功に直接影響を与える戦略的な決定です。

このガイドでは、AWS リソースのプロビジョニングに使用できる 5 つの異なる IaC ツール (AWS CloudFormation、AWS Serverless Application Model (AWS SAM)、AWS Cloud Development Kit (AWS CDK)、HashiCorp Terraform、Pulumi) について説明します。これらのツールを比較し、チーム、組織、クラウド人材のニーズを満たすツールを選択するプロセスをガイドします。重要なのは、選択した IaC ツールを組織の目標と開発者のスキルセットに合わせることです。たとえば、チームが JavaScript に精通している場合は、開発ワークフローを最適化するため、主要な IaC ツールとして TypeScript を使用した AWS CDK を選択できます。

---

- [**導入**](./introduction.md)
- [IaC の利点](./benefits.md)
- [IaC ツール](./iac-tools.md)
  - [AWS CloudFormation](./cloudformation.md)
  - [AWS SAM](./aws-sam.md)
  - [AWS CDK](./aws-cdk.md)
  - [Terraform](./terraform.md)
  - [Pulumi](./pulumi.md)
- [ツールの選択](./choose-tool.md)
- [次のステップ](./next-steps.md)