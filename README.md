# skopeo-static
This contains a GitHub Workflow to publish skopeo static binaries on GitHub Releases.

The resulting binary is statically compiled and can be validated via:

```sh
$ ldd skopeo-nightly
	not a dynamic executable
$ file skopeo-nightly
skopeo-nightly: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), statically linked, Go BuildID=bFc-TSUNHTBADRch8C6z/sys6zdb4zQYqfCzzMUBX/P7NgMLDOOvUbKM2N5_uJ/hQmD6YKcZfJwbbVzxrnS, with debug_info, not stripped
```

Instructions from [here](https://github.com/containers/skopeo/blob/main/install.md#building-a-static-binary).

> Keep in mind that the resulting binary is unsupported and might crash randomly. Only use if you know what you're doing!
