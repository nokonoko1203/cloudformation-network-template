# cloudformation-network-template

クラウドフォーメーションを利用して以下を作成します
- パブリックサブネット2つ
- プライベートサブネット2つ
- データベースインスタンス1つ（プライベートサブネット）

## 使い方

- 作成

```bash
% aws cloudformation create-stack \
  --stack-name sample-stack \
  --region ap-northeast-1 \
  --template-body file://template.yml \
  --parameters file://parameters.json \
  --capabilities CAPABILITY_NAMED_IAM
```

- 更新

```bash
% aws cloudformation update-stack \
  --stack-name sample-stack \
  --template-body file://template.yml \
  --parameters file://parameters.json \
  --capabilities CAPABILITY_NAMED_IAM
```

- 削除

```bash
% aws cloudformation delete-stack --stack-name sample-stack
```