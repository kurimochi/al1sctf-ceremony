# 参加ガイド

このドキュメントは、Groth16 Phase 2 Trusted Setupへの参加手順を説明します。

## ルール

- 必ず **最新 Release の zkey** を使ってください。
- zkey は **GitHub Releases からのみ** 取得してください（PRの添付・外部ミラーは不可）。
- Entropy は **自分で安全に生成** してください（`/dev/urandom`、物理ダイスなど）。
- 作業後は、entropy生成や中間処理に使った一時ファイルを **完全削除** してください。

## 手順

### 前提

- `snarkjs` ([インストールガイド](https://github.com/iden3/snarkjs?tab=readme-ov-file#install-snarkjs))
- `gpg`（署名に使う鍵を用意済み）

### Step 1: 最新 zkey をダウンロード

最新の Releases から `flag_verifier_00XX.zkey` を取得します。

### Step 2: Contribution を実行

```bash
snarkjs zkey contribute flag_verifier_00XX.zkey flag_verifier_00YY.zkey --name="{あなたの名前}" -v
Enter a random text. (Entropy): xxxxxxxxxxxxxxxxxxxxxxxxxx
[INFO]  snarkJS: Circuit Hash:
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
[INFO]  snarkJS: Contribution Hash:
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
                xxxxxxxx xxxxxxxx xxxxxxxx xxxxxxxx
```

- `Enter a random text. (Entropy):` で高品質な entropy を入力します。
- `Circuit Hash` と `Contribution Hash` をそのまま控えてください（attestationに必要）。

`/dev/urandom`由来の乱数を直接渡す例:

```bash
snarkjs zkey contribute flag_verifier_00XX.zkey flag_verifier_00YY.zkey --name="{あなたの名前}" -v -e="$(openssl rand -hex 64)"
```

### Step 3: Attestation を作成

1. `template_attestation.md` をコピーします。
2. 必須項目を記入し、`00XX_{あなたの名前}/attestation.md` として保存します。

### Step 4: 署名を作成

`attestation.md` と同じディレクトリで次を実行します。

```bash
gpg --detach-sign --armor attestation.md
```

`attestation.md.asc` が生成されます。

### Step 5: PR を作成

1. `contrib/00XX` ブランチを作成します。
2. `flag_verifier_00YY.zkey`, `attestation.md`, `attestation.md.sec` が `contributes/00XX_{あなたの名前}` 配下にあることを確認します。
3. `contributes/00XX_{あなたの名前}/` 配下の変更をコミットします。
4. PR を作成します。
