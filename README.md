# レポート課題：簡易版AAarch64エミュレータ

## 仕様

- 汎用レジスタはx0からx30のみ
- cmp命令では、等しい（equal）か、小なり（less than）の情報のみコンテキストに保持
  - src/eval.rsのContext::condの値が変化
- ブランチ命令は、b.eq（等しい場合にジャンプ）か、b.lt（小なりの場合にジャンプ）のみで、行志向
  - 0オリジン
  - 空行は1行として数えない
- 算術演算命令はadd、sub、mul、divのみ

## 修正履歴

- 2020年10月23日
  - 以下のissueを修正
    - https://github.com/ytakano-lecture/aa64emu/issues/1
    - https://github.com/ytakano-lecture/aa64emu/issues/2