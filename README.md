# PPPwn_MAC_ARM64
Run PPPwn on Apple Devices (Mac) with ARM64

## Requirements
- A Mac with an Ethernet port
- Ethernet cable
- MacOS
- Wireshark installed
  Before you install Wireshark, run this command:
  ```sh
  sudo xattr -rd com.apple.quarantine "drag pppwn executable here, DO NOT DRAG PPPwn folder"
  ```
- "SIP" is enabled. Open Terminal and run this command to make sure:
  ```sh
  csrutil status
  ```
  If SIP is enabled, the message will read “**System Integrity Protection status: enabled.**”

## Usage

DO NOT RUN the exploit just yet (don't press Enter yet) but prepare this command on your prompt (see ifconfig for the correct interface):

```sh
sudo ./pppwn --interface en9 --fw 1100 --stage1 ./stage1_1100.bin --stage2 ./stage2_1100.bin --auto-retry
```

***
With :heart: from [akbarhabiby](https://akbar.hk)