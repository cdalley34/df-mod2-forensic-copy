# df-mod2-forensic-copy# P2: Make Forensic Copies & Engage

## Project Overview
I created an evidence folder with five text files, calculated SHA256 hashes for the original evidence, created a forensic copy, and calculated hashes for the copied files. I then modified one file in the forensic copy and recalculated hashes to demonstrate that the change was detected.

## Folders Used
- `evidence`
- `evidence-hashes`
- `evidence-copy`
- `evidence-copy-hashes`

## PowerShell Commands Used

### Hash original evidence
```powershell
Get-ChildItem .\evidence -File | Get-FileHash -Algorithm SHA256 | Out-File .\evidence-hashes\hashes.txt