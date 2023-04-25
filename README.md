# protorepo

- Change into a service specific directory
- Read every language the .protolangs file declares
- Take the proto files and move and outputted them into the language specific repository
- Do a simple git diff to see if anything changed
- If the project did change, commit the changes, and push
- Rinse and repeat for every folder

```
├── .github                  --> GithubCI用の設定
├── .ci                      --> CI用の設定
│   ├── run.sh
├── Makefile
├── README.md
└── monorepo                   --> .protoファイルの保存フォルダ
    ├── test                   --> testという名のプロジェクト
    │   ├── .protolangs        --> コード生成対象の言語リスト
    │   └── test.proto
    └── buf.yaml               --> lintingルール
```
