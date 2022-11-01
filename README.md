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
| `1.35.0-r27` `latest` | `sha256:e342687b2f0e2fd6f94ae38b6d085919fb9801c5adeaf9371edc2fa7a3f75cf4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:e342687b2f0e2fd6f94ae38b6d085919fb9801c5adeaf9371edc2fa7a3f75cf4) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `1.35.0-r25` | `sha256:62eae6a74ce7304c3ef45bdbce9f17f40929f9bdd0ec6da80c84ab4af2bb6057`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:62eae6a74ce7304c3ef45bdbce9f17f40929f9bdd0ec6da80c84ab4af2bb6057) | `386` `amd64` `arm64` `armv6` `armv7` `ppc64le` `riscv64` `s390x` |
| `1.35.0-r2-glibc` | `sha256:a76760a49c6966fa0516404736d7949299433d959ab9910d841e2e3a0f301d48`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:a76760a49c6966fa0516404736d7949299433d959ab9910d841e2e3a0f301d48) | `amd64` |
| `1.35.0-r3-glibc` | `sha256:f4949357be24fe779b6a7d8ff595ed3b9f27536f425835c99a59ebbe1d74c037`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:f4949357be24fe779b6a7d8ff595ed3b9f27536f425835c99a59ebbe1d74c037) | `amd64` |



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
        "docker-manifest-digest": "sha256:e342687b2f0e2fd6f94ae38b6d085919fb9801c5adeaf9371edc2fa7a3f75cf4"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "3f790d645f941efa907c71e9c404501f4f188a7f",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/busybox",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEQCICFXlGYmQA6VXiihsQwCeerx5ehMT+N9VvX8KRSseiGbAiA0YSQGEImUA0Blg6ZOaynOdw/iLbHIz39KbE6mBHY2Lg==",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiJjZjFmODgyMzg5MWE0YzhkNjk0NGRjZDMyOGUxYmU0MjliYTRlY2I3MDM4YmJhY2VjMTU4OTQ2NTM5MDI3MjdlIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUURvanNocVFKZEtnUDcxQy9oSzFuY2wzaWRQNWJZNWwzMDhyVGVteG9VR3BBSWdETUNOck00OUY5TmI5Z0U0L29aQ3lrVXNRVTVCK1VYUjNqYjR0VVcrcWdzPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnlla05EUVhwVFowRjNTVUpCWjBsVlprVmFhRWh2ZVdOcFYzWkZZblYyTWpoVWVtSmpWQzlvUzFkemQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVUVhoTlJFRXhUVVJSTUZkb1kwNU5ha2w0VFZSQmVFMUVSWGROUkZFd1YycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVYxY1cwMUsxVkJhbEpMVFc1VlNXMDRPVlJrUVVndlNYQjFaRE0wWlZGTlVGTnNTV3NLU1U5VlptWkxaa041TkRZeksycDVVMHd2TmpJM1VHNW9UWEZoYms5aE1IQXdVRFZ2V1V0a1lYcHhZbGR3TkU5YVVtRlBRMEZzVFhkblowcFFUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlUwVmxWakNtdE5jV1ZoVEZVeldtRkZXV0kyT0VKdk5uZzNkV0Z2ZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDJGUldVUldVakJTUVZGSUwwSkdPSGRZV1ZwaVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5U2pGak0yeHBZak5uZGt4dFpIQmtSMmd4V1drNU0ySXpTbkphYlhoMlpETk5kbU50Vm5OYVYwWjZXbE0xTlZsWE1YTlJTRXBzQ2xwdVRYWmhSMVpvV2toTmRtSlhSbkJpYWtFMVFtZHZja0puUlVWQldVOHZUVUZGUWtKRGRHOWtTRkozWTNwdmRrd3pVblpoTWxaMVRHMUdhbVJIYkhZS1ltNU5kVm95YkRCaFNGWnBaRmhPYkdOdFRuWmlibEpzWW01UmRWa3lPWFJOUWxsSFEybHpSMEZSVVVKbk56aDNRVkZKUlVOSVRtcGhSMVpyWkZkNGJBcE5SRmxIUTJselIwRlJVVUpuTnpoM1FWRk5SVXRFVG0xT2VtdDNXa1JaTUU1WFdUVk9SRVpzV20xRk5VMUVaR3BPZWtac1QxZE5NRTFFVVRGTlJFWnRDazVIV1hoUFJHaG9UakpaZDBoQldVdExkMWxDUWtGSFJIWjZRVUpDUVZGUFVUTktiRmxZVW14SlJrcHNZa2RXYUdNeVZYZEtkMWxMUzNkWlFrSkJSMFFLZG5wQlFrSlJVVnBaTW1ob1lWYzFibVJYUm5sYVF6RndZbGRHYmxwWVRYWlpibFo2WlZkS2RtVkVRV1JDWjI5eVFtZEZSVUZaVHk5TlFVVkhRa0U1ZVFwYVYxcDZUREpvYkZsWFVucE1NakZvWVZjMGQyZFpjMGREYVhOSFFWRlJRakZ1YTBOQ1FVbEZabEZTTjBGSWEwRmtkMFJrVUZSQ2NYaHpZMUpOYlUxYUNraG9lVnBhZW1ORGIydHdaWFZPTkRoeVppdElhVzVMUVV4NWJuVnFaMEZCUVZsUmQzRXhTME5CUVVGRlFYZENTVTFGV1VOSlVVTm5jRGxIVjBKelJXMEtaR3BqY1VkSEsyMVdZbGhDVjBvMVRuRkdPVlJ1UlZSRFEzcFFNMDR5WmtSRmQwbG9RVW9yUjNScVZreGlWblIyTTJSVlpYZFlLMnBCU1ZOaE1XSjNVZ3BTU1V0cGIwWjNaRkV2VDNoSU5rRlJUVUZ2UjBORGNVZFRUVFE1UWtGTlJFRXlhMEZOUjFsRFRWRkRZbUpYTjNONlFsVkRWRmhzYjBkV1NpOXZiMWR0Q2xKSFkyZHNjSGxEVVd0d2RrRXJaRzVIVjFNck1IUnhaVFZRT0RSUFFVTXhlVk00Wld3M2RuUjRVWGREVFZGRWRtdHpVV1YxYkZneWExUlhTREoyU3lzS09WUkpTVTVKTldka1MyVTJWV2N6YzAxdVduSnBUalkwWldwaGJGZE1lVlk1Y2tjdmFFdzNhRVZVV21sTmJFazlDaTB0TFMwdFJVNUVJRU5GVWxSSlJrbERRVlJGTFMwdExTMEsifX19fQ==",
          "integratedTime": 1667263864,
          "logIndex": 6259979,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/busybox/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/busybox",
      "githubWorkflowSha": "3f790d645f941efa907c71e9c404501f4f188a7f",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3365890856",
      "sha": "3f790d645f941efa907c71e9c404501f4f188a7f"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

