# AutoBuild-OpenWrt
[![LICENSE](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat&logo=github&label=LICENSE)](https://github.com/KJohn2q/OpenWrt-x86_64-firmware/blob/main/LICENSE)
![GitHub Stars](https://img.shields.io/github/stars/KJohn2q/OpenWrt-x86_64-firmware.svg?style=flat&logo=appveyor&label=Stars&logo=github)
![GitHub Forks](https://img.shields.io/github/forks/KJohn2q/OpenWrt-x86_64-firmware.svg?style=flat&logo=appveyor&label=Forks&logo=github)
![GitHub last commit](https://img.shields.io/github/last-commit/KJohn2q/OpenWrt-x86_64-firmware?label=Latest%20Commit&logo=github)

Build OpenWrt firware [Lean's OpenWrt](https://github.com/coolsnowwolf/lede) using GitHub Actions  
Hereby thank P3TERX for his amazing job: https://github.com/P3TERX/Actions-OpenWrt/  
Hereby thank KFERMercer for his amazing job: https://github.com/KFERMercer/OpenWrt-CI
Hereby thank esirplayground for his amazing job: https://github.com/esirplayground/AutoBuild-OpenWrt

## Usage

**1. Prerequisite**
  - Sign up for [GitHub Actions](https://github.com/features/actions/signup)
  - Fork [this GitHub repository](https://github.com/KJohn2q/OpenWrt-x86_64-firmware.git)
    
**2. Compile Firmware**
  - Click `[.github/workflows]` folder on the top of repo and you could see few workflow files, Each for one particular architecture(device).
  - Edit the workflow file you desire，uncomment push section 3 lines together and submit the commit.(Other 2 methods wait you to discover)
  - The build starts automatically. Progress can be viewed on the Actions page.
  - When the build is complete, click the `Artifacts` button in the upper right corner of the Actions page to download the binaries.
  - Default Web Admin IP: `192.168.5.1`, username `root`, no login password
  - Default Luci Theme: `luci-theme-argon`

**3. Sync Code**
  - Uncomment 'push-branches-master' 3 lines under **`On`** section and commit changes to let the script sync the code once for you.
  - Uncomment 'schedule-cron' 2 lines under **`On`** section and commit changes to let the script sync the code everyday on 3 am[UTC +8]