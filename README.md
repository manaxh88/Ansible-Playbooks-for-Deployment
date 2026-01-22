# Ansible Playbooks for Deployment  
Ansible 自动化部署与配置管理

## 项目简介  
本仓库包含使用 Ansible 编写的 Playbook，主要实现 Linux 服务器上常见服务的批量安装、配置下发和版本管控。  

## 主要 Playbook  
- **deploy_nginx_mysql.yml**  
  功能：在 CentOS/Ubuntu 上批量安装 Nginx + MySQL，启动服务并简单安全加固。  
  支持主机组批量执行。

## 适用场景  
- 多节点集群快速部署  
- 环境标准化与配置一致性保障  
- DevOps 管道中的自动化部署环节

## 快速上手  
1. 安装 Ansible（`pip install ansible` 或系统包管理）  
2. 配置 inventory 文件（hosts.ini）  
   示例：
       [webservers]
       192.168.1.10
       192.168.1.11
3. 运行：`ansible-playbook -i hosts.ini deploy_nginx_mysql.yml`  
4. 建议结合 Ansible Vault 加密敏感信息（如数据库密码）

## 项目成果  
- 部署时间从小时级缩短至分钟级  
- 自动化率提升 50%  
- 集群配置一致性 100%，减少配置漂移问题
