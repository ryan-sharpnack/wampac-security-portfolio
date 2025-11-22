# Week 1 Learning Log

**Date:** November 16-17, 2025  
**Total Hours:** 10-12  
**Focus:** Lab environment setup, career planning, and networking fundamentals

---

## What I Did

### GitHub Portfolio & Career Planning
- Created comprehensive GitHub portfolio structure (`wampac-security-portfolio`)
- Established 5-phase project organization (Purple Team, ICS/OT & Grid Foundations, WAMPAC Specialization, Advanced Detection & Response, Comprehensive Assessment)
- Researched and documented WAMPAC security specialization
- Developed career roadmap targeting WAMPAC and electric grid security roles

### Virtual Machine Setup
Built complete 3-VM cybersecurity lab in VirtualBox:

**Kali Linux (Attacker):**
- Imported pre-built VirtualBox image
- Configured dual-adapter networking (Host-only + NAT)
- Static IP for isolation and DHCP on NAT (internet)
- Updated system and verified connectivity
- Snapshot: "Network Configured - Lab Ready"

**Ubuntu Server 22.04 (Defender/SIEM):**
- Full installation from ISO
- Configured Netplan for dual-adapter static networking
- Static IP and DHCP on NAT (internet)
- System updated and ready for Splunk installation
- Snapshot: "Network Configured - Pre-Splunk"

**Windows 11 Enterprise (Target):**
- Full installation from evaluation ISO
- Configured static IP
- Created test users (testuser1, testuser2, admin1) for credential attack labs
- Disabled Windows Defender and configured firewall for lab use
- Snapshot: "Network Configured - Lab Ready"

### Networking Configuration
- Created isolated Host-only network
- DHCP disabled - all VMs use static IPs for predictability
- Implemented dual-adapter strategy:
  - Adapter 1 (Host-only): Lab network isolation
  - Adapter 2 (NAT): Internet access for updates/tools (Kali and Ubuntu only)
- Verified full connectivity between all VMs
- Windows 11 properly isolated (no internet access by design)

---

## What I Learned

### Technical Skills

**VirtualBox Management:**
- VM creation, configuration, and resource allocation
- Network adapter types (Host-only, NAT, bridged)
- Snapshot strategy for lab restoration points
- Resource management within 16GB RAM constraint

**Linux Networking:**
- `/etc/network/interfaces` configuration (Kali/Debian)
- Netplan YAML syntax (Ubuntu Server)
- Static vs. DHCP networking in lab environments
- Network verification commands (`ip addr show`, `ip route show`, `ping`)

**Windows Configuration:**
- Manual IP configuration via Settings and netsh
- Windows Firewall management for lab environments
- User account creation via `net user` commands
- Understanding APIPA addresses (169.254.x.x) and why they appear

**Routing Tables:**
- Understanding `ip route show` output
- Default routes, directly connected networks, and metrics
- How routing decisions are made (most specific route wins)
- Why separate adapters allow both lab isolation AND internet access

### Career Insights

**Purple Team Methodology:**
- Purple team skills remain valuable throughout entire career, not just entry-level
- Offensive understanding makes defensive work exponentially better
- WAMPAC security roles leverage purple team thinking at all levels
- Attack → Detection → Documentation cycle is the foundation of all security work

**Networking Strategy:**
- My strengths: Technical depth, written communication, systematic thinking
- Portfolio + blog posts + LinkedIn = passive networking that works for me

**WAMPAC Security Specialization:**
- WAMPAC security = strategic specialization within electric grid operations
- Nation-state adversaries target synchrophasor systems (high-impact)
- Purple team + WAMPAC + Grid security = rare, high-value skillset
- Career progression: SOC → ICS Security → WAMPAC Specialist → Leadership
- Long-term path to Grid Security leadership roles is achievable

---

## Challenges & Solutions

