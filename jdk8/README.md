# Ansible Role: java

添加jdk1.8版本

## 要求

此角色仅在RHEL及其衍生产品上运行。

## 测试环境

ansible `2.3.0.0`
os `Centos 6.7 X64`
python `2.6.6`

## 角色变量
    software_files_path: "/opt/software"
    software_install_path: "/usr/local"

    java_version: "1.7"
    java_home: "/usr/java/jdk1.7.0_80"

    java_file: "jdk-7u80-linux-x64.tar.gz"
    java_file_path: "{{ software_files_path }}/{{ java_file }}"
    java_install_path: "{{ software_install_path }}/jdk1.7.0_80"
    java_file_url: "http://download.oracle.com/otn/java/jdk/7u80-b15/d54c1d3a095b4ff2b6607d096fa80163/jdk-7u80-linux-x64.tar.gz"


## 依赖
在jdk8下新建files 文件夹 将自己的jdktar包复制到jdk8的files目录下 然后替换vars/jdk1.8里面的变量名
## github地址
https://github.com/lework/Ansible-roles/tree/master/java

## Example Playbook
jdk 1.8版本
 ```yaml
    - hosts: node1
      roles:
       - jdk8
 ```
