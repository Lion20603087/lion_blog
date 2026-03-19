## 1 创建“系统镜像任务”（最重要）

打开 Macrium：

👉 选择：

Create an image of the partition(s) required to backup and restore Windows

然后：

勾选：

-   EFI
    
-   MSR
    
-   C盘（win11-AI）
    

---

## 2 选择备份存储位置（非常关键）

👉 不要存 C 盘

建议：

D盘（AI盘）  
或 share盘  
或外接盘（最好）

原则：

备份不能和系统一起死

---

## 3 设置备份计划（自动备份）

点击：

Schedule

推荐配置（非常适合你）👇

---

### Full（完整备份）

每周 1 次  
（比如 周日凌晨）

---

### Differential（差异备份）

每天 1 次  
（凌晨）

---

为什么不用 Incremental？

👉 因为：

你要稳定 > 空间

Incremental 链太长容易坏。

---

## 4 设置保留策略（Retention Rules）

点击：

Retention Rules

推荐设置👇

Full：保留 2-3 个  
Differential：保留 7-14 个

效果：

-   自动删除旧版本
    
-   不占满硬盘
    

---

## 5 启用自动校验（非常重要）

勾选：

Verify image upon completion

作用：

👉 防止备份坏掉你还不知道

---

# 三、手动备份（你需求里的关键点）

在 Macrium 里：

👉 右键任务 → Run Now → Full

使用场景：

大改系统前  
安装AI工具前  
改OpenClaw前

这一步你必须养成习惯。

---

# 四、恢复机制（你最关心的）

## 1 创建“救援启动盘”（必须做）

在 Macrium：

Other Tasks → Create Rescue Media

用：

-   U盘
    

作用：

👉 系统崩了也能恢复

---

## 2 恢复流程（你要理解）

当系统坏了：

插U盘  
启动  
进入Macrium  
选择备份  
恢复

---

# 五、验证（你必须做一次）

👉 这一点很多人不做，结果出事

你要做一次：

模拟恢复流程（不用真的恢复）

测试：

-   能不能识别备份
    
-   能不能进入恢复界面

如下
# 强烈建议）——“假恢复演练”

👉 重点：**不真正写盘，但走完整流程**

---

## 👉 操作步骤

### 1️⃣ 在 Rescue 中点击：

Restore → 选择你的备份

---

### 2️⃣ 点击：

Restore Image

---

### 3️⃣ 进入分区映射界面（关键）

你会看到：

源分区 → 目标磁盘

👉 这一步你要检查：

✔ EFI → EFI  
✔ C盘 → C盘  
✔ Recovery → Recovery

---

### 4️⃣ 不要点 Next（停止在这里）

你只需要确认：

👉 映射是正确的

---

## 🎯 Level 2 通过标准

✔ 能进入恢复流程  
✔ 分区匹配正确  
✔ 没有报错

👉 说明：

👉 真恢复时不会出问题