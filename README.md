# IntelliJ IDEA 恢复交互式弹窗提交配置

如果你的 IDEA 2026 提交按钮消失，或者想要找回传统的交互式弹窗提交界面，请按照以下步骤修改导出的设置文件。

## 操作流程

### 1. 导出 IDEA 设置
1. 打开 IDEA，点击 `File` -> `Manage IDE Settings` -> `Export Settings...`。
2. 将导出的 `settings.zip` 保存到本地。

### 2. 修改配置文件
1. 解压 `settings.zip`。
2. 找到并打开以下文件：
   `options/advancedSettings.xml`
3. 在 `<map>` 节点中添加 `git.non.modal.commit` 入口，并确保其值为 `true`。

### 3. 代码片段
请确保 `advancedSettings.xml` 中的内容包含以下部分：

```xml
<application>
  <component name="AdvancedSettings">
    <option name="settings">
      <map>
        <entry key="git.non.modal.commit" value="true" />
      </map>
    </option>
  </component>
</application>
```

# 吐槽

这个功能对我很重要，侧边栏的提交我会疯掉(裂开)
