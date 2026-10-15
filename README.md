# EDUP-RT2980-Fix
English

**Title: EDUP RT2980 Packet Injection Not Working? Flash ImmortalWrt & Fix It!**

If you own an **EDUP RT2980 (MT7981 chip)** and can't get Packet Injection or Deauth attacks to work, don't blame the hardware! The issue is with the official OpenWrt firmware.

**✅ The Fix: Switch to ImmortalWrt**

**1. How to Enter U-Boot Recovery (Critical)**
* Power off the router, unplug it.
* Hold the **Reset** button, then plug the power back in.
* If that doesn't work, hold **Reset + Mesh/WPS** together while plugging in power.
* Set your PC's IP to `192.168.1.2` and open **`http://192.168.1.1`** in your browser. You should see the U-Boot WebUI.

**2. Download the Firmware**    https://firmware-selector.immortalwrt.org/
* Download ImmortalWrt for the **CLT-R30B1** board (same board as RT2980) from the official ImmortalWrt website or GitHub. Look for `clt-r30b1-112m-squashfs-sysupgrade.bin` (for the 112M version).

**3. Flash via U-Boot**
* In the U-Boot WebUI, upload the `.bin` file and click Flash.
* Wait for the reboot. The router will now run ImmortalWrt with LuCI WebUI.

**🎯 Results After Flashing ImmortalWrt**
* ✅ Monitor Mode works reliably
* ✅ Handshake capture works
* ✅ Deauth attacks (kicking devices off) work perfectly!

**⚠️ Disclaimer:** Only perform Deauth attacks on your own network or in a lab environment. Attacking others' networks is illegal.

### 🇹🇭 ภาษาไทย

**หัวข้อ: แก้ปัญหา EDUP RT2980 ยิง Packet Injection ไม่ออก? ลง ImmortalWrt จบทุกปัญหา!**

สำหรับใครที่ใช้ **EDUP RT2980 (ชิป MT7981)** แล้วเจอปัญหาเปิด Monitor Mode ได้แต่ยิง Deauth ไม่ออก หรือ Packet Injection ไม่ทำงาน อย่าเพิ่งคิดว่าฮาร์ดแวร์มีปัญหา! ปัญหานี้เกิดจากเฟิร์มแวร์ OpenWrt เวอร์ชันทางการครับ

**✅ วิธีแก้คือเปลี่ยนมาใช้ ImmortalWrt**

**1. วิธีเข้า U-Boot Recovery (สำคัญมาก)**
* ปิดเราเตอร์ ถอดปลั๊กออก
* กดปุ่ม **Reset** ค้างไว้ แล้วเสียบสายไฟเข้าไป
* ถ้าไม่ติด ให้ลองกด **Reset + Mesh/WPS** พร้อมกันแล้วเสียบไฟ
* รอไฟสถานะกะพริบ แล้วตั้งค่า IP คอมพิวเตอร์เป็น `192.168.1.2` เปิดเบราว์เซอร์ไปที่ **`http://192.168.1.1`** จะเจอหน้า U-Boot WebUI

**2. ดาวน์โหลดเฟิร์มแวร์**  https://firmware-selector.immortalwrt.org/
* โหลด ImmortalWrt สำหรับบอร์ด **CLT-R30B1** (บอร์ดเดียวกับ RT2980) จากเว็บไซต์ทางการของ ImmortalWrt หรือ GitHub (ค้นหา `clt-r30b1-112m-squashfs-sysupgrade.bin` สำหรับเวอร์ชัน 112M)

**3. แฟลชผ่าน U-Boot**
* ในหน้า U-Boot WebUI ให้อัปโหลดไฟล์ `.bin` ที่ดาวน์โหลดมา แล้วกด Flash
* รอระบบรีบูต เราเตอร์จะรัน ImmortalWrt พร้อม LuCI WebUI

**🎯 ผลลัพธ์หลังลง ImmortalWrt**
* ✅ เปิด Monitor Mode ได้เสถียร
* ✅ จับ Handshake ได้
* ✅ ยิง Deauth เตะอุปกรณ์ออกได้จริง!

**⚠️ คำเตือน:** การยิง Deauth ควรใช้กับเครือข่ายของตัวเองหรือในห้องแล็บเท่านั้น การโจมตีเครือข่ายผู้อื่นผิดกฎหมาย

---
