cc_library(
    name = "beast",
    srcs = [
        "beast.cc",
    ],
    hdrs = ["beast.h"],
    visibility = ["//visibility:public"],
    deps = [
        ":api_json",
        "@boost//:beast",
        "@nlohmann//:json",
    ],
)

cc_library(
    name = "api_json",
    srcs = ["api_json.cc"],
    hdrs = ["api_json.h"],
    deps = [
        ":api",
        "@boost//:config",
        "@boost//:core",
        "@boost//:fusion",
        "@boost//:move",
        "@boost//:range",
        "@boost//:thread",
        "@com_github_gflags_gflags//:gflags",
        "@com_github_google_glog//:glog",
        "@nlohmann//:json",
        "@org_iota_common//common/helpers:digest",
        "@org_iota_common//common/model:tryte_transaction",
    ],
)

cc_library(
    name = "api",
    hdrs = [
        "api.h",
        "messages.h",
    ],
    visibility = ["//visibility:public"],
    deps = ["@optional_lite"],
)

cc_test(
    name = "tests",
    timeout = "short",
    srcs = glob(["tests/**/*.cc"]),
    deps = [
        ":beast",
        "@com_google_googletest//:gtest_main",
    ],
)
