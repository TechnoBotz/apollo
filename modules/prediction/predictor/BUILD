load("//tools:cpplint.bzl", "cpplint")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "predictor_manager",
    srcs = ["predictor_manager.cc"],
    hdrs = ["predictor_manager.h"],
    deps = [
        "//modules/common:macro",
        "//modules/perception/proto:perception_proto",
        "//modules/prediction/common:prediction_gflags",
        "//modules/prediction/container:container_manager",
        "//modules/prediction/container/obstacles:obstacles_container",
        "//modules/prediction/predictor/pedestrian:regional_predictor",
        "//modules/prediction/predictor/vehicle:free_move_predictor",
        "//modules/prediction/predictor/vehicle:lane_sequence_predictor",
        "//modules/prediction/proto:prediction_conf_proto",
        "//modules/prediction/proto:prediction_proto",
        "@glog//:glog",
    ],
)

cc_test(
    name = "predictor_manager_test",
    size = "small",
    srcs = ["predictor_manager_test.cc"],
    data = [
        "//modules/prediction:prediction_data",
        "//modules/prediction:prediction_testdata",
    ],
    deps = [
        "//modules/common/util",
        "//modules/prediction/predictor:predictor_manager",
        "//modules/prediction/proto:prediction_conf_proto",
        "@gtest//:main",
    ],
)

cc_library(
    name = "predictor",
    srcs = ["predictor.cc"],
    hdrs = ["predictor.h"],
    deps = [
        "//modules/common/proto:pnc_point_proto",
        "//modules/prediction/container/obstacles:obstacle",
        "//modules/prediction/proto:prediction_proto",
    ],
)

cpplint()
