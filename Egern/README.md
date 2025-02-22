# Egern 配置说明

Egern 是一款强大的 iOS 网络工具，支持多种代理协议和灵活的分流规则配置。

## 文件结构

```
Egern/
├── Egern.yaml              # 主配置文件
├── Rules/                  # 分流规则
├── Modules/                # 重写模块
└── Scripts/                # 脚本文件
```

## 配置说明

### 基础配置示例

```yaml
# 基础设置
mixed-port: 7890
allow-lan: true
mode: rule
log-level: info

# DNS 配置
dns:
  enable: true
  nameserver:
    - 223.5.5.5
    - 119.29.29.29

# 策略组
proxy-groups:
  - name: 🚀 节点选择
    type: select
    proxies:
      - ♻️ 自动选择
      - DIRECT
  
  - name: ♻️ 自动选择
    type: url-test
    url: http://www.gstatic.com/generate_204
    interval: 300
```

## 使用指南

1. 导入配置
   - 打开 Egern → 配置 → 导入配置
   - 选择下载的配置文件

2. 规则说明
   - 分流规则按从上到下顺序匹配
   - 建议将 DIRECT 规则置前
   - 使用 MATCH 规则作为兜底

3. 使用建议
   - 定期更新分流规则
   - 按需启用重写功能
   - 合理设置策略组

## 故障排除

- 配置导入失败：检查 YAML 格式
- 规则不生效：检查规则优先级
- 节点连接问题：确认节点信息正确

## 更新日志

**2025-02-22**
- 优化文档结构
- 更新配置示例
- 完善使用说明

---

*Last Updated: 2025-02-22 *  
*Maintained by: [@Sooinn](https://github.com/Sooinn)*
