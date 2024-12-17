[日本語](./new_team_ja.md) | [English](./new_team_en.md)

RoboCup@Homeシミュレーションの基本構成は、SIGVerseを実行するためのWindowsコンピュータと、参加者が作成したROSノードを実行するためのUbuntuコンピュータが必要です。これら2台のコンピュータはスイッチングハブに接続する必要があります。 

SIGVerseについてはhttp://www.sigverse.orgを確認してください。

# 環境構築

### Windows PC

大会主催者は、競技用プログラムを実行するためのWindowsコンピュータを準備します．

| No | 項目       |  詳細   |
|:--:| ---------- |----------------|
| 1  | OS         | Windows 10     |
| 2  | Unity      | [Unity 2021.3.3f1][download unity] |
| 3  | IPアドレス | 192.168.0.1    |
| 4  | Note       | Unityのシステム要件を以下に示します．<br>https://docs.unity3d.com/Manual/system-requirements.html<br> Oculus Quest 2のシステム要件は以下の通りです。<br>https://store.facebook.com/en-us/help/quest/articles/headsets-and-accessories/oculus-link/ |

### Ubuntu PC

参加者はUbuntuコンピュータを準備する必要があります。参加者は、作成したROSノードを動作させるために、ロボットオペレーティングシステム（ROS）をインストールする必要があります。 
(Ubuntuコンピュータを準備できない場合は、OCに連絡すること）

| No | 項目       | 詳細    |
|:--:| ---------- |----------------|
| 1  | OS         | Ubuntu 20.04    |
| 2  | ROS ver| [Noetic Ninjemys][ros installation] |
| 3  | IP Address | 192.168.0.2    |
| 4  | Note       | 競技中の無線通信は禁止されています。 |

### Switching Hub

参加者は、接続速度1Gbpsの1000BASE-Tスイッチングハブを使用すること。

### Oculus Quest 2

参加者は競技課題に応じてOculus Quest 2を使用すること。

[download unity]:https://unity3d.com/get-unity/download/archive "download"
[ros installation]:http://wiki.ros.org/noetic/Installation/Ubuntu "installation"

----------------------------------
# ソフトウェア

### Unity

Unityはゲーム開発プラットフォームです。
https://unity3d.com/

WindowsにUnityをインストールしてください。
[download Unity][download unity]

### ROS

ROS（Robot Operating System）は、オープンソースのロボット用メタオペレーティングシステムです。 
http://wiki.ros.org/

UbuntuにROSをインストールしてください。 
[install ROS][ros installation]

### Oculusソフトウェア

Oculus Quest 2を使用するには、Oculus SoftwareとSteamVRをインストールする必要があります。

[download Oculus Software (OculusSetup.exe)](https://store.facebook.com/quest/setup/)  
[download Steam](https://store.steampowered.com/about/)  
[download SteamVR](https://store.steampowered.com/app/250820/SteamVR/)  

----------------------------------
# 準備


## 競技用ソフトウェアの概要

### Handyman

以下をご覧ください。

https://github.com/RoboCupatHomeSim/handyman-unity/wiki/SystemOverview

### Interactive Cleanup

以下をご覧ください。

https://github.com/RoboCupatHomeSim/interactive-cleanup-unity/wiki/SystemOverview

### Human Navigation

以下をご覧ください。

https://github.com/RoboCupatHomeSim/human-navigation-unity/wiki/SystemOverview

# 競技用ソフトウェアの実行

サンプルプログラムの実行手順は以下に記述されています。
詳細はリポジトリのreadmeやwikiを参照してください。

## Handyman
- Ubuntu(ROS)側  
https://github.com/RoboCupatHomeSim/handyman-ros
- Windows(Unity)側  
https://github.com/RoboCupatHomeSim/handyman-unity

## Interactive Cleanup
- Ubuntu(ROS)側  
https://github.com/RoboCupatHomeSim/interactive-cleanup-ros
- Windows(Unity)側  
https://github.com/RoboCupatHomeSim/interactive-cleanup-unity

## Human Navigation
- Ubuntu(ROS)側  
https://github.com/RoboCupatHomeSim/human-navigation-ros
- Windows(Unity)側  
https://github.com/RoboCupatHomeSim/human-navigation-unity