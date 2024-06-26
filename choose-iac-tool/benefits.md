# IaC を実装するメリット

組織に適した IaC ツールを選択することで、次のようなメリットが得られます。

- **スピード** – IaC の目標の 1 つは、手動プロセスを排除して作業を高速化することです。コードベースのアプローチにより、より短時間でより多くの作業を簡単に行うことができます。各 IT 環境を手動で設定するのは非常にコストがかかり、ハードウェアとソフトウェアの設定には専任のエンジニアとアーキテクトが必要です。スピードを上げることで、組織は変化する顧客のニーズや市場の状況に素早く適応できるようになります。また、IaC コードを 1 回記述すれば、手動で作成する場合のほんのわずかな時間で、同じコードを何百もの環境に展開できます。

- **スケーラビリティ** – IaC を使用すると、既存のインフラストラクチャにリソースを簡単に追加できます。アップグレードは迅速にプロビジョニングされるため、使用ピーク時に迅速に拡張できます。たとえば、オンライン サービスを実行している組織は、ブラック フライデーなどの需要の高い期間にユーザーの需要に対応するために拡張できます。

- **強化されたセキュリティ** – IaC は、組織のセキュリティとコンプライアンスを実現するのに優れています。組織は、ベースラインのセキュリティ ポリシーと構成を設定し、IaC に対して自動テストを実行することで、パイプラインを通じてそれらを適用できます。IaC がコンプライアンス ルールに違反すると、パイプラインは失敗し、開発者に自動的にフィードバックが返されます。これにより、安全でないインフラストラクチャの作成を防ぐことができます。

- **一貫性** – 一貫性は IaC のもう 1 つの重要な利点です。複数のエンジニアが手動で構成を展開する場合、不一致は避けられません。時間が経つにつれて、同じ環境を追跡して再現することが難しくなります。これらの不一致は、開発環境、QA 環境、および本番環境の間に重大な違いをもたらすことがよくあります。

- **効率** – IaC は開発ライフサイクル全体の効率と生産性を向上させます。プログラマーはサンドボックス環境を作成し、分離して開発します。運用部門はセキュリティ テスト用のインフラストラクチャを迅速にプロビジョニングできます。QA エンジニアはテスト中に本番環境の正確なコピーを保持します。展開の準備ができたら、開発者はインフラストラクチャとコードの両方を 1 つの手順で本番環境にプッシュします。また、より高いレベルのコラボレーションとチームワークも実現できます。チームはアプリケーションの安全なパターンを作成し、それらのテンプレートまたは構造を他のチームと共有できるため、重複作業が削減されます。

- **コストの削減** – IaC はソフトウェア開発のコストを削減します。環境を手動で設定するためにリソースを費やす必要はありません。実際に使用しているリソースに対してのみ料金を支払うため、不必要なオーバーヘッドはありません。

- **信頼性の向上** – インフラストラクチャが大きい場合、リソースを誤って構成したり、サービスを間違った順序でプロビジョニングしたりすることが容易になります。IaC を使用すると、リソースは常に宣言どおりにプロビジョニングおよび構成されます。リソースを手動で作成するとエラーが発生しやすいため、IaC を使用すると、インフラストラクチャが意図したとおりに作成されるという高い信頼性が得られます。

- **構成ドリフトの検出** – 構成ドリフトは、環境をプロビジョニングした構成が実際の環境と一致しなくなった場合に発生します。多くの IaC ツールは、ドリフトを検出して修正するのに役立ちます。たとえば、誰かがリソースを手動で誤って変更した場合、IaC ツールを使用して変更内容を検出し、意図した状態に復元できます。

- **実験** – IaC を使用すると、新しいインフラストラクチャのプロビジョニングが非常に迅速かつ簡単になるので、多くの時間とリソースを投資することなく、実験的な変更を加えてテストできます。結果に満足したら、新しいインフラストラクチャをすぐに本番環境にスケールアップできます。

---

- [導入](./introduction.md)
- [**IaC の利点**](./benefits.md)
- [IaC ツール](./iac-tools.md)
  - [AWS CloudFormation](./cloudformation.md)
  - [AWS SAM](./aws-sam.md)
  - [AWS CDK](./aws-cdk.md)
  - [Terraform](./terraform.md)
  - [Pulumi](./pulumi.md)
- [ツールの選択](./choose-tool.md)
- [次のステップ](./next-steps.md)
