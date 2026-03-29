[![](https://github.com/user-attachments/assets/a1a6df48-7925-43c9-81d6-e2351e6c6bb8)](https://blueprint.zip/guides/admin/install)

## 簡介
**Blueprint** 是 Pterodactyl 的開源擴充框架/管理器。開發者可以建立多用途、易於安裝的擴充套件，系統管理員可在數分鐘內（*通常甚至只要幾秒！*）完成安裝，而不必為了多種面板修改（mod）去客製化撰寫彼此相容的程式碼。

我們希望透過淺顯易懂的指南、文件、開發者指令、社群支援等方式，讓更多新開發者能更容易上手 Blueprint。

[了解更多 **Blueprint**](https://blueprint.zip) 或 [尋找你的 **下一個擴充套件**](https://blueprint.zip/browse).

### Install Blueprint
Refer to the [installation guide](https://blueprint.zip/guides/admin/install).

<br>

## 捐款與貢獻
Blueprint 是免費且開源的軟體。我們在 Pterodactyl 模組化社群中扮演重要角色，並提供工具協助開發者把想法化為現實。為了維持所有服務正常運作，我們非常依賴 [捐款](https://hcb.hackclub.com/blueprint/donations)。我們同時也是非營利組織！

如果您是企業組織，[歡迎考慮成為我們的企業贊助夥伴](https://hcb.hackclub.com/donations/start/blueprint/tiers/392)。Blueprint 提供豐富的指南與文件資源，協助更多新進開發者踏入主機託管產業，也為企業開啟接觸新人才、進一步推動營運成長的機會。

[**捐款給我們的非營利組織**](https://hcb.hackclub.com/donations/start/blueprint) or [查看我們的公開財務](https://hcb.hackclub.com/blueprint).

### 貢獻者
貢獻者正在共同塑造 Blueprint 模組化框架的未來。要開始貢獻，你需要先 [fork 此儲存庫](https://github.com/BlueprintFramework/framework/fork) 然後 [開啟一個 pull request](https://github.com/BlueprintFramework/framework/compare).

<a href="https://github.com/BlueprintFramework/framework/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=BlueprintFramework/framework" />
</a>

### 相關的儲存庫
Blueprint 模組開發平台分散在多個儲存庫中，每個儲存庫都有各自的用途。如果你想參與貢獻，請查看以下的儲存庫:

- [**BlueprintFramework/docker**](https://github.com/BlueprintFramework/docker) 是用於以 Docker 執行 Blueprint 與 Pterodactyl 的映像檔。 [[**繁體中文版**](https://github.com/Lingyu-ILY/blueprint-docker-tc)]\
- [**BlueprintFramework/templates**](https://github.com/BlueprintFramework/templates) 是提供擴充套件開發初始化模板的儲存庫。
- [**BlueprintFramework/web**](https://github.com/BlueprintFramework/web) 是我們開源的文件，形象網站以及API。

<br>

## 這裡有哪些內容？
Framework 儲存庫內含可套用至 Pterodactyl Panel 的 Blueprint Patch。它的安裝方式和「獨立附加元件」一樣，會直接覆寫既有檔案，但 Blueprint 不只是單一附加元件，而是讓你的 Panel 能夠透過「Extensions」進一步擴充功能的延伸框架。

- Blueprint 的 CLI 採用 Bash 開發。
- 後端基於 Pterodactyl 架構延伸，使用 PHP/Laravel 建構。
- 使用者端前端延續 Pterodactyl 的架構設計，並以 React/TypeScript 開發。
- 管理端前端同樣建構於 Pterodactyl 架構之上，採用 PHP/Laravel/Blade 打造。

### CLI
我們的主要 CLI 腳本為 [`blueprint.sh`](./blueprint.sh)。當使用者執行 `blueprint` 指令，或觸發 Bash 自動補全查詢時，`/usr/local/bin/blueprint` 便會呼叫此腳本。

[`blueprint.sh`](./blueprint.sh) 負責以下核心工作：
- 完成初始安裝與更新流程中的必要步驟，例如清除快取、執行 Artisan 指令等。
- 載入 CLI 所需的相依腳本([`scripts/libraries`](./scripts/libraries))。
- 依據不同指令呼叫對應的子腳本 ([`scripts/commands`](./scripts/commands))。
- 將 Blueprint 指令捷徑建立至 `/usr/local/bin/blueprint`。

我們過去曾將幾乎*所有功能*都集中在主要 CLI 腳本中，導致整體架構變得*相當複雜*。現在，大多數功能都已劃分到各自對應的模組與區域中，讓整體結構更清晰，也更容易維護。

<br>

## 展示
我們擁有一個持續成長中的擴充生態系，涵蓋了像 Minecraft、Hytale 這類遊戲功能擴充，也包含各種實用、能提升管理體驗的管理工具。

![](https://github.com/user-attachments/assets/1cea099b-9af8-4ccc-ac1a-0a896a30f817)

<br/><br/>
<p align="center">
  © 2023-2026 Emma (prpl.wtf)
  <br/><br/><img src="https://github.com/user-attachments/assets/e6ff62c3-6d99-4e43-850d-62150706e5dd"/>
</p>
