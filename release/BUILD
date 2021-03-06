package(default_visibility = ["//visibility:public"])

load("//infra/bazel:zip.bzl", "pkg_zip")
load("//release:mapping.bzl", "gen_mappings")

filegroup(
    name = "config_json",
    srcs = [
        "config/config.json",
        "config/vpoint_socks_vmess.json",
        "config/vpoint_vmess_freedom.json",
    ],
)

filegroup(
    name = "systemd",
    srcs = [
        "config/systemd/v2ray.service",
        "config/systemv/v2ray",
    ],
)

filegroup(
    name = "doc",
    srcs = glob(["doc/*.md"]),
)

filegroup(
    name = "geodata",
    srcs = [
        "config/geoip.dat",
        "config/geosite.dat",
    ],
)

pkg_zip(
    name = "v2ray_darwin_amd64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_darwin_amd64",
        "//infra/control/main:v2ctl_darwin_amd64_sig",
        "//main:v2ray_darwin_amd64",
        "//main:v2ray_darwin_amd64_sig",
    ],
    out = "v2ray-macos.zip",
    mappings = gen_mappings("darwin", "amd64"),
)

pkg_zip(
    name = "v2ray_windows_amd64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_windows_amd64",
        "//infra/control/main:v2ctl_windows_amd64_sig",
        "//main:v2ray_windows_amd64",
        "//main:v2ray_windows_amd64_nowindow",
        "//main:v2ray_windows_amd64_nowindow_sig",
        "//main:v2ray_windows_amd64_sig",
    ],
    out = "v2ray-windows-64.zip",
    mappings = gen_mappings("windows", "amd64"),
)

pkg_zip(
    name = "v2ray_windows_x86_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_windows_386",
        "//infra/control/main:v2ctl_windows_386_sig",
        "//main:v2ray_windows_386",
        "//main:v2ray_windows_386_nowindow",
        "//main:v2ray_windows_386_nowindow_sig",
        "//main:v2ray_windows_386_sig",
    ],
    out = "v2ray-windows-32.zip",
    mappings = gen_mappings("windows", "386"),
)

pkg_zip(
    name = "v2ray_windows_arm_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_windows_arm_armv5",
        "//infra/control/main:v2ctl_windows_arm_armv5_sig",
        "//infra/control/main:v2ctl_windows_arm_armv6",
        "//infra/control/main:v2ctl_windows_arm_armv6_sig",
        "//infra/control/main:v2ctl_windows_arm_armv7",
        "//infra/control/main:v2ctl_windows_arm_armv7_sig",
        "//main:v2ray_windows_arm_armv5",
        "//main:v2ray_windows_arm_armv5_sig",
        "//main:v2ray_windows_arm_armv5_nowindow",
        "//main:v2ray_windows_arm_armv5_nowindow_sig",
        "//main:v2ray_windows_arm_armv6",
        "//main:v2ray_windows_arm_armv6_sig",
        "//main:v2ray_windows_arm_armv6_nowindow",
        "//main:v2ray_windows_arm_armv6_nowindow_sig",
        "//main:v2ray_windows_arm_armv7",
        "//main:v2ray_windows_arm_armv7_sig",
        "//main:v2ray_windows_arm_armv7_nowindow",
        "//main:v2ray_windows_arm_armv7_nowindow_sig",
    ],
    out = "v2ray-windows-arm.zip",
    mappings = gen_mappings("windows", "arm"),
)

pkg_zip(
    name = "v2ray_freebsd_amd64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_freebsd_amd64",
        "//infra/control/main:v2ctl_freebsd_amd64_sig",
        "//main:v2ray_freebsd_amd64",
        "//main:v2ray_freebsd_amd64_sig",
    ],
    out = "v2ray-freebsd-64.zip",
    mappings = gen_mappings("freebsd", "amd64"),
)

pkg_zip(
    name = "v2ray_freebsd_x86_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_freebsd_386",
        "//infra/control/main:v2ctl_freebsd_386_sig",
        "//main:v2ray_freebsd_386",
        "//main:v2ray_freebsd_386_sig",
    ],
    out = "v2ray-freebsd-32.zip",
    mappings = gen_mappings("freebsd", "386"),
)

pkg_zip(
    name = "v2ray_openbsd_amd64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_openbsd_amd64",
        "//infra/control/main:v2ctl_openbsd_amd64_sig",
        "//main:v2ray_openbsd_amd64",
        "//main:v2ray_openbsd_amd64_sig",
    ],
    out = "v2ray-openbsd-64.zip",
    mappings = gen_mappings("openbsd", "amd64"),
)

pkg_zip(
    name = "v2ray_openbsd_x86_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_openbsd_386",
        "//infra/control/main:v2ctl_openbsd_386_sig",
        "//main:v2ray_openbsd_386",
        "//main:v2ray_openbsd_386_sig",
    ],
    out = "v2ray-openbsd-32.zip",
    mappings = gen_mappings("openbsd", "386"),
)

pkg_zip(
    name = "v2ray_dragonfly_amd64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        "//infra/control/main:v2ctl_dragonfly_amd64",
        "//infra/control/main:v2ctl_dragonfly_amd64_sig",
        "//main:v2ray_dragonfly_amd64",
        "//main:v2ray_dragonfly_amd64_sig",
    ],
    out = "v2ray-dragonfly-64.zip",
    mappings = gen_mappings("dragonfly", "amd64"),
)

