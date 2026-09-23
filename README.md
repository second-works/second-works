# SecondWorks

## 業務課題を整理し、AIで使える小さな仕組みに落とし込みます

生成AI・ローカルLLM・RAGを活用した、業務効率化ツールと小規模Webアプリを設計・実装しています。

- 業務文章の要約・改善・タスク抽出
- PDF / TXTなどの業務文書検索と根拠付き回答
- ローカルLLMを利用した、データを外部へ出しにくい構成
- Python / FastAPI、Next.js / Reactによる業務ツール
- Cloudflare Workersを使った公開・運用設計

本業では15年以上、施設管理に携わっています。現場で培った「問題を整理する」「安全性と優先順位を判断する」「運用まで考える」という視点を、AIシステムの設計・実装にも活かしています。

## 代表ポートフォリオ

### AI Business Assistant

業務報告・メール・議事録などを入力し、要約・文章改善・タスク抽出を行うWebアプリです。

- [デモを開く](https://ai-business-assistant.katamachi.workers.dev)
- [リポジトリを見る](https://github.com/second-works/ai-business-assistant)

Next.js / React / TypeScript、OpenAI互換API、Cloudflare Workers（OpenNext）を使用しています。入力検証、エラー表示、レスポンシブUI、秘密情報の分離、Rate Limitingまで実装しています。

### Local RAG Document Assistant

PDF / TXTの業務文書を検索し、文書名・ページ・根拠文章を示して回答するRAGシステムです。

- [デモを開く](https://local-rag-document-assistant.katamachi.workers.dev)
- [リポジトリを見る](https://github.com/second-works/local-rag-document-assistant)

文書登録、ページ情報を保ったチャンク化、Embedding / Vector Search / Generationの分離、検索スコア閾値による回答不能処理を実装しています。ローカルLLM接続とCloudflare Tunnel / Accessを想定し、公開環境ではデモ文書への根拠付きフォールバックも用意しています。

### Facility AI Assistant

施設管理の現場で、設備マニュアル・点検基準・トラブル記録から関連箇所を探し、文書名・ページ・根拠文章を示す業務特化AIのMVPです。危険作業や法令判断を断定せず、管理者・有資格者・専門業者への確認につなげる安全ガードを組み込んでいます。

- [デモを開く](https://facility-ai-assistant.pages.dev/)
- [リポジトリを見る](https://github.com/second-works/facility-ai-assistant)

公開デモは、サーバー・データベース・Secretsを必要としない静的HTML / JavaScript構成をCloudflare Pagesへ配置しています。実データを公開せずに、検索・出典表示・安全な確認フローを低コストで共有・検証できる構成です。OpenAI互換Local LLM接続用アダプターも実装しており、接続先のallowlist、APIキー、timeout、応答形式を検証し、未設定・失敗時は根拠付きフォールバックへ戻します。現在の公開デモは架空サンプル文書とretrieval fallbackで、実Gemma・本番文書・設備操作は未接続です。

### Cloudflare Decap CMS template

架空の地域密着型リフォーム会社サイトを題材に、Astro / Decap CMS / Cloudflare Pagesを組み合わせたWebサイトテンプレートです。Premium Modernのデザインとレスポンシブ表示を実装し、News / WorksをCMSから編集する構成を用意しています。

- [公開デモを見る](https://web-demo.amirkatamachi.com)
- [ソースリポジトリを見る（非公開）](https://github.com/second-works/cloudflare-decap-template)

公開デモではサイトのデザインとページ構成を確認できます。ソースコードは非公開のため、公開成果物はデモサイトです。

### System Monitor Dashboard

ローカルPCのCPU・メモリ・ディスク・OS・Uptimeをブラウザで確認するダッシュボードです。

- [リポジトリを見る](https://github.com/second-works/system-monitor-dashboard)

Python / FastAPI / psutilでAPIを構築し、5秒間隔の自動更新、API障害時のエラー表示、pytest、GitHub Actions CIを実装しています。機能範囲をV1に限定し、運用確認できる小さなWebアプリとしてまとめています。

## 対応できる開発

- 業務フローのヒアリングと要件整理
- 文章作成・文書検索などのAI活用
- RAGの文書取込・検索・根拠表示
- ローカルLLM / OpenAI互換APIの接続
- Python / FastAPIのAPI・業務ツール
- Next.js / React / TypeScriptのWeb UI
- Cloudflare Workersへの公開
- 入力検証、エラー処理、秘密情報分離、簡易的なRate Limiting
- GitHub Issue / Pull Request / CIを使った変更管理

## 開発の進め方

要件と完了条件を先に整理し、変更範囲を小さく保ちながら進めます。

`要件整理 → 設計・計画 → Issue → 1 Issue / 1 PR → CI → レビュー → 修正 → マージ → 動作確認`

実装済みの機能・未実装の範囲・運用上の制約を分けて説明し、後から確認・修正できる履歴をGitHubに残します。

## 使用技術

- **AI / LLM:** 生成AI、RAG、ローカルLLM、OpenAI互換API、MCP
- **Web / API:** Python、FastAPI、TypeScript、Next.js、React
- **Platform:** Cloudflare Workers、Cloudflare Tunnel、Docker、Linux
- **Quality:** Git、GitHub Actions、pytest、型チェック

## ご相談について

「この業務をAIで効率化できるか整理したい」「社内文書を検索できるようにしたい」「小さな業務ツールをまず試したい」といったご相談に対応します。

ご相談の際は、対象業務・入力データ・期待する成果・希望納期をお知らせください。小さく検証できる範囲を整理し、実装・テスト・公開方法まで提案します。
