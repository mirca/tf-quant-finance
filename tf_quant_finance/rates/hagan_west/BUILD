# Implementation of the Hagan-West algorithm for fitting rate curves.

licenses(["notice"])

# [internal] load python3.bzl

package(default_visibility = ["//tf_quant_finance:__subpackages__"])

py_library(
    name = "hagan_west",
    srcs = ["__init__.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":monotone_convex",
    ],
)

py_library(
    name = "monotone_convex",
    srcs = ["monotone_convex.py"],
    srcs_version = "PY2AND3",
    deps = [
        "//tf_quant_finance/math:diff",
        "//tf_quant_finance/math:piecewise",
        "//tf_quant_finance/rates:forwards",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "monotone_convex_test",
    size = "small",
    srcs = ["monotone_convex_test.py"],
    shard_count = 3,
    deps = [
        ":monotone_convex",
        # numpy dep,
        # tensorflow dep,
    ],
)