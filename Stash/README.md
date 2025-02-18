# Stash 配置

## 配置说明

此目录包含了优化后的 Stash 配置文件，适用于 iOS 和 macOS 平台。

## 文件列表

- `config.yaml`: 主配置文件

## 特性

- DNS 优化配置
  - DoH/DoT 支持
  - 防 DNS 泄露
- TLS 1.3 支持
- 完整的分流规则
  - 应用分流（YouTube、Telegram等）
  - 地区分流（港台日美新等）
- 多样化策略组
  - 自动测速
  - 负载均衡
  - 故障转移
- 隐私保护
  - 广告拦截
  - 隐私规则
  - 安全防护

## 使用方法

1. 下载 `config.yaml`
2. 修改订阅链接
   ```yaml
   proxy-providers:
     机场01:
       url: "替换为你的订阅链接"
   ```
3. 导入到 Stash
