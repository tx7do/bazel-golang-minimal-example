# 定义工作环境名称
workspace(name = "com_github_tx7do_bazel_golang_minimal_example")

# 导入http_archive方法
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# 下载rules_go
http_archive(
    name = "io_bazel_rules_go",
    sha256 = "56d8c5a5c91e1af73eca71a6fab2ced959b67c86d12ba37feedb0a2dfea441a6",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_go/releases/download/v0.37.0/rules_go-v0.37.0.zip",
        "https://github.com/bazelbuild/rules_go/releases/download/v0.37.0/rules_go-v0.37.0.zip",
    ],
)

# 导入go_register_toolchains和go_rules_dependencies方法
load("@io_bazel_rules_go//go:deps.bzl", "go_register_toolchains", "go_rules_dependencies")

# 初始化go规则集的依赖项
go_rules_dependencies()

# 注册go 1.19.5版本的工具链，包含下载安装go环境。
go_register_toolchains(version = "1.19.5")
