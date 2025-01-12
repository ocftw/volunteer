---
title: 志工數位證明
icon: material/card-account-details-star
---

# :identification_card: 志工數位證明

!!! example "持續修正中"

    發行與驗證的流程概念大致底定，驗證流程中所需的工具與操作還在建構中。

以往我們都是透過提供電子複印版本的時數證明，再請對方透過附檔或是印出紙本的方式呈現給需要證明的單位。現在我們將提供一個額外的證明方式，方便後續實現可串接與自動化驗證的可能。

<figure markdown="span">
    <a target="_blank" href="../assets/images/verify-flow.svg">
        <img src="../assets/images/verify-flow.svg"
            alt="簽署、發行與驗證流程"
            title="簽署、發行與驗證流程"
        >
    </a>
    <caption><span style="font-size: small;">簽署、發行與驗證流程</span></caption>
</figure>

流程說明：

1. OCF 透過金鑰簽署「時數證明文件」。
2. 志工夥伴取得已簽署數位文件後提供給需要證明的單位進行驗證。
3. 需驗證單位可自行下載公開金鑰後驗證文件是否正確。或選擇聯繫 OCF 協助驗證簽署文件。
4. 驗證方式也可透過後續建立的 API 服務自動化完成驗證。

## 簽署

```txt title="記載的資訊（基本）"
姓名：
時間：
工作內容：
總時數：
產生日期：
```

經過簽署後可以得到類似以下的證明憑證：

```txt title="簽署後的內容"
-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA512

姓名：
時間：
工作內容：
總時數：
產生日期：
-----BEGIN PGP SIGNATURE-----

iIcEARYKAC8WIQTUe4MbxRE9WD1AG4VSJY0TgQgiGAUCZ4PfOREcdm9sdW50ZWVy
QG9jZi50dwAKCRBSJY0TgQgiGNQUAQCVbtya4X/eeDHv2clxFO3fpoO+pJHm4HrV
2lj7RtyjKAD/XcvOhYAA7KoOs9m0hbd5yx+oT1IWS0Ggp1PCisThhwQ=
=6jUm
-----END PGP SIGNATURE-----
```

## 驗證

當需證明單位取得證明文件後，可以透過 PGP 公開金鑰來驗證文件的真實性。

```txt title="金鑰資訊"
pub   ed25519 2025-01-12 [SC]
      D47B831BC5113D583D401B8552258D1381082218
uid                      Open Culture Foundation Volunteer <volunteer@ocf.tw>
```

```txt title="公開金鑰"
-----BEGIN PGP PUBLIC KEY BLOCK-----

mDMEZ4PUMxYJKwYBBAHaRw8BAQdAvGaE0ASDhilrVKNkZxF/WFRxb+1T4rzWMSBi
ztr3JjW0NE9wZW4gQ3VsdHVyZSBGb3VuZGF0aW9uIFZvbHVudGVlciA8dm9sdW50
ZWVyQG9jZi50dz6IkgQTFgoAOxYhBNR7gxvFET1YPUAbhVIljROBCCIYBQJng9Qz
AhsDBQsJCAcCAiICBhUKCQgLAgQWAgMBAh4HAheAAAoJEFIljROBCCIYW5QA/i6y
KaNPCxwL4jOqwkON1rt+ObZ4rfTocP50nehQknTyAPY4bA5+K4ir/LhbnfwVOndH
YOjKcUFpuB//JGUczX4CuDgEZ4PUMxIKKwYBBAGXVQEFAQEHQN4pukx/ebDymZp7
oKJgnX1aheWa+GhkIJpqBP6XO31bAwEIB4h4BBgWCgAgFiEE1HuDG8URPVg9QBuF
UiWNE4EIIhgFAmeD1DMCGwwACgkQUiWNE4EIIhj6cwD+KUROWHmywmTam9KLF1tN
To9NF8OMNO7KK53IxEm818EBAN0yajOsY3IIPMGWCJfuQY7FvVXaf07vxIlfqlLZ
Gk0P
=/YKa
-----END PGP PUBLIC KEY BLOCK-----
```
