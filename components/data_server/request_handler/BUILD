load("@rules_cc//cc:defs.bzl", "cc_library", "cc_test")

package(default_visibility = [
    "//components/data_server:__subpackages__",
])

cc_library(
    name = "get_values_handler",
    srcs = [
        "get_values_handler.cc",
    ],
    hdrs = [
        "get_values_handler.h",
    ],
    deps = [
        "//components/data_server/cache",
        "//infrastructure/communication:bhttp_utils",
        "//public:base_types_cc_proto",
        "//public:constants",
        "//public/query:get_values_cc_grpc",
        "@com_github_google_glog//:glog",
        "@com_github_google_quiche//quiche:binary_http_unstable_api",
        "@com_github_grpc_grpc//:grpc++",
        "@com_google_absl//absl/strings",
        "@com_google_protobuf//:protobuf",
    ],
)

cc_test(
    name = "get_values_handler_test",
    size = "small",
    srcs = [
        "get_values_handler_test.cc",
    ],
    deps = [
        ":get_values_handler",
        "//components/data_server/cache",
        "//components/data_server/cache:mocks",
        "//infrastructure/communication:bhttp_utils",
        "//public/query:get_values_cc_grpc",
        "//public/test_util:proto_matcher",
        "@com_github_google_quiche//quiche:binary_http_unstable_api",
        "@com_github_grpc_grpc//:grpc++",
        "@com_google_googletest//:gtest_main",
    ],
)
