<a id="top"></a>
<a id="zh"></a>

# Pinger v1.0.1beta

把 Android 手机变成一块「快捷键面板」：在 Photoshop、剪辑等软件里，用手机按键、旋钮代替键盘快捷键。
<img width="1760" height="812" alt="07" src="https://github.com/user-attachments/assets/391f8fb1-7794-4818-a74c-affa94693589" />

**语言** [中文](#zh) · [English](#en)

**下载** [官网](https://www.aitocg.cn/pinger) · [GitHub Releases](https://github.com/Miatoo/pinger/releases)

## 下载哪个文件

| 文件 | 装在哪 | 说明 |
| --- | --- | --- |
| **Pinger-v1.0.1beta.apk** | Android 手机 | 主程序（必装） |
| **PingerSettings-v1.0.1beta-windows-x64.zip** | Windows 电脑 | 改排版、快捷键同步；WiFi 模式时代按键（可选） |
| **SHA256SUMS.txt** | — | 安装包校验码（可选，核对下载是否完整） |

> **推荐组合**：只装手机 APK，用蓝牙连电脑。
>
> 蓝牙不好用时，再解压并打开电脑端 Pinger Settings，手机改用 WiFi。

## 先看：已知限制

| 现象 | 说明 | 处理 |
| --- | --- | --- |
| 部分国产手机注册 HID 失败 | 对「蓝牙 HID 键盘」支持不完整 | 改用 WiFi 模式 |
| 语音（MIC）不可用 | 蓝牙通道下的语音仍在完善 | 本版本请勿强依赖 MIC 键 |
| Windows 配对后显示「手机」 | 配对不等于连上键盘通道 | 回 App 内再点「连键盘」 |

## 安装

### 手机（Pinger）

1. 把 `Pinger-v1.0.1beta.apk` 传到手机并安装（需允许「未知来源」）。
2. 若之前装过旧版，可直接覆盖；若提示签名冲突，先卸载旧版再装。
3. 打开 App，允许**蓝牙**权限；建议**横屏**使用。

### 电脑（Pinger Settings，可选）

1. 解压 `PingerSettings-v1.0.1beta-windows-x64.zip`。
2. 运行文件夹内的 `PingerSettings.exe`（便携版，自带运行环境）。
3. 防火墙若询问，请允许局域网访问（同步与 WiFi 按键使用端口 **8766**）。

## 第一次使用（蓝牙，最常用）

1. 手机两指**右滑**，打开「状态」面板。
2. 选择宿主平台：**Win / Mac / iPad / 安卓**。
3. 点 **注册 HID** → **可被发现**。
4. 在电脑 / 平板蓝牙里搜索并配对（名字以状态页「宿主搜索名」为准）。
5. 回到手机 → **已配对主机** → **连键盘**。
6. 显示「键盘已连」后，打开记事本或 PS 试按。

> **连不上时**：删掉电脑上的旧蓝牙设备 → 手机重新「注册 HID」/「可被发现」 → 再配对 → 再「连键盘」。

## WiFi 模式（可选）

1. 手机与电脑连同一 WiFi。
2. 打开电脑端 **Pinger Settings**。
3. 手机状态面板切到 **WiFi**，填入电脑显示的本机 IP → 连接。
4. 按键经 `ws://电脑IP:8766` 由电脑端代发。

## 改排版 / 快捷键

1. 打开 **Pinger Settings**，记下顶部本机 IP。
2. 手机状态页填入该 IP（自动连同步）。
3. 电脑「同步」按方向操作：

| 操作 | 方向 |
| --- | --- |
| **发送到手机** | 电脑上的排版 + 快捷键 → 手机 |
| **从手机获取** | 手机当前配置 → 电脑 |

手机上也可直接进入布局编辑、快捷键编辑；快捷键页顶部有**按键对应图**（真实皮肤 + T1/E1 等序号），方便对照设置。

## 手势

| 手势 | 作用 |
| --- | --- |
| 两指右滑 | 状态（连接、IP、宿主） |
| 两指左滑 | 预设列表 |
| 两指上滑 | 编辑（皮肤、布局、关于） |
| 按住顶部 / 侧键，再拧旋钮或点其他键 | 组合层 |

## 校验码（SHA256）

完整列表见同目录 `SHA256SUMS.txt`。PowerShell 核对：

```powershell
Get-FileHash .\文件名 -Algorithm SHA256
```

**Pinger-v1.0.1beta.apk**

```
f12ffad0aed2d3e3e76ce1085c9fece9e7a5192fafe44f48c16f8f285ecafe66
```

**PingerSettings-v1.0.1beta-windows-x64.zip**

```
fa7f2ae8e383aa82e6d3e50bcc523fd172eb66200103d36c1dd8321f439746a5
```

## 链接

| 项目 | 地址 |
| --- | --- |
| 官网 | [www.aitocg.cn/pinger](https://www.aitocg.cn/pinger) |
| GitHub | [Miatoo/pinger](https://github.com/Miatoo/pinger) |
| 小红书 | 毛桃moatoa |
| 开源协议 | MIT |

[↑ 回到顶部](#top)

---

<a id="en"></a>

# English

[中文](#zh) · **English**

Turn an Android phone into a shortcut pad for Photoshop, editors, and similar apps.

**Download** [Website](https://www.aitocg.cn/pinger) · [GitHub Releases](https://github.com/Miatoo/pinger/releases)

## What to download

| File | Where | Purpose |
| --- | --- | --- |
| **Pinger-v1.0.1beta.apk** | Android phone | Main app (required) |
| **PingerSettings-v1.0.1beta-windows-x64.zip** | Windows PC | Edit layouts / shortcuts & sync; Wi-Fi key injection (optional) |
| **SHA256SUMS.txt** | — | Checksums (optional) |

> **Recommended**: phone APK + Bluetooth only. Install Pinger Settings only if Bluetooth HID fails, or you need Wi-Fi mode / desktop editing.

## Known limits

| Symptom | Cause | Fix |
| --- | --- | --- |
| HID registration fails on some phones | Incomplete Bluetooth HID support (common on some Chinese ROMs) | Switch to Wi-Fi mode |
| Voice (MIC) not working | Voice over the Bluetooth channel is still in progress | Do not rely on the MIC key in this build |
| Windows shows "phone" after pairing | Pairing is not the same as connecting the keyboard channel | Tap **Connect keyboard** in the app |

## Install

**Phone:** install `Pinger-v1.0.1beta.apk` (allow unknown sources). Grant Bluetooth access; landscape orientation is recommended.

**Windows (optional):** unzip `PingerSettings-v1.0.1beta-windows-x64.zip` and run `PingerSettings.exe` (portable, bundled runtime). Allow LAN access on port **8766** if prompted.

## First use (Bluetooth)

1. Two-finger **swipe right** → Status panel.
2. Pick the host platform: Win / Mac / iPad / Android.
3. **Register HID** → **Discoverable**.
4. Pair from the computer / tablet Bluetooth settings (use the name shown on the Status page).
5. On the phone: **paired host** → **Connect keyboard**.
6. Once it says connected, test in Notepad or Photoshop.

> **If it won't connect**: remove the old Bluetooth entry on the computer → register HID / make discoverable again → pair → **Connect keyboard** again.

## Wi-Fi mode (optional)

1. Phone and PC on the same Wi-Fi network.
2. Open **Pinger Settings** on the PC.
3. Phone Status → **Wi-Fi** → enter the PC IP → connect.
4. Keys are sent over `ws://PC-IP:8766` and injected by the desktop app.

## Layout & shortcuts

1. Open **Pinger Settings** and note the local IP shown at the top.
2. Enter that IP on the phone Status page (sync connects automatically).
3. Use Sync on the PC:

| Action | Direction |
| --- | --- |
| **Send to phone** | PC layout + shortcuts → phone |
| **Fetch from phone** | Current phone config → PC |

You can also edit layout and shortcuts directly on the phone. The shortcut page includes a **key map** (real skin with codes such as T1/E1) for reference.

## Gestures

| Gesture | Action |
| --- | --- |
| Two-finger swipe right | Status (connection, IP, host) |
| Two-finger swipe left | Presets |
| Two-finger swipe up | Edit (skin, layout, about) |
| Hold top / side key, then turn the knob or tap another key | Combo layer |

## SHA256

Full list in `SHA256SUMS.txt`. Verify on PowerShell:

```powershell
Get-FileHash .\filename -Algorithm SHA256
```

**Pinger-v1.0.1beta.apk**

```
f12ffad0aed2d3e3e76ce1085c9fece9e7a5192fafe44f48c16f8f285ecafe66
```

**PingerSettings-v1.0.1beta-windows-x64.zip**

```
fa7f2ae8e383aa82e6d3e50bcc523fd172eb66200103d36c1dd8321f439746a5
```

## Links

| Item | URL |
| --- | --- |
| Website | [www.aitocg.cn/pinger](https://www.aitocg.cn/pinger) |
| GitHub | [Miatoo/pinger](https://github.com/Miatoo/pinger) |
| License | MIT |

[↑ Back to top](#top)
