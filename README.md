# 📝 English Quiz Generator

大学1年生向け英語必修科目の教師用問題作成ツール

## 機能

- **画像アップロード**: 教師用資料の問題と解答部分をスクリーンショット
- **AI問題生成**: Claude APIが画像を分析し、同じ形式の類似問題を自動生成
- **問題編集**: 生成された問題をブラウザ上で編集可能
- **PowerPoint出力**: 問題スライド＋解答スライドをワンクリックでダウンロード
- **スマホ対応**: PWA対応でホーム画面にアイコン追加可能

## Streamlit Community Cloudへのデプロイ

1. このリポジトリをGitHubにプッシュ
2. https://share.streamlit.io にアクセス
3. 「New app」→ このリポジトリを選択
4. Main file path: `app.py`
5. 「Advanced settings」→「Secrets」に以下を入力:
   ```
   ANTHROPIC_API_KEY = "sk-ant-xxxxxxxxxxxxxxxxxxxxx"
   ```
6. 「Deploy」をクリック

## ローカル実行

```bash
pip install -r requirements.txt
# .streamlit/secrets.toml にAPIキーを設定
streamlit run app.py
```

## 技術スタック

- Python + Streamlit
- Anthropic Claude API（画像分析・問題生成）
- python-pptx（PowerPoint生成）
