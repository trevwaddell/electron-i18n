## 类: BrowserView

> 创建和控制视图

**注意:** BrowserView 的 API目前为实验性质，可能会更改或删除。

线程：[主进程](../glossary.md#main-process)

`BrowserView`被用来让`BrowserWindow`嵌入更多的 web 内容。 它就像一个子窗口，除了它的位置是相对于父窗口。 这意味着可以替代`webview`标签.

## 例子

```javascript
// 在主进程中.
const {BrowserView, BrowserWindow} = require('electron')

let win = new BrowserWindow({width: 800, height: 600})
win.on('closed', () => {
  win = null
})

let view = new BrowserView({
  webPreferences: {
    nodeIntegration: false
  }
})
win.setBrowserView(view)
view.setBounds({ x: 0, y: 0, width: 300, height: 300 })
view.webContents.loadURL('https://electron.atom.io')
```

### `new BrowserView([可选])` *实验功能*

* `options` Object (可选) 
  * `webPreferences` Object (可选) - 详情请看 [BrowserWindow](browser-window.md).

### 静态方法

#### `BrowserView.fromId(id)`

* `id` Integer

返回 `BrowserView` - 带有`id`的视图.

### 实例属性

使用 `new BrowserView` 创建的对象具有以下属性:

#### `view.webContents` *实验功能*

视图的[`WebContents`](web-contents.md) 对象

#### `view.id` *实验功能*

视图的唯一ID `Integer`.

### 实例方法

使用 `new BrowserView`创建的对象具有以下实例方法:

#### `view.setAutoResize(options)` *实验功能*

* `options` Object 
  * `width` Boolean - 如果为`true`，视图宽度跟随窗口变化. 默认为 `false`.
  * `height` Boolean - 如果为`true`，视图高度跟随窗口变化. 默认为 `false`.

#### `view.setBounds(bounds)` *实验功能*

* ` bounds`[ 矩形 ](structures/rectangle.md)

调整视图的大小，并将它移动到窗口边界

#### `view.setBackgroundColor(color)` *实验功能*

* `color` String - 颜色值格式为 `#aarrggbb` 或 `#argb`, 透明度为可选参数.