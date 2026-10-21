# Original server file scans

Security checks on the original Rust Legacy dedicated server files and client installer. The project keeps these files privately for compatibility testing. **None of them are distributed here.**

| | |
|---|---|
| **47** | files checked |
| **1** | antivirus detection: a proven false positive |
| **0** | malicious verdicts |
| **1** | file modified after signing, left out of testing |

- **The one detection is a false positive.** `rust_server.exe` (1 of 60 VirusTotal engines) is Unity 4.5.5's own Windows player. It is byte-identical to the copy in Unity's signed installer except for the icon images. [Details ↓](#rust_serverexe-what-triggers-the-detections)
- **One file was modified.** `VAC2.dll` in the server zip carries a Valve signature that no longer matches its contents. It belongs to the bundled offline Steam emulator, and its code is encrypted, so the change cannot be read. It is removed from the copy of the server used for testing. [Details ↓](#signatures-and-the-zips-vac2dll)
- **Coverage still open.** 18 files still need a VirusTotal lookup, because the site showed a CAPTCHA. 26 files have no Hybrid Analysis report yet. This page will be updated when those are done.

Checked on 2026-10-21:
- existing public reports on [VirusTotal](https://www.virustotal.com), [Hybrid Analysis](https://hybrid-analysis.com) and other free services, looked up by SHA-256;
- a byte-for-byte comparison with Unity's official, Authenticode-signed `UnitySetup-4.5.5.exe`;
- Windows Authenticode signature checks.

No file was uploaded or run for this page. Folder layout: `found-folder/` is a server folder as found, `server-zip/` is the server zip, and `installer/` is the client installer. Copies in the zip with the same SHA-256 as a `found-folder/` file share that file's row.

## Lookup totals

| | |
|---|---|
| **47** | files |
| **28** | VirusTotal clean |
| **1** | VirusTotal flagged |
| **0** | VirusTotal no report |
| **18** | VirusTotal not checked |
| **17** | Hybrid Analysis clean / no specific threat |
| **4** | Hybrid Analysis suspicious |
| **0** | Hybrid Analysis malicious |
| **26** | Hybrid Analysis no report |

VirusTotal columns show engines flagging / engines reporting. Hybrid Analysis columns show verdict, threat score and AV detection.

## Main programs

| File | Size | SHA-256 | VirusTotal | Hybrid Analysis | Reports |
|---|---:|---|---|---|---|
| `found-folder/rust_dedicated/rust_server.exe` | 11,546,112 | `7d80d881ad9b7d458c2bca85d550167609369cc35d213a69d6f4b5c828e307b7` | 1/60 (Jiangmin: TrojanSpy.Stealer.akaz), first submitted 2015-01-27 | Suspicious, score 38/100, AV 0/27 | [VT](https://www.virustotal.com/gui/file/7d80d881ad9b7d458c2bca85d550167609369cc35d213a69d6f4b5c828e307b7) · [HA](https://hybrid-analysis.com/sample/7d80d881ad9b7d458c2bca85d550167609369cc35d213a69d6f4b5c828e307b7) |
| `found-folder/rust_dedicated/rust_server_Data/Mono/mono.dll` | 2,101,760 | `755861af5a31f39f8a123d166768b970a45d42d456084f071543a5c8652cac05` | not checked | Clean, score 0/100, AV 0/25 | [VT](https://www.virustotal.com/gui/file/755861af5a31f39f8a123d166768b970a45d42d456084f071543a5c8652cac05) · [HA](https://hybrid-analysis.com/sample/755861af5a31f39f8a123d166768b970a45d42d456084f071543a5c8652cac05) |
| `found-folder/rust_dedicated/rust_server_Data/Plugins/librust.dll` | 854,016 | `37061a57100a02d30ac90933a6553712e00f9a90d7735c3ba59f5f758fcb3c7f` | not checked | no report | [VT](https://www.virustotal.com/gui/file/37061a57100a02d30ac90933a6553712e00f9a90d7735c3ba59f5f758fcb3c7f) |
| `installer/SetupRustLegacy.exe` | 381,433,701 | `a9d079eb552bb3926c6bf3868b636da27c8c08f9ce41d39986c07d6952c2c124` | not checked | no report | [VT](https://www.virustotal.com/gui/file/a9d079eb552bb3926c6bf3868b636da27c8c08f9ce41d39986c07d6952c2c124) |

## Steam and emulator DLLs

| File | Size | SHA-256 | VirusTotal | Hybrid Analysis | Reports |
|---|---:|---|---|---|---|
| `found-folder/rust_dedicated/steamclient.dll` | 7,209,896 | `0978263c467b965b4f13102edbb5028ed0cb6ac0ec22508c156326dedadec0be` | 0/72, first submitted 2013-09-15 | no report | [VT](https://www.virustotal.com/gui/file/0978263c467b965b4f13102edbb5028ed0cb6ac0ec22508c156326dedadec0be) |
| `found-folder/rust_dedicated/steam_api.dll` | 104,872 | `5a5bbe8409ca88f6c7e8ca498dc84b3511d6b017010ed89ad52a89e80492e4f5` | 0/72, first submitted 2013-05-06 | Suspicious, score 70/100, AV 0/28 | [VT](https://www.virustotal.com/gui/file/5a5bbe8409ca88f6c7e8ca498dc84b3511d6b017010ed89ad52a89e80492e4f5) · [HA](https://hybrid-analysis.com/sample/5a5bbe8409ca88f6c7e8ca498dc84b3511d6b017010ed89ad52a89e80492e4f5) |
| `found-folder/rust_dedicated/tier0_s.dll` | 243,112 | `e2d2bc5e7816f5c20e301cf1176eff69c55c3d300cea92fd5fef9bf5c02e42fb` | 0/72, first submitted 2013-09-16 | no report | [VT](https://www.virustotal.com/gui/file/e2d2bc5e7816f5c20e301cf1176eff69c55c3d300cea92fd5fef9bf5c02e42fb) |
| `found-folder/rust_dedicated/vstdlib_s.dll` | 219,560 | `317c24d7dbc990f48cf304ff096756f7a91a3993b0560aaf8a231169fe0254bc` | 0/72, first submitted 2013-09-16 | no report | [VT](https://www.virustotal.com/gui/file/317c24d7dbc990f48cf304ff096756f7a91a3993b0560aaf8a231169fe0254bc) |
| `server-zip/Steam.dll` | 181,248 | `5ec23db011e76038ce8a9ac37d9fc81377ed9f08ebe4dcc86e5062ba99dff3eb` | not checked | no report | [VT](https://www.virustotal.com/gui/file/5ec23db011e76038ce8a9ac37d9fc81377ed9f08ebe4dcc86e5062ba99dff3eb) |
| `server-zip/steam_api.dll` | 94,208 | `daa1c182eeb29a559b2a666d8655030f22b1db835196845274b0ddd2c03305de` | not checked | no report | [VT](https://www.virustotal.com/gui/file/daa1c182eeb29a559b2a666d8655030f22b1db835196845274b0ddd2c03305de) |
| `server-zip/steamclient.dll` | 382,976 | `936359a7f645bbc3422e7fcdca38be084fc9254628a1e9984cec1c3181018933` | not checked | no report | [VT](https://www.virustotal.com/gui/file/936359a7f645bbc3422e7fcdca38be084fc9254628a1e9984cec1c3181018933) |
| `server-zip/VAC2.dll` | 155,232 | `7b717fea39ce416bdb5e30e6de01053f6ea10912dd6df3884838082711ccba8a` | not checked | Suspicious, score 42/100, AV 0/27 | [VT](https://www.virustotal.com/gui/file/7b717fea39ce416bdb5e30e6de01053f6ea10912dd6df3884838082711ccba8a) · [HA](https://hybrid-analysis.com/sample/7b717fea39ce416bdb5e30e6de01053f6ea10912dd6df3884838082711ccba8a) |
| `server-zip/zlib1.dll` | 107,520 | `42967a768f341d9ce5174eb38a4d63754c3c41739e7d88f4e39cd7354c1fac71` | not checked | No specific threat, score 0/100, AV 0/25 | [VT](https://www.virustotal.com/gui/file/42967a768f341d9ce5174eb38a4d63754c3c41739e7d88f4e39cd7354c1fac71) · [HA](https://hybrid-analysis.com/sample/42967a768f341d9ce5174eb38a4d63754c3c41739e7d88f4e39cd7354c1fac71) |

## Game code

| File | Size | SHA-256 | VirusTotal | Hybrid Analysis | Reports |
|---|---:|---|---|---|---|
| `found-folder/rust_dedicated/rust_server_Data/Managed/Assembly-CSharp-firstpass.dll` | 80,896 | `200edd7562e162f90bb75cccbc6369c05c90cd54defd2e96065a21c28b46fa85` | 0/72, first submitted 2017-03-21 | no report | [VT](https://www.virustotal.com/gui/file/200edd7562e162f90bb75cccbc6369c05c90cd54defd2e96065a21c28b46fa85) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Assembly-CSharp.dll` | 3,190,784 | `ce0dd83271472454fc27ce137a9fa9d042b3a5f12fb26f1c7a67d61eea3acfbb` | 0/72, first submitted 2015-12-26 | no report | [VT](https://www.virustotal.com/gui/file/ce0dd83271472454fc27ce137a9fa9d042b3a5f12fb26f1c7a67d61eea3acfbb) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Assembly-UnityScript-firstpass.dll` | 83,456 | `0d358ee486aa2ccb509a7f94764a232c12e0450a5686704b474e18d7f33a8923` | 0/71, first submitted 2017-03-21 | no report | [VT](https://www.virustotal.com/gui/file/0d358ee486aa2ccb509a7f94764a232c12e0450a5686704b474e18d7f33a8923) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Assembly-UnityScript.dll` | 4,096 | `00daaa0710187353794306815653ae931863ab0d2d0c68d1ef90de3d635691f1` | 0/72, first submitted 2017-03-21 | no report | [VT](https://www.virustotal.com/gui/file/00daaa0710187353794306815653ae931863ab0d2d0c68d1ef90de3d635691f1) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/dfScriptLite.dll` | 55,808 | `90c29cf11cd5f966c29b31377a8e10e9e5c1f70ee2c3ee251356f96841fdc1e2` | 0/71, first submitted 2013-10-30 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/90c29cf11cd5f966c29b31377a8e10e9e5c1f70ee2c3ee251356f96841fdc1e2) · [HA](https://hybrid-analysis.com/sample/90c29cf11cd5f966c29b31377a8e10e9e5c1f70ee2c3ee251356f96841fdc1e2) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/EasyRoads3D.dll` | 156,160 | `a6190685790519bb1c12ba8ba8176ee1dba646fced76b83f9aa7c9fc43fa8070` | 0/72, first submitted 2013-07-06 | no report | [VT](https://www.virustotal.com/gui/file/a6190685790519bb1c12ba8ba8176ee1dba646fced76b83f9aa7c9fc43fa8070) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.Actor.dll` | 22,528 | `04a33d3db0f23b84abc6ceafccd4d9133d23fb88d775cf1208a4e1839dd40d65` | 0/72, first submitted 2014-02-18 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/04a33d3db0f23b84abc6ceafccd4d9133d23fb88d775cf1208a4e1839dd40d65) · [HA](https://hybrid-analysis.com/sample/04a33d3db0f23b84abc6ceafccd4d9133d23fb88d775cf1208a4e1839dd40d65) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.Cursor.dll` | 15,360 | `cb49ae57a63647b26762944cb9fceed4d055e85befc782790170f029fd7009d3` | 0/72, first submitted 2014-02-18 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/cb49ae57a63647b26762944cb9fceed4d055e85befc782790170f029fd7009d3) · [HA](https://hybrid-analysis.com/sample/cb49ae57a63647b26762944cb9fceed4d055e85befc782790170f029fd7009d3) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.Geometry.dll` | 74,752 | `249ccd49dc275be04078bd1d4125f9c136ef06fbf1e14c0261827161ddd6bd60` | 0/72, first submitted 2013-12-28 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/249ccd49dc275be04078bd1d4125f9c136ef06fbf1e14c0261827161ddd6bd60) · [HA](https://hybrid-analysis.com/sample/249ccd49dc275be04078bd1d4125f9c136ef06fbf1e14c0261827161ddd6bd60) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.HitBox.dll` | 95,232 | `825d8cfc1f26dacd2a43d3e818efb3622b6369f2c62241062c5bd1f65b8ca00e` | 0/72, first submitted 2014-02-18 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/825d8cfc1f26dacd2a43d3e818efb3622b6369f2c62241062c5bd1f65b8ca00e) · [HA](https://hybrid-analysis.com/sample/825d8cfc1f26dacd2a43d3e818efb3622b6369f2c62241062c5bd1f65b8ca00e) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.ID.dll` | 34,304 | `0ce8917f335df01fdd6b464529e0481af7366d63ec88930881462fb0945762fe` | 0/72, first submitted 2014-02-18 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/0ce8917f335df01fdd6b464529e0481af7366d63ec88930881462fb0945762fe) · [HA](https://hybrid-analysis.com/sample/0ce8917f335df01fdd6b464529e0481af7366d63ec88930881462fb0945762fe) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.MeshBatch.dll` | 94,208 | `d26f63dc160b783028c38ec382447da22a9f63a666387eca3c5428f3762be7b8` | 0/72, first submitted 2014-03-01 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/d26f63dc160b783028c38ec382447da22a9f63a666387eca3c5428f3762be7b8) · [HA](https://hybrid-analysis.com/sample/d26f63dc160b783028c38ec382447da22a9f63a666387eca3c5428f3762be7b8) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.Movement.dll` | 43,520 | `67db1cf9de5ee122b8b1b1a4f391ef4503c2a137404098189576cd546f5e88fc` | 0/72, first submitted 2014-02-18 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/67db1cf9de5ee122b8b1b1a4f391ef4503c2a137404098189576cd546f5e88fc) · [HA](https://hybrid-analysis.com/sample/67db1cf9de5ee122b8b1b1a4f391ef4503c2a137404098189576cd546f5e88fc) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.Prefetch.dll` | 8,704 | `f27ce4bd6d206ec329bd65ce66227dbfdc4f1192cca6c43aa6155d7a122d21d5` | 0/72, first submitted 2014-02-18 | no report | [VT](https://www.virustotal.com/gui/file/f27ce4bd6d206ec329bd65ce66227dbfdc4f1192cca6c43aa6155d7a122d21d5) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Facepunch.Utility.dll` | 126,464 | `73c1306e8f60241262cbe92905fe0e7013e9d8f76516bef3b7adad26d52e467b` | 0/72, first submitted 2014-02-18 | No specific threat, score 0/100, AV 0/1 | [VT](https://www.virustotal.com/gui/file/73c1306e8f60241262cbe92905fe0e7013e9d8f76516bef3b7adad26d52e467b) · [HA](https://hybrid-analysis.com/sample/73c1306e8f60241262cbe92905fe0e7013e9d8f76516bef3b7adad26d52e467b) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Google.ProtocolBuffers.dll` | 318,464 | `7b4974dd9bfe6b744ce9b27b65d879d95c0fbe9c200be4f6fe5794e4e5167cee` | 0/72, first submitted 2013-05-14 | No specific threat, score 0/100, AV 0/26 | [VT](https://www.virustotal.com/gui/file/7b4974dd9bfe6b744ce9b27b65d879d95c0fbe9c200be4f6fe5794e4e5167cee) · [HA](https://hybrid-analysis.com/sample/7b4974dd9bfe6b744ce9b27b65d879d95c0fbe9c200be4f6fe5794e4e5167cee) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Google.ProtocolBuffers.Serialization.dll` | 57,344 | `18881a540d03c3628bce8861d5134fa15391e272468bbe802ebbfc01b1bc956c` | 0/72, first submitted 2013-05-14 | No specific threat, score 0/100, AV 0/28 | [VT](https://www.virustotal.com/gui/file/18881a540d03c3628bce8861d5134fa15391e272468bbe802ebbfc01b1bc956c) · [HA](https://hybrid-analysis.com/sample/18881a540d03c3628bce8861d5134fa15391e272468bbe802ebbfc01b1bc956c) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/LitJSON.dll` | 83,968 | `ef47a9d3733f0061f1149f0cfbab583b5997ef04e611954700da2dcd4a0d978b` | 0/71, first submitted 2014-02-18 | no report | [VT](https://www.virustotal.com/gui/file/ef47a9d3733f0061f1149f0cfbab583b5997ef04e611954700da2dcd4a0d978b) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/uLink-cleaned.dll` | 394,240 | `58dcf24841d512bd6f72c840bee5330760d82050f3b3568db19045a6f960200b` | not checked | no report | [VT](https://www.virustotal.com/gui/file/58dcf24841d512bd6f72c840bee5330760d82050f3b3568db19045a6f960200b) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/uLink.dll` | 562,176 | `5b0539b30599d758582b7ce9740bf1616cbb7c539acf460c3a4169466afe4bdd` | not checked | no report | [VT](https://www.virustotal.com/gui/file/5b0539b30599d758582b7ce9740bf1616cbb7c539acf460c3a4169466afe4bdd) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/UnityEngine.Cloud.Analytics.dll` | 79,872 | `bd900a7429a259c5fa3a780ac844d760ed0866236d8ac2c958291bbd30c6f723` | not checked | no report | [VT](https://www.virustotal.com/gui/file/bd900a7429a259c5fa3a780ac844d760ed0866236d8ac2c958291bbd30c6f723) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/UnityEngine.Cloud.Analytics.Util.dll` | 4,096 | `73b646cb3376349579832b27cb685ce8c36723de5fcadc60d2c7768b83aa97d8` | not checked | No specific threat, score 0/100, AV 0/27 | [VT](https://www.virustotal.com/gui/file/73b646cb3376349579832b27cb685ce8c36723de5fcadc60d2c7768b83aa97d8) · [HA](https://hybrid-analysis.com/sample/73b646cb3376349579832b27cb685ce8c36723de5fcadc60d2c7768b83aa97d8) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/UnityEngine.dll` | 592,384 | `3366ad9f9806fe74b1c7cc98c6ee662322d47cd9d9d884895655329570a539eb` | not checked | Suspicious, score 35/100, AV 1/25 (Webroot SMD: Malware) | [VT](https://www.virustotal.com/gui/file/3366ad9f9806fe74b1c7cc98c6ee662322d47cd9d9d884895655329570a539eb) · [HA](https://hybrid-analysis.com/sample/3366ad9f9806fe74b1c7cc98c6ee662322d47cd9d9d884895655329570a539eb) |

## Mono / .NET runtime

| File | Size | SHA-256 | VirusTotal | Hybrid Analysis | Reports |
|---|---:|---|---|---|---|
| `found-folder/rust_dedicated/rust_server_Data/Managed/Boo.Lang.dll` | 126,976 | `754d695c07b28a7e5f3c55dfb1191aa04542356ca31e01346b2f6b5003baf9f5` | 0/69, first submitted 2014-10-10 | No specific threat, score 0/100, AV 0/25 | [VT](https://www.virustotal.com/gui/file/754d695c07b28a7e5f3c55dfb1191aa04542356ca31e01346b2f6b5003baf9f5) · [HA](https://hybrid-analysis.com/sample/754d695c07b28a7e5f3c55dfb1191aa04542356ca31e01346b2f6b5003baf9f5) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Mono.Posix.dll` | 184,320 | `b6d2eac30623b12414b30f38ea785d0a8e067f98659df092a9947227b18121eb` | 0/69, first submitted 2014-10-11 | no report | [VT](https://www.virustotal.com/gui/file/b6d2eac30623b12414b30f38ea785d0a8e067f98659df092a9947227b18121eb) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/Mono.Security.dll` | 294,400 | `ce647058617eb548fe9867a8bf3cd4dc95e79d3af1c64f0de5005489935cbe35` | 0/65, first submitted 2014-10-11 | no report | [VT](https://www.virustotal.com/gui/file/ce647058617eb548fe9867a8bf3cd4dc95e79d3af1c64f0de5005489935cbe35) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/mscorlib.dll` | 2,590,208 | `ff0985ac88b62e93e81748b1b312c1703e4dec4f94aa6a7d232a9776385811e7` | 0/60, first submitted 2014-10-11 | no report | [VT](https://www.virustotal.com/gui/file/ff0985ac88b62e93e81748b1b312c1703e4dec4f94aa6a7d232a9776385811e7) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/System.Configuration.dll` | 124,928 | `f5ebfeee825c3c55fdd5eaf991687556b100cb198f5a51c3139f44a61e39bf0b` | not checked | no report | [VT](https://www.virustotal.com/gui/file/f5ebfeee825c3c55fdd5eaf991687556b100cb198f5a51c3139f44a61e39bf0b) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/System.Core.dll` | 299,520 | `dbeaa6b35a44f1acd53876c3a18e68614fd7726f02b2aba71937ce5958bd80d4` | 0/68, first submitted 2014-10-11 | no report | [VT](https://www.virustotal.com/gui/file/dbeaa6b35a44f1acd53876c3a18e68614fd7726f02b2aba71937ce5958bd80d4) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/System.dll` | 1,678,848 | `5b9929d1ed25c0fb2144f655dc71933fca3c44dc8ed70012c36b046d7988de8d` | not checked | no report | [VT](https://www.virustotal.com/gui/file/5b9929d1ed25c0fb2144f655dc71933fca3c44dc8ed70012c36b046d7988de8d) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/System.Security.dll` | 135,168 | `9ea75cff42d78369aa559473159c82e6f2a7bfe884ca0034cc89fe776981f16b` | not checked | no report | [VT](https://www.virustotal.com/gui/file/9ea75cff42d78369aa559473159c82e6f2a7bfe884ca0034cc89fe776981f16b) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/System.Xml.dll` | 1,270,272 | `14dc8f5dfd721834387ece328b83b5b1fe988506e61700904a243113ef44ea16` | not checked | no report | [VT](https://www.virustotal.com/gui/file/14dc8f5dfd721834387ece328b83b5b1fe988506e61700904a243113ef44ea16) |
| `found-folder/rust_dedicated/rust_server_Data/Managed/UnityScript.Lang.dll` | 14,336 | `628dda1e48ce5be6c2aa293a1cd40fde8ddac1d43b417341a7d5f2962b9aef93` | not checked | No specific threat, score 0/100, AV 0/28 | [VT](https://www.virustotal.com/gui/file/628dda1e48ce5be6c2aa293a1cd40fde8ddac1d43b417341a7d5f2962b9aef93) · [HA](https://hybrid-analysis.com/sample/628dda1e48ce5be6c2aa293a1cd40fde8ddac1d43b417341a7d5f2962b9aef93) |

## Scripts

| File | Size | SHA-256 | VirusTotal | Hybrid Analysis | Reports |
|---|---:|---|---|---|---|
| `found-folder/rust_dedicated/Run Server.bat` | 127 | `d0a167c5093006290a1386d919ac5028a86a407284a62be2aecdeec48ab3a2fc` | 0/59, first submitted 2023-03-19 | No specific threat, score 0/100, AV 0/27 | [VT](https://www.virustotal.com/gui/file/d0a167c5093006290a1386d919ac5028a86a407284a62be2aecdeec48ab3a2fc) · [HA](https://hybrid-analysis.com/sample/d0a167c5093006290a1386d919ac5028a86a407284a62be2aecdeec48ab3a2fc) |

## Notes

- **VirusTotal coverage.** 29 of 47 files were looked up. VirusTotal then showed a CAPTCHA, so the remaining 18 files are marked "not checked" and still need a lookup.
- **rust_server.exe.** 1 of 60 VirusTotal engines (Jiangmin) labels it `TrojanSpy.Stealer.akaz`; the other engines report it as undetected. Hybrid Analysis rates it suspicious (38/100) because of a CrowdStrike MalQuery database match, with 0 of 27 AV engines flagging it. Both are explained below: the file is Unity's own engine player.
- **UnityEngine.dll.** 1 of 25 AV engines on Hybrid Analysis (Webroot SMD) labels it `Malware`; Hybrid Analysis rates it suspicious (35/100).
- **steam_api.dll (104,872 bytes, `ValveAPI.dll` in the zip) and VAC2.dll.** Hybrid Analysis rates them suspicious (70/100 and 42/100) from behaviour indicators, with 0 current AV detections. `steam_api.dll` carries a valid Valve signature; `VAC2.dll` does not (see the last section).
- **LumaEmu offline Steam emulator.** The zip-only files `Steam.dll`, the 382,976-byte `steamclient.dll`, the 94,208-byte `steam_api.dll`, `VAC2.dll` and `zlib1.dll` belong to the LumaEmu offline Steam emulator. Files of this kind are commonly labelled HackTool, Crack or Riskware by antivirus engines.
- **uLink-cleaned.dll** exists only in `found-folder/`; it is not in the server zip.
- **Pending.** Files with no public report on a site still need to be uploaded there. Hybrid Analysis sandbox uploads are pending.

## rust_server.exe: what triggers the detections

`rust_server.exe` is the only file with an antivirus detection (1 of 60 engines on VirusTotal). It was compared byte for byte with Unity's own Windows player from the official Unity 4.5.5 installer. That installer is `UnitySetup-4.5.5.exe` from download.unity3d.com: 1,310,170,560 bytes, with a valid Authenticode signature from Unity Technologies ApS.

| | |
|---|---|
| **11,546,112** | bytes: same size as Unity's `win32_nondevelopment/player_win.exe` |
| **0** | differing bytes in the headers, code and data sections (`.text`, `.rdata`, `.data`, `.trace`, `_RDATA`, `.reloc`) |
| **483,483** | differing bytes, all inside the 9 icon images in `.rsrc` |
| **0** | differing bytes outside the icon images |

Unity's build process copies `player_win.exe`, renames it after the game and replaces its icon with the game's icon. Apart from the icon pixels, `rust_server.exe` is Unity's unmodified, signed-installer player. Every program instruction in it is Unity's.

The same check matched these files byte for byte to files in the same Unity installer:
- `mono.dll` = `Data/Mono/bin/mono.dll`
- `UnityEngine.dll` = `.../win32_nondevelopment/Data/Managed/UnityEngine.dll` (flagged by 1 of 25 engines on Hybrid Analysis: Webroot SMD, "Malware")
- `mscorlib.dll`, `System.dll`, `System.Core.dll`, `System.Xml.dll`, `System.Security.dll`, `System.Configuration.dll`, `Mono.Posix.dll`, `Mono.Security.dll`, `Boo.Lang.dll`, `UnityScript.Lang.dll` = `Data/Mono/lib/mono/2.0/`

What each warning points at, all Unity 4.5.5 engine code:

| Warning | Cause in the file |
|---|---|
| Jiangmin `TrojanSpy.Stealer.akaz` | A generic single-engine signature. It is also seen on unrelated old game executables. The file has been seen inside several game-server archives and inside one 2016 wrapper EXE that 42 of 54 engines flag. That is a likely way this engine learned the bytes. No sandbox run showed stealer behaviour. |
| Hybrid Analysis "suspicious" 38/100 | The report says it enforced the verdict from a CrowdStrike MalQuery database match, not from behaviour. 0 of 27 antivirus engines detect it. |
| Possible debugger checks | Unity's crash handler: `IsDebuggerPresent`, `dbghelp.dll`, "You can attach a debugger now if you want". |
| Registry key monitor | Windows' own Winsock catalogue watches, which are set in any program that uses networking. |
| WMI references | Unity's hardware survey reads `Win32_Processor`, `Win32_VideoController`, `Win32_BIOS` and similar classes. |
| Unusual PE section name | `.trace` and `_RDATA`. Both sections are byte-identical in Unity's official player. |
| Suspicious API imports | Engine features: input (`GetAsyncKeyState`), clipboard (GUI text fields), `ShellExecuteW`/`rundll32 url.dll` (`Application.OpenURL`), Winsock (Unity networking), CryptoAPI (signature checks). |
| IP `83.221.146.11` | A constant in `GetLocalIP`. Unity connects a UDP socket to it only to learn which local network interface would be used. A UDP connect sends no packets. |

Behaviour seen in public sandbox runs: the program only showed Unity's "Data folder not found" dialog and exited. There were no dropped files, no persistence, and no network traffic from the sample.

Network addresses built into the engine: `stats.unity3d.com/HWStats.cgi` (Unity's hardware survey), `masterserver.unity3d.com` and `facilitator.unity3d.com` (Unity's legacy networking, used only when a game asks for it).

Other files:
- `uLink-cleaned.dll` (in `found-folder/` only) is a de-obfuscated copy of `uLink.dll`, with the same assembly name and the same strings. It looks like a modder's leftover. The server loads `uLink.dll`.
- `Assembly-*.dll` (the game's own code) differs from Unity's template files of the same name, as expected.
- The zip's `zlib1.dll` differs from Unity's copy of that name.
- Not covered by this check: the files that are not Unity's: Facepunch's `librust.dll` and managed DLLs, uLink, the Steam DLLs and the zip's LumaEmu emulator.

## Signatures and the zip's VAC2.dll

Authenticode signatures, checked with Windows' own `Get-AuthenticodeSignature`:

| File | Signature |
|---|---|
| `found-folder/` `steamclient.dll`, `steam_api.dll`, `tier0_s.dll`, `vstdlib_s.dll` | **Valid**, signed by Valve |
| `server-zip/VAC2.dll` | Valve certificate, but **HashMismatch**: the file was changed after Valve signed it |
| every other file | not signed (normal for Unity 4 builds and these libraries) |

The Valve signature explains Hybrid Analysis's "suspicious" score for `steam_api.dll`: it is Valve's own file.

`VAC2.dll` (155,232 bytes) is Valve's 2010 VAC module:
- Its signed SHA-1 Authenticode digest is `6f7e964f5c6eb5076d5ec215288055f09ac9e77a`; the file now hashes to `38b0011cd5c8dfaea20a4b5ad63c2a6305f9f665`.
- Its PE checksum no longer matches either (stored `0x2f710`, actual `0x2beb8`).
- Its code section is encrypted. The emulator's `steamclient.dll` loads it, calls `Startup3` and decrypts its `.text` section at run time, so the exact change cannot be read from the file.
- It imports `OpenProcess` and `ReadProcessMemory`, as VAC's process scanning does.

No unmodified copy is published to compare against. It is the one file in the package whose contents cannot be verified, so the test setup removes it from the server copy that runs.

The zip's offline Steam emulator (LumaEmu) ships with `Master = 1` (Valve master-server heartbeats) and `UnlockDLC = 1` (online DLC lookups). The test setup turns both off.
