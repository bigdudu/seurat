# Copyright 2017 Google Inc. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS-IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load(
    "//seurat/dev:build_defs.bzl",
    "cc_test",
    "test_suite",
)

package_group(
    name = "friends",
    packages = [
        "//seurat/...",
    ],
)

package(
    default_visibility = [":friends"],
)

cc_library(
    name = "image_metrics",
    srcs = [
        "image_metrics.cc",
    ],
    hdrs = [
        "image_metrics.h",
    ],
    deps = [
        "//seurat/image",
        "@ion//:iongfx",
        "@ion//:ionmath",
    ],
)

cc_test(
    name = "image_metrics_test",
    size = "small",
    srcs = ["image_metrics_test.cc"],
    deps = [
        ":image_metrics",
        "//seurat/image",
        "//seurat/image:image_test_utils",
        "@com_google_googletest//:gtest",
        "@com_google_googletest//:gtest_main",
        "@ion//:ionmath",
    ],
)

test_suite(
    name = "image_metrics_tests",
    tests = [
        ":image_metrics_test",
    ],
)
