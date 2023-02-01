# 导入go_binary、go_test、go_library方法
load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library", "go_test")

# 构建二进制程序
go_binary(
    name = "hello",
    srcs = ["hello.go"],
    deps = [":greeter"],
)

# 构建库
go_library(
    name = "greeter",
    importpath = "github.com/tx7do/bazel-golang-minimal-example/greeter",
    srcs = ["greeter.go"],
)

# 构建单元测试
go_test(
    name = "greeter_test",
    srcs = [ "greeter_test.go" ],
    embed = [ ":greeter" ],
)
