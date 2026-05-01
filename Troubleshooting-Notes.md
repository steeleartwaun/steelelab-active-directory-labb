## Troubleshooting & Lessons Learned

### Domain Controller Lost Internet After Static IP
**Issue:** After setting a static IP, the server lost internet connectivity.

**Cause:** Incorrect subnet and gateway configuration.

**Resolution:** Updated network settings to match VMware NAT:
- IP: 192.168.190.10
- Gateway: 192.168.190.2
- DNS: 127.0.0.1

---

### FS1 Could Not Reach Domain Controller
**Issue:** FS1 could not ping the Domain Controller.

**Cause:** Domain Controller was powered off.

**Resolution:** Powered DC back on and verified connectivity using ping.

---

### Domain Login Issues
**Issue:** Unable to log in using steelelab\Administrator.

**Cause:** Authentication format mismatch.

**Resolution:** Successfully logged in using:
Administrator@steelelab.local

---

### IIS index.html Missing
**Issue:** Default index.html file was not present after IIS installation.

**Resolution:** Created index.html manually in:
C:\inetpub\wwwroot