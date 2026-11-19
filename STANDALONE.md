# SDK 独立使用说明

本仓库从 `zx_test_project` 整包仓库的 `45042066` 拆分，保留 SDK 相关历史。
应用工程独立维护，下载 SDK 不会连带下载手表或蓝牙音频工程。

```bash
git clone https://gitee.com/a2641293697/SiFli-SDK.git
cd SiFli-SDK
# 按 README.md 安装环境后导出。
source ./export.sh --profile default
```

`middleware/bluetooth` 和 `tools/SiliconSchema` 在本发行仓库中是完整源码，
无需执行子模块下载；上游 `.gitmodules` 保留供参考，本仓库无对应 gitlink。
客户工程通过导出的 `SIFLI_SDK` 使用该 SDK，不要求固定目录布局。
拆分前未提交的本地修改继续保留为工作区修改。
