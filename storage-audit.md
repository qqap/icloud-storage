# iCloud Storage Audit

Scanned on 2026-10-23 using `icloud-pp-cli` (local SQLite reads, no network).

## Tool Used

```bash
# Install Go
mkdir -p ~/go-sdk && tar -C ~/go-sdk -xzf go1.23.4.darwin-arm64.tar.gz
GOPATH=~/go-path ~/go-sdk/go/bin/go install github.com/matysanchez/icloudcli/cmd/icloud-pp-cli@latest

# Run audit
~/go-path/bin/icloud-pp-cli drive status --json
~/go-path/bin/icloud-pp-cli drive usage --json
```

## Per-App Breakdown

| App | Files | Downloaded | Cloud-Only |
|-----|-------|-----------|-----------|
| iCloud Drive | 553 | 756MB | 1.4GB |
| WhatsApp | 15 | 0MB | 924MB |
| Ulysses | 15 | 214KB | ~4KB |
| Mail | 1 | 0 | ~3KB |

## iCloud Drive — File-Level Findings

### Deleted (safe — all sideloading builds)

| File | Size |
|------|------|
| `X-10.85-BHTwitter.ipa` | 166MB |
| `BHTwitter-sideloaded.ipa` | 121MB |
| `uYouPlus_19.49.3-3.0.4.ipa` | 116MB |
| `uYouPlus_18.08.1_2.3.1.ipa` | 106MB |
| `z8jg5n.ipa` × 3 | 99MB × 3 |
| `SpotilifeC.v1.2.3.ipa` | 47MB |
| `XinaA12.1.1.7.2.ipa` | 35MB |
| `Hot Tub-2.1.1(17).ipa` | 29MB |
| `balatro-base.ipa` | 18MB |
| `app.acutecalc.Acute_1.0.14.ipa` | 13MB |
| `com.openai.chat.ipa` | 7MB |
| **Total freed** | **~1.0GB** |

### Still Present — Action Needed

| File | Size | Verdict |
|------|------|---------|
| `output.mp4` | 362MB | Likely temp export — check before deleting |
| `output.zip` | 360MB | Same video zipped — delete if mp4 confirmed |
| `Rowen Mallare - To My Wife.webm` | 94MB | Personal video — keep if wanted |
| Hex `.zip` + GoPro JPG folder | 61MB | GoPro export — already backed up? |
| `AmazonPhotos.zip` + 15 JPGs | 33MB | Already in Amazon Photos? |
| `uYouPlus_19.49.3_3.0.4.zip` | 118MB | Sideloading zip — delete |
| `skydiving honolulu.pdf` | 10MB | Junk save — delete |
| `Costco breaks ground.pdf` | 8MB | Junk save — delete |
| `Screenshot 2025-01-11.pdf` | 8MB | Junk save — delete |
| `arcexport/` folder | ~10MB | Old browser history exports — delete |
| Duplicate resume PDFs | ~1MB | Keep one, delete rest |

### Additional Safe Deletes Remaining: ~600MB+
