针对Kali Linux的完整镜像源配置指南，配合测试后镜像源地址，可显著提升软件下载速度：

---

### ⚙️ 一、配置步骤（需root权限）
1. **备份源列表**  
   ```bash
   sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
   ```

2. **编辑源配置文件**  
   ```bash
   sudo nano /etc/apt/sources.list  # 或使用vim
   ```
   - 删除原有内容或用”#“注释掉，粘贴所选镜像源配置（**仅保留一个源**，避免冲突）。

3. **更新软件仓库**  
   ```bash
   sudo apt update && sudo apt upgrade -y  # 更新源并升级系统
   ```
    - ⚠️ apt full-upgrade 也用于升级软件包，并在遇到依赖关系冲突时，提供更彻底的解决方案。


---

### ⚠️ 二、常见问题解决
- **GPG签名错误**（`NO_PUBKEY`）:  
更换 Kali Linux 的软件源后，出现 `NO_PUBKEY` 或 GPG 签名错误时，此命令可解决问题。
  ```bash
  sudo wget https://archive.kali.org/archive-keyring.gpg -O /usr/share/keyrings/kali-archive-keyring.gpg
  ```
**作用**：  
直接下载 Kali 官方 GPG 密钥文件，并保存到 `/usr/share/keyrings/` 目录

- **网络质量差导致下载中断**:  
  终止当前任务（`Ctrl+C`），切换其他镜像源后重试`apt update`。




### 💎 三、官方资源补充
- **最新版下载**：[https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)  
- **历史版本库** https://old.kali.org/kali-images/
- **预构建镜像库**：https://cdimage.kali.org/ 
- **完镜像站列表**：[Kali Official Mirrors](https://http.kali.org/README.mirrorlist)  

> 配置完成后，软件安装速度可提升3-5倍。建议定期运行 `apt update` 保持工具最新。