### Challenge 1: Kali Linux Update Hanging
**Problem:** PostgreSQL database initialization appeared frozen during `apt upgrade`  
**Solution:** Patience - large database operations take time (15+ minutes)  
**Lesson:** Not every pause is a freeze; check system resources before assuming failure

### Challenge 2: Windows 11 Forcing Online Setup
**Problem:** OOBE (Out of Box Experience) demanded internet connection  
**Solution:** `Shift + F10` → `OOBE\BYPASSNRO` command enabled offline setup  
**Lesson:** Modern OSes have workarounds; research before assuming limitation

### Challenge 3: Windows 11 Getting APIPA Address (169.254.x.x)
**Problem:** Windows couldn't find DHCP server, self-assigned useless IP  
**Solution:** Manual static IP configuration via Settings GUI or netsh  
**Lesson:** When DHCP is disabled (by design), static configuration is required

### Challenge 4: Networking Event Discomfort
**Problem:** Attended local cybersecurity meetup, felt too uncomfortable, left early  
**Solution:** Recognized this approach doesn't play to my strengths  
**Lesson:** Portfolio-driven discovery (passive networking) is more sustainable for me  
**Action:** Focus energy on technical work and written content, not forced socializing

---

## Key Takeaways

### Technical
1. **Static IPs are essential for labs** - DHCP causes unpredictable addressing
2. **Dual-adapter strategy works perfectly** - Lab isolation + internet access when needed
3. **Snapshots are critical** - Restoration points before major changes
4. **Resource planning matters** - 2-3 concurrent VMs max with 16GB RAM
5. **Configuration files ensure persistence** - Manual commands are temporary

### Career/Personal
1. **Purple team is a lifelong advantage** - Not just an entry-level skillset
2. **WAMPAC security is the right specialization** - Strategic, high-impact, well-compensated
3. **Portfolio quality > networking quantity** - Let work speak for itself
4. **Written communication is a strength** - Blog posts, documentation, GitHub are my networking
5. **Self-awareness enables strategic decisions** - Understanding personal strengths leads to better choices

### Process
1. **One step at a time works** - Break complex tasks into manageable pieces
2. **Documentation while building = better learning** - Writing reinforces understanding
3. **Asking "why" deepens knowledge** - Understanding routing tables, not just configuring them
4. **Combining days in log when needed** - Flexibility in tracking, focus on content quality
5. **Consistent progress > speed** - 10-12 hours over 2 days built entire lab foundation

---

## Portfolio Progress

### Completed
- ✅ GitHub repository structure (`wampac-security-portfolio`)
- ✅ Phase 1-5 folder organization
- ✅ WAMPAC security specialization planning
- ✅ 40-week pathway structure
- ✅ Learning log system initiated

### In Progress
- Lab infrastructure documentation (network diagrams, IP schemes)
- Network verification documentation

### Next
- Install Splunk on Ubuntu Server VM
- Configure Windows 11 log forwarding to Splunk
- Complete Phase 1, Project 1: Lab Infrastructure Documentation

---

## Resources Used

### Documentation
- VirtualBox User Manual (networking, snapshots)
- Ubuntu Server Installation Guide
- Netplan documentation
- Windows 11 Enterprise Evaluation setup guides

### Learning
- Professor Messer's Network+ videos (TCP/IP fundamentals)
- Routing table explanations (understanding `ip route show`)
- Career research: WAMPAC security roles, electric grid operations

### Tools
- VirtualBox 7.x (hypervisor)
- Kali Linux 2024.3 (pre-built image)
- Ubuntu Server 22.04 LTS (ISO)
- Windows 11 Enterprise Evaluation (ISO)

---

## Next Steps (Week 1, Days 3-4)

### Immediate (Tomorrow)
1. ✅ Install Splunk Free on Ubuntu Server VM (1 hour)
2. ✅ Configure Splunk web interface and create admin account (15 min)
3. ✅ Install Splunk Universal Forwarder on Windows 11 (30 min)
4. ✅ Configure Windows Security Event Log forwarding to Splunk (30 min)
5. ✅ Verify logs appearing in Splunk (test log pipeline) (15 min)

