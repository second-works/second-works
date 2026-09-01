# SecondWorks

生成AI・ローカルLLM・RAGを活用した、小規模な業務支援ツールやWebアプリを制作しています。

本業では15年以上、施設管理に携わっています。設備管理で培った「問題を整理する」「安全性と優先順位を判断する」「運用まで考える」という視点を、ソフトウェア開発にも活かしています。

## What I build

- 生成AIを利用した業務効率化ツール
- RAG / 文書検索システム
- ローカルLLMを利用したアプリケーション
- Python / FastAPIによる小規模Web API・業務ツール
- Next.js / React / TypeScriptによるWebアプリ
- Cloudflareを利用したデプロイ・公開
- GitHub Issue / Pull Request / CIを利用した開発フロー

## Portfolio

### AI Business Assistant
業務文章の要約・文章改善・タスク抽出を行う生成AI Webアプリです。

- Next.js / React / TypeScript
- OpenAI互換 Chat Completions API
- Cloudflare Workers
- 入力検証、エラー処理、レスポンシブUI
- 秘密情報の分離、Rate Limiting

Repository: https://github.com/second-works/ai-business-assistant

### Local RAG Document Assistant
PDF/TXTの業務文書を検索し、文書名・ページ・根拠を示して回答するRAGシステムです。

- RAG / Vector Search
- PDF/TXT文書処理
- ローカルLLM / OpenAI互換API
- Cloudflare Workers / R2
- 回答不能処理によるハルシネーション抑制

Repository: https://github.com/second-works/local-rag-document-assistant

### System Monitor Dashboard
ローカルPCのCPU・メモリ・ディスク・OS・Uptimeをブラウザから確認するダッシュボードです。

- Python / FastAPI
- psutil
- HTML / CSS / JavaScript
- pytest
- GitHub Actions

Repository: https://github.com/second-works/system-monitor-dashboard

## Development style

実装速度だけでなく、後から確認・修正できる開発工程を重視しています。

`要件整理 → 設計・計画 → GitHub Issue → 1 Issue / 1 PR → CI → AIコードレビュー → 修正 → マージ → デプロイ`

AIにすべてを任せるのではなく、要件、変更範囲、テスト条件、完了条件を明確にし、GitHub上に判断と実装履歴を残すようにしています。

## Skills

**Languages / Frameworks**  
Python / FastAPI / TypeScript / JavaScript / Next.js / React

**AI / LLM**  
ChatGPT / Codex / RAG / Local LLM / OpenAI-compatible API / MCP

**Platform / Tools**  
Git / GitHub / GitHub Actions / Docker / Linux / Cloudflare

## Current focus

- 生成AIを利用した業務効率化
- ローカルLLMとクラウドサービスの安全な連携
- RAGによる業務文書検索
- AI支援開発フローの改善

---

クラウドワークス等で、AI活用・Python・RAG・業務効率化に関する小規模案件への対応を目指しています。