pkg_zip(
    name = "v2ray_linux_amd64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_amd64",
        "//infra/control/main:v2ctl_linux_amd64_sig",
        "//main:v2ray_linux_amd64",
        "//main:v2ray_linux_amd64_sig",
    ],
    out = "v2ray-linux-64.zip",
    mappings = gen_mappings("linux", "amd64"),
)

pkg_zip(
    name = "v2ray_linux_x86_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_386",
        "//infra/control/main:v2ctl_linux_386_sig",
        "//main:v2ray_linux_386",
        "//main:v2ray_linux_386_sig",
    ],
    out = "v2ray-linux-32.zip",
    mappings = gen_mappings("linux", "386"),
)

pkg_zip(
    name = "v2ray_linux_arm_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_arm_armv5",
        "//infra/control/main:v2ctl_linux_arm_armv5_sig",
        "//infra/control/main:v2ctl_linux_arm_armv6",
        "//infra/control/main:v2ctl_linux_arm_armv6_sig",
        "//infra/control/main:v2ctl_linux_arm_armv7",
        "//infra/control/main:v2ctl_linux_arm_armv7_sig",
        "//main:v2ray_linux_arm_armv5",
        "//main:v2ray_linux_arm_armv5_sig",
        "//main:v2ray_linux_arm_armv6",
        "//main:v2ray_linux_arm_armv6_sig",
        "//main:v2ray_linux_arm_armv7",
        "//main:v2ray_linux_arm_armv7_sig",
    ],
    out = "v2ray-linux-arm.zip",
    mappings = gen_mappings("linux", "arm"),
)

pkg_zip(
    name = "v2ray_linux_arm64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_arm64",
        "//infra/control/main:v2ctl_linux_arm64_sig",
        "//main:v2ray_linux_arm64",
        "//main:v2ray_linux_arm64_sig",
    ],
    out = "v2ray-linux-arm64.zip",
    mappings = gen_mappings("linux", "arm64"),
)

pkg_zip(
    name = "v2ray_linux_mips_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_mips",
        "//infra/control/main:v2ctl_linux_mips_sig",
        "//infra/control/main:v2ctl_linux_mips_softfloat",
        "//infra/control/main:v2ctl_linux_mips_softfloat_sig",
        "//main:v2ray_linux_mips",
        "//main:v2ray_linux_mips_sig",
        "//main:v2ray_linux_mips_softfloat",
        "//main:v2ray_linux_mips_softfloat_sig",
    ],
    out = "v2ray-linux-mips.zip",
    mappings = gen_mappings("linux", "mips"),
)

pkg_zip(
    name = "v2ray_linux_mipsle_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_mipsle",
        "//infra/control/main:v2ctl_linux_mipsle_sig",
        "//infra/control/main:v2ctl_linux_mipsle_softfloat",
        "//infra/control/main:v2ctl_linux_mipsle_softfloat_sig",
        "//main:v2ray_linux_mipsle",
        "//main:v2ray_linux_mipsle_sig",
        "//main:v2ray_linux_mipsle_softfloat",
        "//main:v2ray_linux_mipsle_softfloat_sig",
    ],
    out = "v2ray-linux-mipsle.zip",
    mappings = gen_mappings("linux", "mipsle"),
)

pkg_zip(
    name = "v2ray_linux_mips64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_mips64",
        "//infra/control/main:v2ctl_linux_mips64_sig",
        "//main:v2ray_linux_mips64",
        "//main:v2ray_linux_mips64_sig",
    ],
    out = "v2ray-linux-mips64.zip",
    mappings = gen_mappings("linux", "mips64"),
)

pkg_zip(
    name = "v2ray_linux_mips64le_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_mips64le",
        "//infra/control/main:v2ctl_linux_mips64le_sig",
        "//main:v2ray_linux_mips64le",
        "//main:v2ray_linux_mips64le_sig",
    ],
    out = "v2ray-linux-mips64le.zip",
    mappings = gen_mappings("linux", "mips64le"),
)

pkg_zip(
    name = "v2ray_linux_s390x_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_s390x",
        "//infra/control/main:v2ctl_linux_s390x_sig",
        "//main:v2ray_linux_s390x",
        "//main:v2ray_linux_s390x_sig",
    ],
    out = "v2ray-linux-s390x.zip",
    mappings = gen_mappings("linux", "s390x"),
)

pkg_zip(
    name = "v2ray_linux_ppc64_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_ppc64",
        "//infra/control/main:v2ctl_linux_ppc64_sig",
        "//main:v2ray_linux_ppc64",
        "//main:v2ray_linux_ppc64_sig",
    ],
    out = "v2ray-linux-ppc64.zip",
    mappings = gen_mappings("linux", "ppc64"),
)

pkg_zip(
    name = "v2ray_linux_ppc64le_package",
    srcs = [
        ":config_json",
        ":doc",
        ":geodata",
        ":systemd",
        "//infra/control/main:v2ctl_linux_ppc64le",
        "//infra/control/main:v2ctl_linux_ppc64le_sig",
        "//main:v2ray_linux_ppc64le",
        "//main:v2ray_linux_ppc64le_sig",
    ],
    out = "v2ray-linux-ppc64le.zip",
    mappings = gen_mappings("linux", "ppc64le"),
)
