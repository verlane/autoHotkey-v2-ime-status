# Summary

IME.ahk ( eamat http://www6.atwiki.jp/eamat/ ) for AutoHotkey V2

For Windows 11 old Microsoft IME

You can get the IME status for Japanese and Korean keyboard input.

일본어 및 한국어 키보드 입력에 대한 IME 상태를 확인할 수 있습니다.

日本語と韓国語のキーボード入力のIMEステータスを確認できます。

# Code

```AutoHotkey

#Include IME.ahk

if (IME_GET() = 1 && (IME_GetConvMode() = 0 || IME_GetConvMode() = 1)) {
  ; Korean
} else if (IME_GET() = 1 && (IME_GetConvMode() = 25 || IME_GetConvMode() = 9)) {
  ; Japanese
} else if (IME_GetConvMode() = 0) {
  ; English on Korean
} else {
  ; English on Japanese
}

if (IME_GetSentenceMode() = 0) {
  ; Not input mode
}
```
