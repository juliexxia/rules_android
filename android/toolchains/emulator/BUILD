# Description:
#   Defines an emulator toolchain so that the emulator used for android_device
#   can be configured at build-time.

load(":toolchain.bzl", "emulator_toolchain")

package(default_visibility = ["//visibility:public"])

# By convention, toolchain_type targets are named "toolchain_type"
# and distinguished by their package path.
toolchain_type(
    name = "toolchain_type",
)

emulator_toolchain(
    name = "emulator_default",
    emulator = "@androidsdk//:emulator",
    emulator_deps = [
        "@androidsdk//:emulator_shared_libs",
    ],
)

toolchain(
    name = "emulator_default_toolchain",
    toolchain = ":emulator_default",
    toolchain_type = ":toolchain_type",
)
