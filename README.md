# Gadget Entangle for Plasticity (GEP)

Welcome to "Gadget Entangle for Plasticity" (GEP)! This tool provides ultra-low latency, real-time mesh synchronization directly between Plasticity and Unity Editor. 

## ⚠️ Important Notice

* **No Support (As-Is):** I am a solo developer working in the industrial engineering field. Therefore, providing individual technical support is practically impossible. This tool is provided "as-is" and completely free, without official support.
* **Plasticity License:** This tool utilizes Plasticity's native WebSocket server. Please ensure you have a valid Plasticity license that supports the Bridge/Server features.

## 🙏 Support the Project!

This tool is completely free to use. However, if you find it helpful for your workflow, I would greatly appreciate it if you could **Subscribe to my YouTube channel and Like the videos!** Your support is my greatest motivation to continue developing tools like this! 
▶️ https://www.youtube.com/channel/UCj9OYwzMAIgYAeVkTV4wczw

**Windows Only:** This tool currently only supports Windows environments. macOS and Linux are not supported.

---

## 🚀 Installation Guide

### 1. Plasticity Setup
1. Open Plasticity.
2. Ensure the built-in server is running (Usually accessible via Preferences, default port is `8980`).

### 2. Unity Setup
1. Create a **New Project** in Unity (Recommended version: Unity 6 / URP).
2. Download the `GEP_v1.0.0.unitypackage` from this repository.
3. Import the package into your Unity project (`Assets > Import Package > Custom Package...`).

---

## How to use and main features

1. **Launch Dashboard:** From the top menu, click `Gadget > Gadget Entangle`.
2. **Connect:** Ensure the Server Address is `localhost:8980` and click the **Connect** button.
3. **Entangle (Subscribe):** Keep this toggled ON to enable real-time mesh updates as you model in Plasticity.
4. **📂 Target Work Area (Sandbox):** Drag and drop an empty GameObject (Folder) from your Hierarchy here. GEP will exclusively sync objects within this folder, preventing your other scene objects from being accidentally modified.※Completely preventing this may be a mistake; it is recommended to duplicate the modeled object in the Unity hierarchy (this will break the Plasticity object ID).
5. **Generate ID Map:** Instantly assigns random colored materials to each part based on its Plasticity ID for easy material separation.
6. **🛠️ Ultimate Weld (For Sculpting):**
   * Select your synced meshes and click `Execute Ultimate Weld` to close gaps and merge overlapping vertices.
   * **Force Topology Merge:** Turn this ON if you plan to export the mesh to ZBrush or 3DCoat. It completely merges the topology (ignoring CAD hard edges) to prevent mesh tearing during voxelization or subdivision.

---

## ⚖️ License
This software is provided under a proprietary license. Unauthorized redistribution, modification, and reverse engineering (decompiling) are strictly prohibited. 
For full details, please read the [LICENSE](./LICENSE) file.

===========================================================================

# Gadget Entangle for Plasticity (日本語版)

「Gadget Entangle for Plasticity (GEP)」へようこそ！このツールは、PlasticityとUnityエディタを直接繋ぎ、超低遅延のリアルタイムメッシュ同期を実現します。

## ⚠️ 重要な注意事項（必ずお読みください）

* **サポートなし（現状渡し）:** 開発者は普段、FA・産業機械系の本業を抱える個人エンジニアです。そのため、個別の環境に合わせた技術サポートを提供することは事実上不可能です。本ツールは「完全無料・サポート対象外」として提供されます。
* **Plasticityライセンス:** 本ツールはPlasticity内蔵のWebSocketサーバー機能を使用します。Bridge/サーバー機能が利用可能な有効なPlasticityライセンスをご用意ください。

## 🙏 開発者からのお願い

本ツールは完全無料でお使いいただけます。もし皆様の制作のお役に立てましたら、ぜひ**YouTubeチャンネルの登録と高評価**をお願いいたします！ 皆様からの応援が、今後の開発の最大のモチベーションになります！ 
▶️ https://www.youtube.com/channel/UCj9OYwzMAIgYAeVkTV4wczw

**Windows専用:** 本ツールは現在、Windows環境でのみ動作します。macOSやLinuxには対応しておりません。

---

## 🚀 導入手順

### 1. Plasticity側の準備
1. Plasticityを起動します。
2. Preferences（設定）等から、内部サーバーが起動していることを確認してください（デフォルトポート: `8980`）。

### 2. Unity側の準備
1. Unityで**空の新規プロジェクト**を作成します（推奨：Unity 6 / URP環境）。
2. このリポジトリから `GEP_v1.0.0.unitypackage` をダウンロードします。
3. Unityプロジェクトにインポートします（`Assets > Import Package > Custom Package...`）。

---

## 🎮 使い方と主要機能

1. **ダッシュボード起動:** Unity上部メニューから `Gadget > Gadget Entangle` をクリックします。
2. **接続:** Server Addressが `localhost:8980` になっていることを確認し、**Connect** ボタンを押します。
3. **Entangle (Subscribe):** これをONにしておくと、Plasticityでのモデリング結果がリアルタイムに反映されます。
4. **📂 Target Work Area (サンドボックス機能):** ヒエラルキー上の空オブジェクト（フォルダ）をここにドラッグ＆ドロップすると、そのフォルダ内だけで同期が行われます。他のモデルを巻き込む事故を完全に防ぎます。※完全に防ぐは誤りの可能性あり、モデリングが完了したオブジェクトはUnityのヒエラルキーで複製(これによりPlasticityのオブジェクトIDを断ち切る事ができます)を取ることを推奨します。
5. **Generate ID Map:** PlasticityのIDを元に、パーツごとにランダムなカラーマテリアルを自動生成・割り当てします。
6. **🛠️ Ultimate Weld（スカルプト向け頂点結合）:**
   * 同期したメッシュを選択して `Execute Ultimate Weld` を押すと、パーツ間の隙間を埋めて頂点を結合します（Ctrl+ZでUndo可能）。
   * **Force Topology Merge:** ZBrushや3DCoatへ持っていく場合はONにしてください。CAD特有のハードエッジ（法線）を無視してトポロジーを完全結合し、ボクセル化やサブディビジョン時のメッシュの破綻を防ぎます。

---

## ⚖️ License
本ソフトウェアは独自ライセンスのもとで提供されています。無断再配布、改変、および逆コンパイル（リバースエンジニアリング）は固く禁じられています。
詳細については、[LICENSE](./LICENSE) ファイルをご確認ください。
