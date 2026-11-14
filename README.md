<a id="top"></a>
<a id="zh"></a>

# Pinger v1.0.2beta

把 Android 手机变成一块「快捷键面板」：在 Photoshop、剪辑等软件里，用手机按键、旋钮代替键盘快捷键。

**语言** [中文](#zh) · [English](#en)

**下载** [官网](https://www.aitocg.cn/pinger) · [GitHub Releases](https://github.com/Miatoo/pinger/releases)

## 本版更新（相对 v1.0.1beta）

- Spec 皮肤按键文字居中；十字键四向标签对齐
- 快捷键设置：十字键展开为 D1–D4 四个独立绑定（与四向文字一致）
- 布局编辑：移动 / 缩放 / 旋转后，文字、触控与滑条填充跟随键体
- 旋钮布局旋转后，指针仍绕正确中心转动
- 粗野 / 纸白等皮肤命中区与视觉对齐；布局工具栏更紧凑
- iOS：已连但不出字问题（键盘-only 描述符，不再发 gamepad 报告）
- 新增预设：Procreate (iPad)、剪映专业版、After Effects、CLIP STUDIO v2

## 下载哪个文件

| 文件 | 装在哪 | 说明 |
| --- | --- | --- |
| **Pinger-v1.0.2beta.apk** | Android 手机 | 主程序（必装） |
| **SHA256SUMS.txt** | — | 安装包校验码（可选） |

> **推荐**：只装手机 APK，用蓝牙连电脑。
>
> 电脑端 **Pinger Settings**（改排版 / WiFi）本包未重打；可继续使用 [v1.0.1beta](../v1.0.1beta/) 的 Settings zip。

## 先看：已知限制

| 现象 | 说明 | 处理 |
| --- | --- | --- |
| 部分国产手机注册 HID 失败 | 对「蓝牙 HID 键盘」支持不完整 | 改用 WiFi 模式 |
| 语音（MIC）不可用 | 蓝牙通道下的语音仍在完善 | 本版本请勿强依赖 MIC 键 |
| Windows 配对后显示「手机」 | 配对不等于连上键盘通道 | 回 App 内再点「连键盘」 |

## 安装

### 手机（Pinger）

1. 把 `Pinger-v1.0.2beta.apk` 传到手机并安装（需允许「未知来源」）。
2. 若之前装过旧版，可直接覆盖；若提示签名冲突，先卸载旧版再装。
3. 打开 App，允许**蓝牙**权限；建议**横屏**使用。

### 电脑（Pinger Settings，可选）

继续使用 v1.0.1beta 的 `PingerSettings-v1.0.1beta-windows-x64.zip` 即可（端口 **8766**）。

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

手机上也可直接进入布局编辑、快捷键编辑。

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

**Pinger-v1.0.2beta.apk**

```
a71b03ce071766dd91036e3c45546e728fd898d371925d7ceae08fab36a21fd1
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

## What's new (vs v1.0.1beta)

- Spec skin captions centered; D-pad labels aligned
- Shortcut editor: D-pad expands to four bindings (D1–D4)
- Layout editor: captions, hit targets, and fader fills follow move / scale / rotate
- Knob needle stays on-center after layout rotation
- Brutal / Paper hit zones aligned; compact layout toolbar
- iOS: connected-but-no-keys fix (keyboard-only descriptor)
- New presets: Procreate (iPad), CapCut Pro, After Effects, CLIP STUDIO v2

## What to download

| File | Where | Purpose |
| --- | --- | --- |
| **Pinger-v1.0.2beta.apk** | Android phone | Main app (required) |
| **SHA256SUMS.txt** | — | Checksums (optional) |

> Phone APK + Bluetooth is enough for most users. Desktop **Pinger Settings** is not rebuilt in this package — keep using the [v1.0.1beta](../v1.0.1beta/) Settings zip if needed.

## Known limits

| Symptom | Cause | Fix |
| --- | --- | --- |
| HID registration fails on some phones | Incomplete Bluetooth HID support | Switch to Wi-Fi mode |
| Voice (MIC) not working | Still in progress on Bluetooth | Do not rely on MIC in this build |
| Windows shows "phone" after pairing | Pairing ≠ keyboard channel | Tap **Connect keyboard** in the app |

## Install

**Phone:** install `Pinger-v1.0.2beta.apk` (allow unknown sources). Grant Bluetooth; landscape recommended.

**Windows (optional):** reuse `PingerSettings-v1.0.1beta-windows-x64.zip` from the previous release (port **8766**).

## First use (Bluetooth)

1. Two-finger **swipe right** → Status.
2. Pick host: Win / Mac / iPad / Android.
3. **Register HID** → **Discoverable**.
4. Pair from the computer / tablet.
5. On the phone: **paired host** → **Connect keyboard**.
6. Test in Notepad or Photoshop.

## SHA256

**Pinger-v1.0.2beta.apk**

```
a71b03ce071766dd91036e3c45546e728fd898d371925d7ceae08fab36a21fd1
```

## Links

| Item | URL |
| --- | --- |
| Website | [www.aitocg.cn/pinger](https://www.aitocg.cn/pinger) |
| GitHub | [Miatoo/pinger](https://github.com/Miatoo/pinger) |
| License | MIT |

[↑ Back to top](#top)
