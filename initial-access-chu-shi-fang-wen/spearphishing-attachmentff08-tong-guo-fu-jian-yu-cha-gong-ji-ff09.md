# Spearphishing Attachment（通过附件鱼叉式攻击）

通过附件的鱼叉攻击是鱼叉攻击的一种特殊手法。通过附件进行的鱼叉攻击不同于其他类型的鱼叉攻击，它将恶意软件附在邮件附件里。所有的鱼叉攻击都是针对特定人、公司或者团体的电子社会工程学。在这种场景中，攻击者将恶意文件放到邮件的附件中并且靠用户打开该文件来获得代码执行。

有多种文件可以作为附件，比如微软的office文档、可执行文件、PDF或者压缩包。在打开附件（或者点击确定，过掉安全防护）之后，攻击者将利用目标系统的漏洞，或者直接在目标系统执行执行程序。邮件正文通常给出一个看似可信的理由来说明附件为什么必须被打开，也许也会介绍怎么绕过安全软件的防护。有时邮件里也会包含解密压缩包的密码，这是为了绕过电子邮件防御网关。通常攻击者会更改后缀名和图标让一个可执行文件看起来像一个文档，或者让这个文件像其他的文件。

## 缓解

| Mitigation | Description |
| :--- | :--- |
| [Antivirus/Antimalware](https://attack.mitre.org/mitigations/M1049) | Anti-virus can also automatically quarantine suspicious files. |
| [Network Intrusion Prevention](https://attack.mitre.org/mitigations/M1031) | Network intrusion prevention systems and systems designed to scan and remove malicious email attachments can be used to block activity. |
| [Restrict Web Based Content](https://attack.mitre.org/mitigations/M1021) | Block unknown or unused attachments by default that should not be transmitted over email as a best practice to prevent some vectors, such as .scr, .exe, .pif, .cpl, etc. Some email scanning devices can open and analyze compressed and encrypted formats, such as zip and rar that may be used to conceal malicious attachments in [Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027). |
| [User Training](https://attack.mitre.org/mitigations/M1017) | Users can be trained to identify social engineering techniques and spearphishing emails. |

## 例子

| Name | Description |
| :--- | :--- |
| [APT12](https://attack.mitre.org/groups/G0005) | [APT12](https://attack.mitre.org/groups/G0005) has sent emails with malicious Microsoft Office documents and PDFs attached.[\[1\]](https://www.fireeye.com/blog/threat-research/2014/09/darwins-favorite-apt-group-2.html)[\[2\]](https://www.trendmicro.de/cloud-content/us/pdfs/security-intelligence/white-papers/wp_ixeshe.pdf) |
| [APT19](https://attack.mitre.org/groups/G0073) | [APT19](https://attack.mitre.org/groups/G0073) sent spearphishing emails with malicious attachments in RTF and XLSM formats to deliver initial exploits.[\[3\]](https://www.fireeye.com/blog/threat-research/2017/06/phished-at-the-request-of-counsel.html) |
| [APT28](https://attack.mitre.org/groups/G0007) | [APT28](https://attack.mitre.org/groups/G0007) sent spearphishing emails containing malicious Microsoft Office attachments.[\[4\]](https://researchcenter.paloaltonetworks.com/2018/02/unit42-sofacy-attacks-multiple-government-entities/)[\[5\]](https://researchcenter.paloaltonetworks.com/2018/03/unit42-sofacy-uses-dealerschoice-target-european-government-agency/)[\[6\]](https://researchcenter.paloaltonetworks.com/2018/06/unit42-sofacy-groups-parallel-attacks/)[\[7\]](https://www.justice.gov/file/1080281/download)[\[8\]](https://securelist.com/a-slice-of-2017-sofacy-activity/83930/)[\[9\]](https://www.accenture.com/t20181129T203820Z__w__/us-en/_acnmedia/PDF-90/Accenture-snakemackerel-delivers-zekapab-malware.pdf#zoom=50) |
| [APT29](https://attack.mitre.org/groups/G0016) | [APT29](https://attack.mitre.org/groups/G0016) has used spearphishing emails with an attachment to deliver files with exploits to initial victims.[\[10\]](https://www.f-secure.com/documents/996508/1030745/dukes_whitepaper.pdf)[\[11\]](https://www.fireeye.com/blog/threat-research/2018/11/not-so-cozy-an-uncomfortable-examination-of-a-suspected-apt29-phishing-campaign.html) |
| [APT32](https://attack.mitre.org/groups/G0050) | [APT32](https://attack.mitre.org/groups/G0050) has sent spearphishing emails with a malicious executable disguised as a document or spreadsheet.[\[12\]](https://www.welivesecurity.com/2018/03/13/oceanlotus-ships-new-backdoor/)[\[13\]](https://www.cybereason.com/blog/operation-cobalt-kitty-apt)[\[14\]](https://cdn2.hubspot.net/hubfs/3354902/Cybereason%20Labs%20Analysis%20Operation%20Cobalt%20Kitty.pdf)[\[15\]](https://www.welivesecurity.com/2019/03/20/fake-or-fake-keeping-up-with-oceanlotus-decoys/) |
| [APT37](https://attack.mitre.org/groups/G0067) | [APT37](https://attack.mitre.org/groups/G0067) delivers malware using spearphishing emails with malicious HWP attachments.[\[16\]](https://www2.fireeye.com/rs/848-DID-242/images/rpt_APT37.pdf)[\[17\]](https://blog.talosintelligence.com/2018/01/korea-in-crosshairs.html)[\[18\]](https://securelist.com/scarcruft-continues-to-evolve-introduces-bluetooth-harvester/90729/) |
| [APT39](https://attack.mitre.org/groups/G0087) | [APT39](https://attack.mitre.org/groups/G0087) leveraged spearphishing emails with malicious attachments to initially compromise victims.[\[19\]](https://www.fireeye.com/blog/threat-research/2019/01/apt39-iranian-cyber-espionage-group-focused-on-personal-information.html) |
| [BRONZE BUTLER](https://attack.mitre.org/groups/G0060) | [BRONZE BUTLER](https://attack.mitre.org/groups/G0060) used spearphishing emails with malicious Microsoft Word attachments to infect victims.[\[20\]](https://www.symantec.com/connect/blogs/tick-cyberespionage-group-zeros-japan) |
| [Cobalt Group](https://attack.mitre.org/groups/G0080) | [Cobalt Group](https://attack.mitre.org/groups/G0080) has sent spearphishing emails with various attachment types to corporate and personal email accounts of victim organizations. Attachment types have included .rtf, .doc, .xls, archives containing LNK files, and password protected archives containing .exe and .scr executables.[\[21\]](https://blog.talosintelligence.com/2018/07/multiple-cobalt-personality-disorder.html)[\[22\]](https://www.ptsecurity.com/upload/corporate/ww-en/analytics/Cobalt-2017-eng.pdf)[\[23\]](https://www.ptsecurity.com/upload/corporate/ww-en/analytics/Cobalt-Snatch-eng.pdf)[\[24\]](https://www.group-ib.com/blog/cobalt)[\[25\]](https://www.proofpoint.com/us/threat-insight/post/microsoft-word-intruder-integrates-cve-2017-0199-utilized-cobalt-group-target)[\[26\]](https://www.riskiq.com/blog/labs/cobalt-strike/)[\[27\]](https://researchcenter.paloaltonetworks.com/2018/10/unit42-new-techniques-uncover-attribute-cobalt-gang-commodity-builders-infrastructure-revealed/)[\[28\]](https://blog.trendmicro.com/trendlabs-security-intelligence/cobalt-spam-runs-use-macros-cve-2017-8759-exploit/) |
| [Darkhotel](https://attack.mitre.org/groups/G0012) | [Darkhotel](https://attack.mitre.org/groups/G0012) has sent spearphishing emails with malicious RAR attachments.[\[29\]](https://securelist.com/darkhotels-attacks-in-2015/71713/) |
| [DarkHydrus](https://attack.mitre.org/groups/G0079) | [DarkHydrus](https://attack.mitre.org/groups/G0079) has sent spearphishing emails with password-protected RAR archives containing malicious Excel Web Query files \(.iqy\). The group has also sent spearphishing emails that contained malicious Microsoft Office documents that use the "attachedTemplate" technique to load a template from a remote server.[\[30\]](https://researchcenter.paloaltonetworks.com/2018/07/unit42-new-threat-actor-group-darkhydrus-targets-middle-east-government/)[\[31\]](https://researchcenter.paloaltonetworks.com/2018/08/unit42-darkhydrus-uses-phishery-harvest-credentials-middle-east/)[\[32\]](https://pan-unit42.github.io/playbook_viewer/) |
| [Dragonfly 2.0](https://attack.mitre.org/groups/G0074) | [Dragonfly 2.0](https://attack.mitre.org/groups/G0074) used spearphishing with Microsoft Office attachments to target victims.[\[33\]](https://www.us-cert.gov/ncas/alerts/TA18-074A)[\[34\]](https://www.us-cert.gov/ncas/alerts/TA17-293A) |
| [Elderwood](https://attack.mitre.org/groups/G0066) | [Elderwood](https://attack.mitre.org/groups/G0066) has delivered zero-day exploits and malware to victims via targeted emails containing malicious attachments.[\[35\]](http://www.symantec.com/content/en/us/enterprise/media/security_response/whitepapers/the-elderwood-project.pdf)[\[36\]](https://www.csmonitor.com/USA/2012/0914/Stealing-US-business-secrets-Experts-ID-two-huge-cyber-gangs-in-China) |
| [Emotet](https://attack.mitre.org/software/S0367) | [Emotet](https://attack.mitre.org/software/S0367) has been delivered by phishing emails containing attachments.[\[37\]](https://www.cisecurity.org/blog/emotet-changes-ttp-and-arrives-in-united-states/)[\[38\]](https://support.malwarebytes.com/docs/DOC-2295)[\[39\]](https://www.symantec.com/blogs/threat-intelligence/evolution-emotet-trojan-distributor)[\[40\]](https://www.us-cert.gov/ncas/alerts/TA18-201A)[\[41\]](https://blog.talosintelligence.com/2019/01/return-of-emotet.html)[\[42\]](https://documents.trendmicro.com/assets/white_papers/ExploringEmotetsActivities_Final.pdf)[\[43\]](https://www.picussecurity.com/blog/the-christmas-card-you-never-wanted-a-new-wave-of-emotet-is-back-to-wreak-havoc.html)[\[44\]](https://www.carbonblack.com/2019/04/24/cb-tau-threat-intelligence-notification-emotet-utilizing-wmi-to-launch-powershell-encoded-code/) |
| [FIN4](https://attack.mitre.org/groups/G0085) | [FIN4](https://attack.mitre.org/groups/G0085) has used spearphishing emails containing attachments \(which are often stolen, legitimate documents sent from compromised accounts\) with embedded malicious macros.[\[45\]](https://www.fireeye.com/current-threats/threat-intelligence-reports/rpt-fin4.html)[\[46\]](https://www2.fireeye.com/WBNR-14Q4NAMFIN4.html) |
| [FIN7](https://attack.mitre.org/groups/G0046) | [FIN7](https://attack.mitre.org/groups/G0046) sent spearphishing emails with either malicious Microsoft Documents or RTF files attached.[\[47\]](https://www.fireeye.com/blog/threat-research/2017/04/fin7-phishing-lnk.html)[\[48\]](https://www.justice.gov/opa/press-release/file/1084361/download)[\[49\]](https://www.flashpoint-intel.com/blog/fin7-revisited-inside-astra-panel-and-sqlrat-malware/) |
| [FIN8](https://attack.mitre.org/groups/G0061) | [FIN8](https://attack.mitre.org/groups/G0061) has distributed targeted emails containing Word documents with embedded malicious macros.[\[50\]](https://www.fireeye.com/blog/threat-research/2017/06/obfuscation-in-the-wild.html)[\[51\]](https://www.fireeye.com/blog/threat-research/2016/05/windows-zero-day-payment-cards.html)[\[52\]](https://www2.fireeye.com/WBNR-Know-Your-Enemy-UNC622-Spear-Phishing.html) |
| [Gallmaker](https://attack.mitre.org/groups/G0084) | [Gallmaker](https://attack.mitre.org/groups/G0084) sent emails with malicious Microsoft Office documents attached.[\[53\]](https://www.symantec.com/blogs/threat-intelligence/gallmaker-attack-group) |
| [Gorgon Group](https://attack.mitre.org/groups/G0078) | [Gorgon Group](https://attack.mitre.org/groups/G0078) sent emails to victims with malicious Microsoft Office documents attached.[\[54\]](https://researchcenter.paloaltonetworks.com/2018/08/unit42-gorgon-group-slithering-nation-state-cybercrime/) |
| [Lazarus Group](https://attack.mitre.org/groups/G0032) | [Lazarus Group](https://attack.mitre.org/groups/G0032) has targeted victims with spearphishing emails containing malicious Microsoft Word documents.[\[55\]](https://securingtomorrow.mcafee.com/mcafee-labs/hidden-cobra-targets-turkish-financial-sector-new-bankshot-implant/) |
| [Leviathan](https://attack.mitre.org/groups/G0065) | [Leviathan](https://attack.mitre.org/groups/G0065) has sent spearphishing emails with malicious attachments, including .rtf, .doc, and .xls files.[\[56\]](https://www.proofpoint.com/us/threat-insight/post/leviathan-espionage-actor-spearphishes-maritime-and-defense-targets) |
| [Magic Hound](https://attack.mitre.org/groups/G0059) | [Magic Hound](https://attack.mitre.org/groups/G0059) sent malicious attachments to victims over email, including an Excel spreadsheet containing macros to download Pupy.[\[57\]](https://www.secureworks.com/research/the-curious-case-of-mia-ash) |
| [menuPass](https://attack.mitre.org/groups/G0045) | [menuPass](https://attack.mitre.org/groups/G0045) has sent malicious Office documents via email as part of spearphishing campaigns as well as executables disguised as documents.[\[58\]](https://www.pwc.co.uk/cyber-security/pdf/cloud-hopper-annex-b-final.pdf)[\[59\]](https://www.fireeye.com/blog/threat-research/2017/04/apt10_menupass_grou.html)[\[60\]](https://www.fireeye.com/blog/threat-research/2018/09/apt10-targeting-japanese-corporations-using-updated-ttps.html)[\[61\]](https://www.justice.gov/opa/press-release/file/1121706/download) |
| [MuddyWater](https://attack.mitre.org/groups/G0069) | [MuddyWater](https://attack.mitre.org/groups/G0069) has compromised third parties and used compromised accounts to send spearphishing emails with targeted attachments to recipients.[\[62\]](https://researchcenter.paloaltonetworks.com/2017/11/unit42-muddying-the-water-targeted-attacks-in-the-middle-east/)[\[63\]](https://www.fireeye.com/blog/threat-research/2018/03/iranian-threat-group-updates-ttps-in-spear-phishing-campaign.html)[\[64\]](https://securelist.com/muddywater/88059/) |
| [OceanSalt](https://attack.mitre.org/software/S0346) | [OceanSalt](https://attack.mitre.org/software/S0346) has been delivered via spearphishing emails with Microsoft Office attachments.[\[65\]](https://www.mcafee.com/enterprise/en-us/assets/reports/rp-operation-oceansalt.pdf) |
| [OilRig](https://attack.mitre.org/groups/G0049) | [OilRig](https://attack.mitre.org/groups/G0049) has sent spearphising emails with malicious attachments to potential victims using compromised and/or spoofed email accounts.[\[66\]](https://researchcenter.paloaltonetworks.com/2018/02/unit42-oopsie-oilrig-uses-threedollars-deliver-new-trojan/)[\[67\]](https://researchcenter.paloaltonetworks.com/2018/07/unit42-oilrig-targets-technology-service-provider-government-agency-quadagent/)[\[68\]](https://www.crowdstrike.com/blog/meet-crowdstrikes-adversary-of-the-month-for-november-helix-kitten/) |
| [Patchwork](https://attack.mitre.org/groups/G0040) | [Patchwork](https://attack.mitre.org/groups/G0040) has used spearphishing with an attachment to deliver files with exploits to initial victims.[\[69\]](https://s3-us-west-2.amazonaws.com/cymmetria-blog/public/Unveiling_Patchwork.pdf)[\[70\]](https://securelist.com/the-dropping-elephant-actor/75328/)[\[71\]](https://documents.trendmicro.com/assets/tech-brief-untangling-the-patchwork-cyberespionage-group.pdf)[\[72\]](https://www.volexity.com/blog/2018/06/07/patchwork-apt-group-targets-us-think-tanks/) |
| [PLATINUM](https://attack.mitre.org/groups/G0068) | [PLATINUM](https://attack.mitre.org/groups/G0068) has sent spearphishing emails with attachments to victims as its primary initial access vector.[\[73\]](https://download.microsoft.com/download/2/2/5/225BFE3E-E1DE-4F5B-A77B-71200928D209/Platinum%20feature%20article%20-%20Targeted%20attacks%20in%20South%20and%20Southeast%20Asia%20April%202016.pdf) |
| [Rancor](https://attack.mitre.org/groups/G0075) | [Rancor](https://attack.mitre.org/groups/G0075) has attached a malicious document to an email to gain initial access.[\[74\]](https://researchcenter.paloaltonetworks.com/2018/06/unit42-rancor-targeted-attacks-south-east-asia-using-plaintee-ddkong-malware-families/) |
| [Silence](https://attack.mitre.org/groups/G0091) | [Silence](https://attack.mitre.org/groups/G0091) has sent emails with malicious DOCX, CHM and ZIP attachments. [\[75\]](https://cyberforensicator.com/2019/01/20/silence-dissecting-malicious-chm-files-and-performing-forensic-analysis/)[\[76\]](https://securelist.com/the-silence/83009/) |
| [TA459](https://attack.mitre.org/groups/G0062) | [TA459](https://attack.mitre.org/groups/G0062) has targeted victims using spearphishing emails with malicious Microsoft Word attachments.[\[77\]](https://www.proofpoint.com/us/threat-insight/post/apt-targets-financial-analysts) |
| [TA505](https://attack.mitre.org/groups/G0092) | [TA505](https://attack.mitre.org/groups/G0092) has used spearphishing emails with malicious attachments to initially compromise victims.[\[78\]](https://www.proofpoint.com/us/threat-insight/post/threat-actor-profile-ta505-dridex-globeimposter)[\[79\]](https://www.proofpoint.com/us/threat-insight/post/ta505-shifts-times)[\[80\]](https://www.proofpoint.com/us/threat-insight/post/servhelper-and-flawedgrace-new-malware-introduced-ta505)[\[81\]](https://www.cybereason.com/blog/threat-actor-ta505-targets-financial-enterprises-using-lolbins-and-a-new-backdoor-malware)[\[82\]](https://www.proofpoint.com/us/threat-insight/post/ta505-abusing-settingcontent-ms-within-pdf-files-distribute-flawedammyy-rat)[\[83\]](https://www.proofpoint.com/us/threat-insight/post/leaked-ammyy-admin-source-code-turned-malware) |
| [The White Company](https://attack.mitre.org/groups/G0089) | [The White Company](https://attack.mitre.org/groups/G0089) has sent phishing emails with malicious Microsoft Word attachments to victims.[\[84\]](https://www.cylance.com/content/dam/cylance-web/en-us/resources/knowledge-center/resource-library/reports/WhiteCompanyOperationShaheenReport.pdf?_ga=2.161661948.1943296560.1555683782-1066572390.1555511517) |
| [TrickBot](https://attack.mitre.org/software/S0266) | [TrickBot](https://attack.mitre.org/software/S0266) has used an email with an Excel sheet containing a malicious macro to deploy the malware[\[85\]](https://blog.trendmicro.com/trendlabs-security-intelligence/trickbot-adds-remote-application-credential-grabbing-capabilities-to-its-repertoire/) |
| [Tropic Trooper](https://attack.mitre.org/groups/G0081) | [Tropic Trooper](https://attack.mitre.org/groups/G0081) sent spearphishing emails that contained malicious Microsoft Office attachments.[\[86\]](https://researchcenter.paloaltonetworks.com/2016/11/unit42-tropic-trooper-targets-taiwanese-government-and-fossil-fuel-provider-with-poison-ivy/)[\[87\]](https://www.trendmicro.de/cloud-content/us/pdfs/security-intelligence/white-papers/wp-operation-tropic-trooper.pdf)[\[88\]](https://citizenlab.ca/2018/08/familiar-feeling-a-malware-campaign-targeting-the-tibetan-diaspora-resurfaces/) |
| [Turla](https://attack.mitre.org/groups/G0010) | [Turla](https://attack.mitre.org/groups/G0010) has used spearphishing emails to deliver [BrainTest](https://attack.mitre.org/software/S0293) as a malicious attachment.[\[89\]](https://www.welivesecurity.com/2017/03/30/carbon-paper-peering-turlas-second-stage-backdoor/) |

## 检测

网络入侵检测系统和邮件网关可以检测到经过的恶意邮件。 detonation chambers（直译震爆室，应该是检测附件行为的沙箱）也可以发现恶意附件。可以基于签名，也可以基于行为来检测，但是攻击者也可以构造附件去绕过这些检测。

反病毒软件可能在扫描存储在邮件服务器上或者用户机器上的恶意邮件或者附件时检测到攻击行为。端点感知和网络感知系统可能会在恶意文档打开时检测到恶意文件的行为。（例如微软office文档和pdf可能会启动powershell进程，另外还有其他客户端代码执行的方法和脚本）

## 参考

1. [Moran, N., Oppenheim, M., Engle, S., & Wartell, R.. \(2014, September 3\). Darwin’s Favorite APT Group \[Blog\]. Retrieved November 12, 2014.](https://www.fireeye.com/blog/threat-research/2014/09/darwins-favorite-apt-group-2.html)
2. [Sancho, D., et al. \(2012, May 22\). IXESHE An APT Campaign. Retrieved June 7, 2019.](https://www.trendmicro.de/cloud-content/us/pdfs/security-intelligence/white-papers/wp_ixeshe.pdf)
3. [Ahl, I. \(2017, June 06\). Privileges and Credentials: Phished at the Request of Counsel. Retrieved May 17, 2018.](https://www.fireeye.com/blog/threat-research/2017/06/phished-at-the-request-of-counsel.html)
4. [Lee, B, et al. \(2018, February 28\). Sofacy Attacks Multiple Government Entities. Retrieved March 15, 2018.](https://researchcenter.paloaltonetworks.com/2018/02/unit42-sofacy-attacks-multiple-government-entities/)
5. [Falcone, R. \(2018, March 15\). Sofacy Uses DealersChoice to Target European Government Agency. Retrieved June 4, 2018.](https://researchcenter.paloaltonetworks.com/2018/03/unit42-sofacy-uses-dealerschoice-target-european-government-agency/)
6. [Lee, B., Falcone, R. \(2018, June 06\). Sofacy Group’s Parallel Attacks. Retrieved June 18, 2018.](https://researchcenter.paloaltonetworks.com/2018/06/unit42-sofacy-groups-parallel-attacks/)
7. [Mueller, R. \(2018, July 13\). Indictment - United States of America vs. VIKTOR BORISOVICH NETYKSHO, et al. Retrieved September 13, 2018.](https://www.justice.gov/file/1080281/download)
8. [Kaspersky Lab's Global Research & Analysis Team. \(2018, February 20\). A Slice of 2017 Sofacy Activity. Retrieved November 27, 2018.](https://securelist.com/a-slice-of-2017-sofacy-activity/83930/)
9. [Accenture Security. \(2018, November 29\). SNAKEMACKEREL. Retrieved April 15, 2019.](https://www.accenture.com/t20181129T203820Z__w__/us-en/_acnmedia/PDF-90/Accenture-snakemackerel-delivers-zekapab-malware.pdf#zoom=50)
10. [F-Secure Labs. \(2015, September 17\). The Dukes: 7 years of Russian cyberespionage. Retrieved December 10, 2015.](https://www.f-secure.com/documents/996508/1030745/dukes_whitepaper.pdf)
11. [Dunwoody, M., et al. \(2018, November 19\). Not So Cozy: An Uncomfortable Examination of a Suspected APT29 Phishing Campaign. Retrieved November 27, 2018.](https://www.fireeye.com/blog/threat-research/2018/11/not-so-cozy-an-uncomfortable-examination-of-a-suspected-apt29-phishing-campaign.html)
12. [Foltýn, T. \(2018, March 13\). OceanLotus ships new backdoor using old tricks. Retrieved May 22, 2018.](https://www.welivesecurity.com/2018/03/13/oceanlotus-ships-new-backdoor/)
13. [Dahan, A. \(2017, May 24\). OPERATION COBALT KITTY: A LARGE-SCALE APT IN ASIA CARRIED OUT BY THE OCEANLOTUS GROUP. Retrieved November 5, 2018.](https://www.cybereason.com/blog/operation-cobalt-kitty-apt)
14. [Dahan, A. \(2017\). Operation Cobalt Kitty. Retrieved December 27, 2018.](https://cdn2.hubspot.net/hubfs/3354902/Cybereason%20Labs%20Analysis%20Operation%20Cobalt%20Kitty.pdf)
15. [Dumont, R. \(2019, March 20\). Fake or Fake: Keeping up with OceanLotus decoys. Retrieved April 1, 2019.](https://www.welivesecurity.com/2019/03/20/fake-or-fake-keeping-up-with-oceanlotus-decoys/)
16. [FireEye. \(2018, February 20\). APT37 \(Reaper\): The Overlooked North Korean Actor. Retrieved March 1, 2018.](https://www2.fireeye.com/rs/848-DID-242/images/rpt_APT37.pdf)
17. [Mercer, W., Rascagneres, P. \(2018, January 16\). Korea In The Crosshairs. Retrieved May 21, 2018.](https://blog.talosintelligence.com/2018/01/korea-in-crosshairs.html)
18. [GReAT. \(2019, May 13\). ScarCruft continues to evolve, introduces Bluetooth harvester. Retrieved June 4, 2019.](https://securelist.com/scarcruft-continues-to-evolve-introduces-bluetooth-harvester/90729/)
19. [Hawley et al. \(2019, January 29\). APT39: An Iranian Cyber Espionage Group Focused on Personal Information. Retrieved February 19, 2019.](https://www.fireeye.com/blog/threat-research/2019/01/apt39-iranian-cyber-espionage-group-focused-on-personal-information.html)
20. [DiMaggio, J. \(2016, April 28\). Tick cyberespionage group zeros in on Japan. Retrieved July 16, 2018.](https://www.symantec.com/connect/blogs/tick-cyberespionage-group-zeros-japan)
21. [Svajcer, V. \(2018, July 31\). Multiple Cobalt Personality Disorder. Retrieved September 5, 2018.](https://blog.talosintelligence.com/2018/07/multiple-cobalt-personality-disorder.html)
22. [Positive Technologies. \(2017, August 16\). Cobalt Strikes Back: An Evolving Multinational Threat to Finance. Retrieved September 5, 2018.](https://www.ptsecurity.com/upload/corporate/ww-en/analytics/Cobalt-2017-eng.pdf)
23. [Positive Technologies. \(2016, December 16\). Cobalt Snatch. Retrieved October 9, 2018.](https://www.ptsecurity.com/upload/corporate/ww-en/analytics/Cobalt-Snatch-eng.pdf)
24. [Matveeva, V. \(2017, August 15\). Secrets of Cobalt. Retrieved October 10, 2018.](https://www.group-ib.com/blog/cobalt)
25. [Mesa, M, et al. \(2017, June 1\). Microsoft Word Intruder Integrates CVE-2017-0199, Utilized by Cobalt Group to Target Financial Institutions. Retrieved October 10, 2018.](https://www.proofpoint.com/us/threat-insight/post/microsoft-word-intruder-integrates-cve-2017-0199-utilized-cobalt-group-target)
26. [Klijnsma, Y.. \(2017, November 28\). Gaffe Reveals Full List of Targets in Spear Phishing Attack Using Cobalt Strike Against Financial Institutions. Retrieved October 10, 2018.](https://www.riskiq.com/blog/labs/cobalt-strike/)
27. [Unit 42. \(2018, October 25\). New Techniques to Uncover and Attribute Financial actors Commodity Builders and Infrastructure Revealed. Retrieved December 11, 2018.](https://researchcenter.paloaltonetworks.com/2018/10/unit42-new-techniques-uncover-attribute-cobalt-gang-commodity-builders-infrastructure-revealed/)
28. [Giagone, R., Bermejo, L., and Yarochkin, F. \(2017, November 20\). Cobalt Strikes Again: Spam Runs Use Macros and CVE-2017-8759 Exploit Against Russian Banks. Retrieved March 7, 2019.](https://blog.trendmicro.com/trendlabs-security-intelligence/cobalt-spam-runs-use-macros-cve-2017-8759-exploit/)
29. [Kaspersky Lab's Global Research & Analysis Team. \(2015, August 10\). Darkhotel's attacks in 2015. Retrieved November 2, 2018.](https://securelist.com/darkhotels-attacks-in-2015/71713/)
30. [Falcone, R., et al. \(2018, July 27\). New Threat Actor Group DarkHydrus Targets Middle East Government. Retrieved August 2, 2018.](https://researchcenter.paloaltonetworks.com/2018/07/unit42-new-threat-actor-group-darkhydrus-targets-middle-east-government/)
31. [Falcone, R. \(2018, August 07\). DarkHydrus Uses Phishery to Harvest Credentials in the Middle East. Retrieved August 10, 2018.](https://researchcenter.paloaltonetworks.com/2018/08/unit42-darkhydrus-uses-phishery-harvest-credentials-middle-east/)
32. [Unit 42. \(2017, December 15\). Unit 42 Playbook Viewer. Retrieved December 20, 2017.](https://pan-unit42.github.io/playbook_viewer/)
33. [US-CERT. \(2018, March 16\). Alert \(TA18-074A\): Russian Government Cyber Activity Targeting Energy and Other Critical Infrastructure Sectors. Retrieved June 6, 2018.](https://www.us-cert.gov/ncas/alerts/TA18-074A)
34. [US-CERT. \(2017, October 20\). Alert \(TA17-293A\): Advanced Persistent Threat Activity Targeting Energy and Other Critical Infrastructure Sectors. Retrieved November 2, 2017.](https://www.us-cert.gov/ncas/alerts/TA17-293A)
35. [O'Gorman, G., and McDonald, G.. \(2012, September 6\). The Elderwood Project. Retrieved February 15, 2018.](http://www.symantec.com/content/en/us/enterprise/media/security_response/whitepapers/the-elderwood-project.pdf)
36. [Clayton, M.. \(2012, September 14\). Stealing US business secrets: Experts ID two huge cyber 'gangs' in China. Retrieved February 15, 2018.](https://www.csmonitor.com/USA/2012/0914/Stealing-US-business-secrets-Experts-ID-two-huge-cyber-gangs-in-China)
37. [CIS. \(2017, April 28\). Emotet Changes TTPs and Arrives in United States. Retrieved January 17, 2019.](https://www.cisecurity.org/blog/emotet-changes-ttp-and-arrives-in-united-states/)
38. [Smith, A.. \(2017, December 22\). Protect your network from Emotet Trojan with Malwarebytes Endpoint Security. Retrieved January 17, 2019.](https://support.malwarebytes.com/docs/DOC-2295)
39. [Symantec. \(2018, July 18\). The Evolution of Emotet: From Banking Trojan to Threat Distributor. Retrieved March 25, 2019.](https://www.symantec.com/blogs/threat-intelligence/evolution-emotet-trojan-distributor)
40. [US-CERT. \(2018, July 20\). Alert \(TA18-201A\) Emotet Malware. Retrieved March 25, 2019.](https://www.us-cert.gov/ncas/alerts/TA18-201A)
41. [Brumaghin, E.. \(2019, January 15\). Emotet re-emerges after the holidays. Retrieved March 25, 2019.](https://blog.talosintelligence.com/2019/01/return-of-emotet.html)
42. [Trend Micro. \(2019, January 16\). Exploring Emotet's Activities . Retrieved March 25, 2019.](https://documents.trendmicro.com/assets/white_papers/ExploringEmotetsActivities_Final.pdf)
43. [Özarslan, S. \(2018, December 21\). The Christmas Card you never wanted - A new wave of Emotet is back to wreak havoc. Retrieved March 25, 2019.](https://www.picussecurity.com/blog/the-christmas-card-you-never-wanted-a-new-wave-of-emotet-is-back-to-wreak-havoc.html)
44. [Lee, S.. \(2019, April 24\). Emotet Using WMI to Launch PowerShell Encoded Code. Retrieved May 24, 2019.](https://www.carbonblack.com/2019/04/24/cb-tau-threat-intelligence-notification-emotet-utilizing-wmi-to-launch-powershell-encoded-code/)
45. [Vengerik, B. et al.. \(2014, December 5\). Hacking the Street? FIN4 Likely Playing the Market. Retrieved December 17, 2018.](https://www.fireeye.com/current-threats/threat-intelligence-reports/rpt-fin4.html)
46. [Vengerik, B. & Dennesen, K.. \(2014, December 5\). Hacking the Street? FIN4 Likely Playing the Market. Retrieved January 15, 2019.](https://www2.fireeye.com/WBNR-14Q4NAMFIN4.html)
47. [Carr, N., et al. \(2017, April 24\). FIN7 Evolution and the Phishing LNK. Retrieved April 24, 2017.](https://www.fireeye.com/blog/threat-research/2017/04/fin7-phishing-lnk.html)
48. [Department of Justice. \(2018, August 01\). HOW FIN7 ATTACKED AND STOLE DATA. Retrieved August 24, 2018.](https://www.justice.gov/opa/press-release/file/1084361/download)
49. [Platt, J. and Reeves, J.. \(2019, March\). FIN7 Revisited: Inside Astra Panel and SQLRat Malware. Retrieved June 18, 2019.](https://www.flashpoint-intel.com/blog/fin7-revisited-inside-astra-panel-and-sqlrat-malware/)
50. [Bohannon, D. & Carr N. \(2017, June 30\). Obfuscation in the Wild: Targeted Attackers Lead the Way in Evasion Techniques. Retrieved February 12, 2018.](https://www.fireeye.com/blog/threat-research/2017/06/obfuscation-in-the-wild.html)
51. [Kizhakkinan, D. et al.. \(2016, May 11\). Threat Actor Leverages Windows Zero-day Exploit in Payment Card Data Attacks. Retrieved February 12, 2018.](https://www.fireeye.com/blog/threat-research/2016/05/windows-zero-day-payment-cards.html)
52. [Elovitz, S. & Ahl, I. \(2016, August 18\). Know Your Enemy: New Financially-Motivated & Spear-Phishing Group. Retrieved February 26, 2018.](https://www2.fireeye.com/WBNR-Know-Your-Enemy-UNC622-Spear-Phishing.html)
53. [Symantec Security Response. \(2018, October 10\). Gallmaker: New Attack Group Eschews Malware to Live off the Land. Retrieved November 27, 2018.](https://www.symantec.com/blogs/threat-intelligence/gallmaker-attack-group)
54. [Falcone, R., et al. \(2018, August 02\). The Gorgon Group: Slithering Between Nation State and Cybercrime. Retrieved August 7, 2018.](https://researchcenter.paloaltonetworks.com/2018/08/unit42-gorgon-group-slithering-nation-state-cybercrime/)
55. [Sherstobitoff, R. \(2018, March 08\). Hidden Cobra Targets Turkish Financial Sector With New Bankshot Implant. Retrieved May 18, 2018.](https://securingtomorrow.mcafee.com/mcafee-labs/hidden-cobra-targets-turkish-financial-sector-new-bankshot-implant/)
56. [Axel F, Pierre T. \(2017, October 16\). Leviathan: Espionage actor spearphishes maritime and defense targets. Retrieved February 15, 2018.](https://www.proofpoint.com/us/threat-insight/post/leviathan-espionage-actor-spearphishes-maritime-and-defense-targets)
57. [Counter Threat Unit Research Team. \(2017, July 27\). The Curious Case of Mia Ash: Fake Persona Lures Middle Eastern Targets. Retrieved February 26, 2018.](https://www.secureworks.com/research/the-curious-case-of-mia-ash)
58. [PwC and BAE Systems. \(2017, April\). Operation Cloud Hopper: Technical Annex. Retrieved April 13, 2017.](https://www.pwc.co.uk/cyber-security/pdf/cloud-hopper-annex-b-final.pdf)
59. [FireEye iSIGHT Intelligence. \(2017, April 6\). APT10 \(MenuPass Group\): New Tools, Global Campaign Latest Manifestation of Longstanding Threat. Retrieved June 29, 2017.](https://www.fireeye.com/blog/threat-research/2017/04/apt10_menupass_grou.html)
60. [Matsuda, A., Muhammad I. \(2018, September 13\). APT10 Targeting Japanese Corporations Using Updated TTPs. Retrieved September 17, 2018.](https://www.fireeye.com/blog/threat-research/2018/09/apt10-targeting-japanese-corporations-using-updated-ttps.html)
61. [United States District Court Southern District of New York \(USDC SDNY\) . \(2018, December 17\). United States of America v. Zhu Hua and Zhang Shilong. Retrieved April 17, 2019.](https://www.justice.gov/opa/press-release/file/1121706/download)
62. [Lancaster, T.. \(2017, November 14\). Muddying the Water: Targeted Attacks in the Middle East. Retrieved March 15, 2018.](https://researchcenter.paloaltonetworks.com/2017/11/unit42-muddying-the-water-targeted-attacks-in-the-middle-east/)
63. [Singh, S. et al.. \(2018, March 13\). Iranian Threat Group Updates Tactics, Techniques and Procedures in Spear Phishing Campaign. Retrieved April 11, 2018.](https://www.fireeye.com/blog/threat-research/2018/03/iranian-threat-group-updates-ttps-in-spear-phishing-campaign.html)
64. [Kaspersky Lab's Global Research & Analysis Team. \(2018, October 10\). MuddyWater expands operations. Retrieved November 2, 2018.](https://securelist.com/muddywater/88059/)
65. [Sherstobitoff, R., Malhotra, A. \(2018, October 18\). ‘Operation Oceansalt’ Attacks South Korea, U.S., and Canada With Source Code From Chinese Hacker Group. Retrieved November 30, 2018.](https://www.mcafee.com/enterprise/en-us/assets/reports/rp-operation-oceansalt.pdf)
66. [Lee, B., Falcone, R. \(2018, February 23\). OopsIE! OilRig Uses ThreeDollars to Deliver New Trojan. Retrieved July 16, 2018.](https://researchcenter.paloaltonetworks.com/2018/02/unit42-oopsie-oilrig-uses-threedollars-deliver-new-trojan/)
67. [Lee, B., Falcone, R. \(2018, July 25\). OilRig Targets Technology Service Provider and Government Agency with QUADAGENT. Retrieved August 9, 2018.](https://researchcenter.paloaltonetworks.com/2018/07/unit42-oilrig-targets-technology-service-provider-government-agency-quadagent/)
68. [Meyers, A. \(2018, November 27\). Meet CrowdStrike’s Adversary of the Month for November: HELIX KITTEN. Retrieved December 18, 2018.](https://www.crowdstrike.com/blog/meet-crowdstrikes-adversary-of-the-month-for-november-helix-kitten/)
69. [Cymmetria. \(2016\). Unveiling Patchwork - The Copy-Paste APT. Retrieved August 3, 2016.](https://s3-us-west-2.amazonaws.com/cymmetria-blog/public/Unveiling_Patchwork.pdf)
70. [Kaspersky Lab's Global Research & Analysis Team. \(2016, July 8\). The Dropping Elephant – aggressive cyber-espionage in the Asian region. Retrieved August 3, 2016.](https://securelist.com/the-dropping-elephant-actor/75328/)
71. [Lunghi, D., et al. \(2017, December\). Untangling the Patchwork Cyberespionage Group. Retrieved July 10, 2018.](https://documents.trendmicro.com/assets/tech-brief-untangling-the-patchwork-cyberespionage-group.pdf)
72. [Meltzer, M, et al. \(2018, June 07\). Patchwork APT Group Targets US Think Tanks. Retrieved July 16, 2018.](https://www.volexity.com/blog/2018/06/07/patchwork-apt-group-targets-us-think-tanks/)
73. [Windows Defender Advanced Threat Hunting Team. \(2016, April 29\). PLATINUM: Targeted attacks in South and Southeast Asia. Retrieved February 15, 2018.](https://download.microsoft.com/download/2/2/5/225BFE3E-E1DE-4F5B-A77B-71200928D209/Platinum%20feature%20article%20-%20Targeted%20attacks%20in%20South%20and%20Southeast%20Asia%20April%202016.pdf)
74. [Ash, B., et al. \(2018, June 26\). RANCOR: Targeted Attacks in South East Asia Using PLAINTEE and DDKONG Malware Families. Retrieved July 2, 2018.](https://researchcenter.paloaltonetworks.com/2018/06/unit42-rancor-targeted-attacks-south-east-asia-using-plaintee-ddkong-malware-families/)
75. [Skulkin, O.. \(2019, January 20\). Silence: Dissecting Malicious CHM Files and Performing Forensic Analysis. Retrieved May 24, 2019.](https://cyberforensicator.com/2019/01/20/silence-dissecting-malicious-chm-files-and-performing-forensic-analysis/)
76. [GReAT. \(2017, November 1\). Silence – a new Trojan attacking financial organizations. Retrieved May 24, 2019.](https://securelist.com/the-silence/83009/)
77. [Axel F. \(2017, April 27\). APT Targets Financial Analysts with CVE-2017-0199. Retrieved February 15, 2018.](https://www.proofpoint.com/us/threat-insight/post/apt-targets-financial-analysts)
78. [Proofpoint Staff. \(2017, September 27\). Threat Actor Profile: TA505, From Dridex to GlobeImposter. Retrieved May 28, 2019.](https://www.proofpoint.com/us/threat-insight/post/threat-actor-profile-ta505-dridex-globeimposter)
79. [Proofpoint Staff. \(2018, June 8\). TA505 shifts with the times. Retrieved May 28, 2019.](https://www.proofpoint.com/us/threat-insight/post/ta505-shifts-times)
80. [Schwarz, D. and Proofpoint Staff. \(2019, January 9\). ServHelper and FlawedGrace - New malware introduced by TA505. Retrieved May 28, 2019.](https://www.proofpoint.com/us/threat-insight/post/servhelper-and-flawedgrace-new-malware-introduced-ta505)
81. [Salem, E. \(2019, April 25\). Threat Actor TA505 Targets Financial Enterprises Using LOLBins and a New Backdoor Malware. Retrieved May 28, 2019.](https://www.cybereason.com/blog/threat-actor-ta505-targets-financial-enterprises-using-lolbins-and-a-new-backdoor-malware)
82. [Proofpoint Staff. \(2018, July 19\). TA505 Abusing SettingContent-ms within PDF files to Distribute FlawedAmmyy RAT. Retrieved April 19, 2019.](https://www.proofpoint.com/us/threat-insight/post/ta505-abusing-settingcontent-ms-within-pdf-files-distribute-flawedammyy-rat)
83. [Proofpoint Staff. \(2018, March 7\). Leaked Ammyy Admin Source Code Turned into Malware. Retrieved May 28, 2019.](https://www.proofpoint.com/us/threat-insight/post/leaked-ammyy-admin-source-code-turned-malware)
84. [Livelli, K, et al. \(2018, November 12\). Operation Shaheen. Retrieved May 1, 2019.](https://www.cylance.com/content/dam/cylance-web/en-us/resources/knowledge-center/resource-library/reports/WhiteCompanyOperationShaheenReport.pdf?_ga=2.161661948.1943296560.1555683782-1066572390.1555511517)
85. [Llimos, N., Pascual, C.. \(2019, February 12\). Trickbot Adds Remote Application Credential-Grabbing Capabilities to Its Repertoire. Retrieved March 12, 2019.](https://blog.trendmicro.com/trendlabs-security-intelligence/trickbot-adds-remote-application-credential-grabbing-capabilities-to-its-repertoire/)
86. [Ray, V. \(2016, November 22\). Tropic Trooper Targets Taiwanese Government and Fossil Fuel Provider With Poison Ivy. Retrieved November 9, 2018.](https://researchcenter.paloaltonetworks.com/2016/11/unit42-tropic-trooper-targets-taiwanese-government-and-fossil-fuel-provider-with-poison-ivy/)
87. [Alintanahin, K. \(2015\). Operation Tropic Trooper: Relying on Tried-and-Tested Flaws to Infiltrate Secret Keepers. Retrieved June 14, 2019.](https://www.trendmicro.de/cloud-content/us/pdfs/security-intelligence/white-papers/wp-operation-tropic-trooper.pdf)
88. [Alexander, G., et al. \(2018, August 8\). Familiar Feeling: A Malware Campaign Targeting the Tibetan Diaspora Resurfaces. Retrieved June 17, 2019.](https://citizenlab.ca/2018/08/familiar-feeling-a-malware-campaign-targeting-the-tibetan-diaspora-resurfaces/)
89. [ESET. \(2017, March 30\). Carbon Paper: Peering into Turla’s second stage backdoor. Retrieved November 7, 2018.](https://www.welivesecurity.com/2017/03/30/carbon-paper-peering-turlas-second-stage-backdoor/)