### This Week
1. Complete Phase 1, Project 1: Lab Infrastructure Documentation
   - Network topology diagram (draw.io)
   - Full setup guide (reproducible by others)
   - Configuration reference (IPs, credentials, settings)
   - Commit to GitHub

2. Begin Phase 1, Project 2: Credential Attack Detection
   - Execute password spraying attack from Kali → Windows 11
   - Capture Windows Event Logs
   - Build Splunk detection rule
   - Document attack → detection cycle

### This Month (November)
- Complete Phase 1 Projects 1-2 (lab setup + credential attacks)
- Write blog post announcing WAMPAC security specialization
- Publish to Beehiiv newsletter
- Update LinkedIn and GitHub with WAMPAC focus

---

## Reflections

### What Went Well
- **Systematic approach paid off** - Breaking down VM setup into discrete steps prevented overwhelm
- **Asking questions when confused** - Understanding routing tables deeply vs. blindly following instructions
- **Recognizing personal limits** - Leaving the networking event wasn't failure; it was self-awareness
- **Portfolio-first mindset** - Every configuration is documented, building proof of capability

### What I'll Improve
- **Time estimation** - Lab setup took longer than expected (10-12 hours vs. planned 6-8)
- **Windows 11 RAM allocation** - Started with 4GB, should have gone with 6GB initially
- **Snapshot timing** - Take snapshots BEFORE and AFTER major changes, not just after

### Mindset Shifts
- **Purple team is permanent, not temporary** - This isn't just Phase 1 training; it's career-long methodology
- **Portfolio > networking events** - Technical depth and documentation are my competitive advantages
- **WAMPAC specialization clarity** - Sub-specialization is clear: synchrophasor protocols and grid operations security
- **Patience with complexity** - Networking, VMs, career planning - all complex, all learnable with systematic effort

---

## Metrics

**Time Breakdown:**
- VM setup and configuration: 6 hours
- Network configuration and troubleshooting: 2 hours
- Documentation and learning logs: 1 hour
- Career research and planning: 2 hours
- Networking event (unsuccessful): 1 hour

**GitHub Activity:**
- Repository created and renamed to `wampac-security-portfolio`
- Initial commits: 5+
- Portfolio structure established
- Learning log system initiated

**Technical Artifacts Created:**
- 3 fully configured VMs
- 3 VM snapshots (restoration points)
- Network configuration files (persistent)
- IP address scheme documentation
- Connectivity verification matrix

---

## Commitment Check

**Original Goal:** Complete 40-week WAMPAC specialization pathway, build portfolio, land WAMPAC/grid security role

**Progress:** On track. Foundation established. Week 1 exceeded expectations for setup.

**Energy Level:** High. Motivated by clarity on WAMPAC security specialization path.

**Sustainability:** Pace is manageable. 10-12 hours over 2 days is sustainable long-term.

**Next Milestone:** Splunk operational + first attack/detection project documented by end of Week 1.

---

**Status: Week 1 Days 1-2 COMPLETE ✅**  
**Lab Foundation: OPERATIONAL ✅**  
**Ready for Phase 1 Labs: YES ✅**

---

**Date:** November 18-19, 2025
**Focus:** Career research

---

**Date:** November 20, 2025
**Focus:** Troubleshot Home Lab Network issues, installed openssh-server, wireshark, tshark, suricata, and Splunk on Ubuntu Server, and installed Splunk Universal Forwarder on Windows 11. Phase 1 Project 1 will begin on November 21, 2025.

---

**Date** November 21, 2025
**Focus** Phase 1 of pathway will be resource-intensive on current system, create a strategy of hardware utilization that is efficient. Update project list as needed. Research new career options.

---

*Onward to Splunk installation and first detection project.* 🚀
