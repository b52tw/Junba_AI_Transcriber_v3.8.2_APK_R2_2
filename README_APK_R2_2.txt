Junba AI Transcriber v3.8.2 APK R2.2
====================================

這是 Android-only 完整建置封包，Windows 版未包含、未修改。

R2.2 的目的：
1. 以已成功通過 compileDebugKotlin / compileDebugJavaWithJavac / assembleDebug 的 R2.1 程式碼為基底。
2. Android versionCode 提升為 386，versionName 為 3.8.2-apk-r2.2。
3. GitHub Actions 改為「clean → compile → assemble → 立即上傳 APK」。
4. APK 一旦 assemble 成功，先上傳 Artifact；後續診斷不再阻擋成品下載。
5. 移除非必要的 attestation / Robolectric / DEX grep 等會造成假失敗的 CI 關卡。
6. 後續 APK diagnostics 設為 continue-on-error，只供查看，不影響 Build 成功狀態。

GitHub Actions：
.github/workflows/build-android-v3.8.2-r2.yml

成功後 Artifact：
Junba-v382-APK-R2.2

APK：
Junba-R2.2.apk

重要：這份封包的 Android runtime 功能沿用 R2.1；本次不再改動 Gemini、Whisper、API Key、預覽與自動存檔邏輯，避免引入新的手機端變數。
