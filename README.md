<a id="top"></a>
<img width="1084" height="626" alt="image" src="https://github.com/user-attachments/assets/0819e937-07b3-426e-99dc-c3208efaef65" />

<a id="zh"></a>

# Pinger · v1.0.4beta

把 Android 手机变成一块「快捷键面板」：在 Photoshop、剪辑软件里，用手机按键、旋钮代替键盘快捷键。

**语言** [中文](#zh) · [English](#en)

下载与更新：[www.aitocg.cn/pinger](https://www.aitocg.cn/pinger)  
安装包也可在 GitHub [Releases](https://github.com/Miatoo/pinger/releases) 下载。

## 本版要点

- 修复 release 包 Wi‑Fi 明文被系统拦截（CLEARTEXT not permitted），局域网 `ws://` 可连
- HID 注册增加 10 秒超时；不支持 HID Device 的机型会提示改用 Wi‑Fi 模式
- Windows 端：解压 zip 后双击 **PingerSettings.exe**（自带运行库，会请求管理员权限）

---

## 你需要下载什么

| 软件 | 装在哪 | 干什么 |
|--|--|--|
| **Pinger**（`Pinger-v1.0.4beta.apk`） | Android 手机 | 主界面，真正操作按键 |
| **Pinger Settings**（`PingerSettings-Windows-portable-v1.0.4beta.zip`） | Windows 电脑 | ① 改排版 / 快捷键并同步<br>② WiFi 模式时代为按键 |

日常最常用：**只装手机 Pinger + 蓝牙连电脑**，不必装电脑端。  
蓝牙不好用时：解压 Settings zip → 双击 **PingerSettings.exe** → 手机切 WiFi。

---

## 本软件用到哪些系统能力（请知晓）

| 场景 | 实际调用 / 通道 | 白话解释 |
|--|--|--|
| 蓝牙模式（推荐入门） | Android **蓝牙 HID 键盘**（`BluetoothHidDevice`） | 手机对电脑来说就像一块无线键盘 |
| WiFi 模式 | 手机连 **`ws://电脑IP:8766`** → **Pinger Settings** | 按键与同步共用同一端口；电脑端在前台软件里代按 |
| 改排版 / 改快捷键同步 | 同上 **`ws://电脑IP:8766`** → **Pinger Settings** | 传布局和预设；与 WiFi 按键同一连接入口 |
| 语音（MIC） | 系统语音识别 | **蓝牙端仍在构建，暂时不能用**；WiFi 模式后续可用 |
| 宿主类型 | App 内选 **Win / Mac / iPad / 安卓** | Mac、iPad 会把快捷键里的 Ctrl 自动改成 Cmd |

> **注意：** 蓝牙模式依赖手机是否完整支持「蓝牙 HID」。部分国产手机可能注册失败，可改用 WiFi 模式（需打开电脑端 Pinger Settings）。  
> **已知限制：** 蓝牙通道下的语音识别功能还在开发中，本版本请勿依赖 MIC 键。

---

## 第一次使用：蓝牙连电脑（最常用）

适合：Windows / Mac / iPad / 安卓平板，不想在电脑上再装东西。

### 手机上

1. 安装并打开 **Pinger**，按提示允许**蓝牙**权限。  
2. 手机**横屏**使用。  
3. **两指从右往左滑**，打开「状态」面板。（两指左滑是预设，两指上滑是编辑。）  
4. 在「宿主平台」里选对：**Win / Mac / iPad / 安卓**。  
5. 点 **注册 HID**（把手机注册成蓝牙键盘）。  
6. 看清面板上的 **宿主搜索名**（多数是手机蓝牙名，不一定叫 Pinger）。  
7. 点 **可被发现**，允许系统弹窗。

### 电脑 / 平板上

1. 打开系统蓝牙，搜索并配对上面那个**搜索名**。  
   - **Windows：** 设置 → 蓝牙 → 添加设备  
   - **Mac：** 系统设置 → 蓝牙  
   - **iPad / 安卓平板：** 系统蓝牙列表里选同一名字  
2. **Windows 特别说明：** 配对后可能仍显示「手机 / 个人区域网」，正常——还没连上「键盘通道」。  
3. 回到手机状态面板 → **已配对主机** → 找到你的电脑 → 点 **连键盘**。  
4. 手机显示「键盘已连」后，打开记事本或 PS 试按。  
5. 若宿主是 **Mac / iPad**，确认状态页已选对应平台，否则 Ctrl/Cmd 会对不上。

### 连不上时

- 在电脑蓝牙里删掉旧设备，手机重新「注册 HID」→「可被发现」→ 再配对 → 再「连键盘」。  
- 搜不到「Pinger」：搜状态面板里写的名字；也可在系统蓝牙设置把手机改名为 `Pinger`。

---

## 可选：WiFi 模式（用电脑端代按键）

适合：蓝牙 HID 不可用，或你更习惯局域网。

1. 电脑与手机连**同一个 WiFi**。  
2. 打开 **Pinger Settings**（自动监听 **8766**：同步 + WiFi 按键）。  
3. 手机状态面板把通道切到 **WiFi**，填入电脑顶部显示的 **本机 IP**。  
4. 点「连接电脑（WiFi）」；手机按键经 **`ws://电脑IP:8766`** 发到电脑端代按。

> 蓝牙模式**不需要**开电脑端。  
> WiFi 模式**只要打开 Pinger Settings** 即可。电脑若显示「手机已连接」而手机仍失败，请确认手机与电脑用的是同一 IP，并重装最新手机 APK。

---

## 可选：用电脑改排版和快捷键

1. 打开 **Pinger Settings**（同步服务端口 **8766** 也会自动开）。  
2. 记下软件顶部的**本机 IP**。  
3. 手机状态面板填入这个 IP（会自动连同步）。  
4. 电脑「同步」页：  
   - **发送到手机**：把电脑上的排版 + 快捷键发到手机  
   - **从手机获取**：把手机当前界面和快捷键读回电脑  

> 同步与 WiFi 按键都走 **8766**，同一套 Pinger Settings。

---

## 面板怎么滑、怎么按

| 手势 / 操作 | 作用 |
|--|--|
| 两指右滑 | 打开状态（连接、IP、宿主） |
| 两指左滑 | 打开预设列表 |
| 两指上滑 | 打开编辑（皮肤、布局、关于） |
| 按住顶部 / 侧键不放，再拧旋钮或点别的键 | 组合键（类似实体 Pinger） |

---

## 作者与协议

- 工具网址：[www.aitocg.cn/pinger](https://www.aitocg.cn/pinger)  
- GitHub：[Miatoo/pinger](https://github.com/Miatoo/pinger)  
- 作者小红书：毛桃moatoa  
- 开源协议：[MIT License](LICENSE)

[↑ 回到顶部](#top)

---

<a id="en"></a>

# English

[中文](#zh) · **English**

Turn an Android phone into a shortcut pad: use keys and knobs instead of keyboard shortcuts in Photoshop, editors, and similar apps.

**Download** [Website](https://www.aitocg.cn/pinger) · [GitHub Releases](https://github.com/Miatoo/pinger/releases)

## Highlights

- Fix: release builds blocked LAN cleartext (`ws://`) — Wi‑Fi mode works on Android 9+
- HID register now times out after 10s and suggests switching to Wi‑Fi on unsupported ROMs

---

## What to download

| App | Where | Purpose |
|--|--|--|
| **Pinger** (phone APK) | Android phone | Main UI — the keys you press |
| **Pinger Settings** (Windows portable, optional) | Windows PC | ① Edit layout / shortcuts and sync to the phone<br>② Inject keys when the phone uses **Wi‑Fi mode** |

Most users only need **phone Pinger + Bluetooth**.  
If Bluetooth HID fails, install **Pinger Settings** and switch the phone to Wi‑Fi (no other companion app required).

---

## System capabilities used

| Scenario | Channel | Plain English |
|--|--|--|
| Bluetooth (recommended) | Android **Bluetooth HID keyboard** (`BluetoothHidDevice`) | The phone appears as a wireless keyboard |
| Wi‑Fi mode | Phone → **`ws://PC-IP:8766`** → **Pinger Settings** | Keys and sync share the same port; the PC injects keystrokes |
| Layout / shortcut sync | Same **`ws://PC-IP:8766`** → **Pinger Settings** | Push / pull layouts and presets |
| Voice (MIC) | System speech recognition | **Not ready on Bluetooth yet**; Wi‑Fi path comes later |
| Host type | In-app: **Win / Mac / iPad / Android** | Mac / iPad map Ctrl → Cmd in shortcuts |

> **Note:** Bluetooth needs full HID keyboard support. Some phones fail to register — use Wi‑Fi mode with Pinger Settings.  
> **Known limit:** Do not rely on the MIC key in this beta.

---

## First use: Bluetooth (most common)

For Windows / Mac / iPad / Android tablets — no desktop app required.

### On the phone

1. Install **Pinger** and allow **Bluetooth**.  
2. Use **landscape**.  
3. **Two-finger swipe right → left** opens Status. (Swipe left = presets; swipe up = edit.)  
4. Set host: **Win / Mac / iPad / Android**.  
5. Tap **Register HID**.  
6. Note the **discoverable name** (often the phone Bluetooth name, not always “Pinger”).  
7. Tap **Discoverable** and accept the system prompt.

### On the computer / tablet

1. Pair that **discoverable name** in system Bluetooth.  
   - **Windows:** Settings → Bluetooth → Add device  
   - **Mac:** System Settings → Bluetooth  
   - **iPad / Android tablet:** pick the same name  
2. **Windows:** after pairing it may still say “phone / PAN” — normal; the keyboard channel is not connected yet.  
3. Back on the phone → **Paired hosts** → your PC → **Connect keyboard**.  
4. When it says keyboard connected, test in Notepad or Photoshop.  
5. For **Mac / iPad**, confirm the host type on the Status page so Ctrl/Cmd match.

### If it won’t connect

- Remove the old Bluetooth device on the PC, then phone: **Register HID** → **Discoverable** → pair → **Connect keyboard** again.  
- Can’t find “Pinger”: search the name shown on Status, or rename the phone to `Pinger` in system Bluetooth settings.

---

## Optional: Wi‑Fi mode

When Bluetooth HID is unavailable, or you prefer LAN.

1. Phone and PC on the **same Wi‑Fi**.  
2. Open **Pinger Settings** (listens on **8766**: sync + Wi‑Fi keys).  
3. On the phone Status panel, switch to **Wi‑Fi** and enter the PC IP shown at the top.  
4. Tap **Connect (Wi‑Fi)**; keys go via **`ws://PC-IP:8766`**.

> Bluetooth does **not** need the desktop app.  
> Wi‑Fi only needs **Pinger Settings**. If the PC shows “phone connected” but the phone fails, confirm the same IP and reinstall the latest APK.

---

## Optional: edit layout & shortcuts on PC

1. Open **Pinger Settings** (sync on **8766** starts automatically).  
2. Note the **local IP** at the top.  
3. Enter that IP on the phone Status panel (sync connects automatically).  
4. On the PC Sync page:  
   - **Send to phone** — push layout + shortcuts to the phone  
   - **Get from phone** — pull the phone’s current setup  

> Sync and Wi‑Fi keys both use **8766** via Pinger Settings.

---

## Gestures

| Gesture | Action |
|--|--|
| Two-finger swipe right | Status (connection, IP, host) |
| Two-finger swipe left | Preset list |
| Two-finger swipe up | Edit (skins, layout, about) |
| Hold a top / side key, then turn a knob or tap another key | Combo layer (like a physical Pinger) |

---

## Author & license

- Website: [www.aitocg.cn/pinger](https://www.aitocg.cn/pinger)  
- GitHub: [Miatoo/pinger](https://github.com/Miatoo/pinger)  
- Xiaohongshu: 毛桃moatoa  
- License: [MIT License](LICENSE)

[↑ Back to top](#top)

