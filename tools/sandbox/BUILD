if CONFIG.get("STATIC_SANDBOX"):
    # TODO(peterebden): figure out why c_binary isn't doing what we want here.
    genrule(
        name = "please_sandbox",
        srcs = ["main.c"],
        outs = ["please_sandbox"],
        cmd = "$TOOL -static -no-pie -s -Wl,--build-id=none -o $OUT $SRCS",
        tools = [CONFIG.CC_TOOL],
        visibility = ["PUBLIC"],
    )
else:
    c_binary(
        name = "please_sandbox",
        srcs = ["main.c"],
        visibility = ["PUBLIC"],
    )
