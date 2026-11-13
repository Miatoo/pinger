# Pinger v1.0.1beta

**语言 / Language：** [中文](#pinger-v101beta) · [English](#english)

把 Android 手机变成一块「快捷键面板」：在 Photoshop、剪辑等软件里，用手机按键、旋钮代替键盘快捷键。

下载与更新：[www.aitocg.cn/pinger](https://www.aitocg.cn/pinger) · [GitHub Releases](https://github.com/Miatoo/pinger/releases)

---

## 下载哪个文件

| 文件 | 装在哪 | 说明 |
|--|--|--|
| **Pinger-v1.0.1beta.apk** | Android 手机 | 主程序（必装） |
| **PingerSettings-v1.0.1beta-windows-x64.zip** | Windows 电脑 | 改排版 / 快捷键同步；WiFi 模式时代按键（可选） |
| **SHA256SUMS.txt** | — | 安装包校验码（可选，用于核对下载是否完整） |

> 日常推荐：**只装手机 APK + 蓝牙连电脑**。  
> 蓝牙不好用时，再解压并打开电脑端 Pinger Settings，手机改用 WiFi。

---

## 安装

### 手机（Pinger）

1. 把 `Pinger-v1.0.1beta.apk` 传到手机并安装（需允许「未知来源」）。  
2. 若之前装过旧版，可直接覆盖；若提示签名冲突，先卸载旧版再装。  
3. 打开 App，允许**蓝牙**权限；建议**横屏**使用。

### 电脑（Pinger Settings，可选）

1. 解压 `PingerSettings-v1.0.1beta-windows-x64.zip`。  
2. 运行文件夹内的 `PingerSettings.exe`（便携版，自带运行环境）。  
3. 防火墙若询问，请允许局域网访问（同步与 WiFi 按键使用端口 **8766**）。

---

## 第一次使用（蓝牙，最常用）

1. 手机两指**右滑**打开「状态」面板。  
2. 选择宿主平台：**Win / Mac / iPad / 安卓**。  
3. 点 **注册 HID** → **可被发现**。  
4. 在电脑 / 平板蓝牙里搜索并配对（名字以状态页「宿主搜索名」为准）。  
5. 回到手机 → **已配对主机** → **连键盘**。  
6. 显示「键盘已连」后，打开记事本或 PS 试按。

**连不上时：** 删掉电脑上的旧蓝牙设备 → 手机重新注册 / 可被发现 → 再配对 → 再「连键盘」。

---

## WiFi 模式（可选）

1. 手机与电脑连同一 WiFi。  
2. 打开电脑端 **Pinger Settings**。  
3. 手机状态面板切到 **WiFi**，填入电脑显示的本机 IP → 连接。  
4. 按键经 `ws://电脑IP:8766` 由电脑端代发。

---

## 改排版 / 快捷键

1. 打开 **Pinger Settings**，记下顶部本机 IP。  
2. 手机状态页填入该 IP（自动连同步）。  
3. 电脑「同步」：  
   - **发送到手机**：把电脑上的排版 + 快捷键发到手机  
   - **从手机获取**：把手机当前配置读回电脑  

手机上也可直接进入布局编辑、快捷键编辑；快捷键页顶部有**按键对应图**（真实皮肤 + T1/E1 等序号），方便对照设置。

---

## 手势

| 手势 | 作用 |
|--|--|
| 两指右滑 | 状态（连接、IP、宿主） |
| 两指左滑 | 预设列表 |
| 两指上滑 | 编辑（皮肤、布局、关于） |
| 按住顶部 / 侧键，再拧旋钮或点其他键 | 组合层 |

---

## 校验码（SHA256）

完整列表见同目录 `SHA256SUMS.txt`。主安装包：

```
Pinger-v1.0.1beta.apk
f12ffad0aed2d3e3e76ce1085c9fece9e7a5192fafe44f48c16f8f285ecafe66

PingerSettings-v1.0.1beta-windows-x64.zip
fa7f2ae8e383aa82e6d3e50bcc523fd172eb66200103d36c1dd8321f439746a5
```

PowerShell 核对：`Get-FileHash .\文件名 -Algorithm SHA256`

---

## 已知说明

- 部分国产手机对「蓝牙 HID 键盘」支持不完整，可改用 WiFi 模式。  
- 蓝牙通道下的语音（MIC）仍在完善，本版本请勿强依赖。  
- Windows 蓝牙配对后可能仍显示「手机」，需在 App 内再点「连键盘」。

---

## 链接

- 官网：[www.aitocg.cn/pinger](https://www.aitocg.cn/pinger)  
- GitHub：[Miatoo/pinger](https://github.com/Miatoo/pinger)  
- 小红书：毛桃moatoa  
- 协议：MIT

---

# English

<a id="english"></a>

## Pinger v1.0.1beta (English)

Turn an Android phone into a shortcut pad for Photoshop, editors, and similar apps.

[↑ Back to top / 返回顶部](#pinger-v101beta)

Site: [www.aitocg.cn/pinger](https://www.aitocg.cn/pinger) · [GitHub Releases](https://github.com/Miatoo/pinger/releases)

## What to download

| File | Where | Purpose |
|--|--|--|
| **Pinger-v1.0.1beta.apk** | Android phone | Main app (required) |
| **PingerSettings-v1.0.1beta-windows-x64.zip** | Windows PC | Edit layouts/shortcuts & sync; Wi‑Fi key injection (optional) |
| **SHA256SUMS.txt** | — | Checksums (optional) |

Recommended: **phone APK + Bluetooth**. Install Pinger Settings only if Bluetooth HID fails or you need Wi‑Fi / desktop editing.

## Install

**Phone:** install `Pinger-v1.0.1beta.apk` (allow unknown sources). Grant Bluetooth; landscape is recommended.

**Windows (optional):** unzip `PingerSettings-v1.0.1beta-windows-x64.zip` and run `PingerSettings.exe`. Allow LAN access on port **8766** if prompted.

## First use (Bluetooth)

1. Two-finger **swipe right** → Status.  
2. Pick host platform: Win / Mac / iPad / Android.  
3. **Register HID** → **Discoverable**.  
4. Pair from the computer/tablet Bluetooth settings (use the name shown on Status).  
5. On the phone: paired host → **Connect keyboard**.  
6. When it says connected, test in Notepad or Photoshop.

## Wi‑Fi mode (optional)

Same Wi‑Fi → open Pinger Settings on PC → phone Status → Wi‑Fi → enter PC IP → connect (`ws://PC-IP:8766`).

## Layout & shortcuts

Open Pinger Settings, note the PC IP, enter it on the phone Status page, then use Sync (**Send to phone** / **Fetch from phone**). The phone shortcut editor includes a **key map** (real skin + codes such as T1/E1).

## Gestures

| Gesture | Action |
|--|--|
| Two-finger swipe right | Status |
| Two-finger swipe left | Presets |
| Two-finger swipe up | Edit (skin, layout, about) |
| Hold top/side key + another control | Combo layer |

## SHA256

See `SHA256SUMS.txt`. Main packages:

```
Pinger-v1.0.1beta.apk
f12ffad0aed2d3e3e76ce1085c9fece9e7a5192fafe44f48c16f8f285ecafe66

PingerSettings-v1.0.1beta-windows-x64.zip
fa7f2ae8e383aa82e6d3e50bcc523fd172eb66200103d36c1dd8321f439746a5
```

## Notes

- Some Android phones have incomplete Bluetooth HID support — use Wi‑Fi mode.  
- Voice (MIC) over Bluetooth is still incomplete in this build.  
- On Windows, pairing alone is not enough; tap **Connect keyboard** in the app.

## Links

- [www.aitocg.cn/pinger](https://www.aitocg.cn/pinger) · [GitHub](https://github.com/Miatoo/pinger) · MIT License
