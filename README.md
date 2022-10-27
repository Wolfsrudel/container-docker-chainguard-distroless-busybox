# busybox

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/busybox/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/busybox/actions/workflows/release.yaml)

Container image with only busybox and libc (available in both musl and glibc variants). Suitable for running any binaries that only have a dependency on glibc/musl.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/busybox:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `1.35.0-r27` `latest` | `sha256:622fb94ed9f3566f9bff4e19f362f43a401baba1c72f6de8d6799d7a8360e788`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:622fb94ed9f3566f9bff4e19f362f43a401baba1c72f6de8d6799d7a8360e788) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `1.35.0-r25` | `sha256:62eae6a74ce7304c3ef45bdbce9f17f40929f9bdd0ec6da80c84ab4af2bb6057`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:62eae6a74ce7304c3ef45bdbce9f17f40929f9bdd0ec6da80c84ab4af2bb6057) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `1.35.0-r2-glibc` | `sha256:a76760a49c6966fa0516404736d7949299433d959ab9910d841e2e3a0f301d48`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:a76760a49c6966fa0516404736d7949299433d959ab9910d841e2e3a0f301d48) | `amd64` |
| `1.35.0-r3-glibc` | `sha256:2b8537226cd3abf1105749708f5e8108bbe4c3268713ef0d3860130e1ac006d9`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:2b8537226cd3abf1105749708f5e8108bbe4c3268713ef0d3860130e1ac006d9) | `amd64` |



## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/busybox:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/busybox:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/busybox"
      },
      "image": {
        "docker-manifest-digest": "sha256:622fb94ed9f3566f9bff4e19f362f43a401baba1c72f6de8d6799d7a8360e788"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "cd2f1e888f64dd8504760e368ea653a6d28417cb",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/busybox",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIQDkPr2rgEqmHvSVSdcu06sMsHXNGstUUoubczwgQpwS9wIgXy25/ngMKSeHb9f5Wi4uUThn6mfc0nmMT/2tEkA8OIU=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiI2ZGFhNmZlZTFlZWI0ZjEwMDQ3ZTgyMWE5NjJhN2MwZTVhYjM0YTVmNTFhZTgyODM1MWQxOWJjNWM4OThmNDc1In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FWUNJUUNWaFZnWk5obGM2WXFLQWlZOGVyUXpnYVFtU1pBbkZldkpITXpuZVFwaW9RSWhBTzMrUmZGallGdDBBZitzanNJY2IzQlJEQjYvbnczdmRQSGFoS2NkbllvWiIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnlha05EUVhwVFowRjNTVUpCWjBsVlpVRnpkM0ZOZEZKcVlsZDFTVnBWTTBkNVpHRmliWE5GVmpacmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFFU1ROTlJFRXdUa1JCTVZkb1kwNU5ha2w0VFVSSk0wMUVRVEZPUkVFeFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZNVFVkSE1XaEdhbFU0WjNoWVowdHZNMVkyYm5Gdk4yUXZhbU5uTUdjeVUwVnViR01LTVVsNlRVUlRTbUZzYnpSdFRrOUxhRnBDZHpWM2RHUXhRbVZEWVZndldUaHlLMHRKTHk5RFRrRjBWV1J0TmtKRFdXRlBRMEZzVFhkblowcFFUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZyTVRGcENqTkNhbUV5Wm1aalpGUXlkbXBsYmxkbU4yMU1VVFpCZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJGUldVUldVakJTUVZGSUwwSkdPSGRZV1ZwaVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5U2pGak0yeHBZak5uZGt4dFpIQmtSMmd4V1drNU0ySXpTbkphYlhoMlpETk5kbU50Vm5OYVYwWjZXbE0xTlZsWE1YTlJTRXBzQ2xwdVRYWmhSMVpvV2toTmRtSlhSbkJpYWtFMVFtZHZja0puUlVWQldVOHZUVUZGUWtKRGRHOWtTRkozWTNwdmRrd3pVblpoTWxaMVRHMUdhbVJIYkhZS1ltNU5kVm95YkRCaFNGWnBaRmhPYkdOdFRuWmlibEpzWW01UmRWa3lPWFJOUWxsSFEybHpSMEZSVVVKbk56aDNRVkZKUlVOSVRtcGhSMVpyWkZkNGJBcE5SRmxIUTJselIwRlJVVUpuTnpoM1FWRk5SVXRIVG10TmJWbDRXbFJuTkU5SFdUSk9SMUpyVDBSVmQwNUVZekpOUjFWNlRtcG9iRmxVV1RGTk1rVXlDbHBFU1RST1JFVXpXVEpKZDBoQldVdExkMWxDUWtGSFJIWjZRVUpDUVZGUFVUTktiRmxZVW14SlJrcHNZa2RXYUdNeVZYZEtkMWxMUzNkWlFrSkJSMFFLZG5wQlFrSlJVVnBaTW1ob1lWYzFibVJYUm5sYVF6RndZbGRHYmxwWVRYWlpibFo2WlZkS2RtVkVRV1JDWjI5eVFtZEZSVUZaVHk5TlFVVkhRa0U1ZVFwYVYxcDZUREpvYkZsWFVucE1NakZvWVZjMGQyZFpjMGREYVhOSFFWRlJRakZ1YTBOQ1FVbEZabEZTTjBGSWEwRmtkMEZKV1VwTWQwdEdUQzloUlZoU0NqQlhjMjVvU25oR1duaHBjMFpxTTBSUFRrcDBOWEozYVVKcVduWmpaMEZCUVZsUlZ6VlhNRmxCUVVGRlFYZENTVTFGV1VOSlVVUkNOVEZxWTBwclFrMEtieXN2V1c1V1ZXaGhZMjVSTVROeU5HTnVhR2RDTVZac1JqbFpZVTQyYjFaMVowbG9RVkJSZEVaTk5tdzNPWEYzWTFwWWNGbElUWE5HYUhCbVNURjJNd3B6WkhoeVRIRjFja2RUYXpSV09IQXpUVUZ2UjBORGNVZFRUVFE1UWtGTlJFRXlaMEZOUjFWRFRWRkVlQzgwVWpFM1N6UlJXbXM0VVRGWU5HRmlUVVZTQ2pJNVRFWnBjRnBNVm1KdlZsWnlLMlZMTkNzMlVsQnVhVGxoUVV3eGFIbHJNRzAzVlV0QmFIRndUMFZEVFVWelpGWnZSbEpUUm5sQlFVdEhPV1puZVVNS1lVdzNNazkyTWtOM2JXczNkMFZ6TjBGTVdHNXhiQzh3UjBoMk9VNURWMFJaY0RaMk9EbGpVVFpsY0ZJcmR6MDlDaTB0TFMwdFJVNUVJRU5GVWxSSlJrbERRVlJGTFMwdExTMEsifX19fQ==",
          "integratedTime": 1666831464,
          "logIndex": 5944519,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/busybox/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/busybox",
      "githubWorkflowSha": "cd2f1e888f64dd8504760e368ea653a6d28417cb",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3333624305",
      "sha": "cd2f1e888f64dd8504760e368ea653a6d28417cb"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

