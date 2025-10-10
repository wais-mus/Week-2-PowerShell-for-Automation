Week 2 - PowerShell for Automation

# Week 2 — PowerShell for Automation ⚙️

### 🎯 Goal
Use PowerShell to automate common Windows tasks and build simple scripts.

---

### 🧠 What I Learned

- PowerShell variables and data types
- Loops (`for`, `foreach`, `while`)
- Functions and parameters
- Common cmdlets:
  - `Get-Process`
  - `Get-Service`
  - `Export-CSV`
- How to automate cleanup tasks (like deleting temp files)
- How to export user and process info to CSV

---

### 🧩 Practice Scripts

#### 🧹 `clean-temp.ps1`
Automates deletion of temporary files in Windows temp directories.

```powershell
# Deletes temporary files older than 7 days
$TempPath = "$env:TEMP"
Get-ChildItem -Path $TempPath -Recurse | 
Where-Object { $_.LastWriteTime -lt (Get-Date).AddDays(-7) } |
Remove-Item -Force -Recurse
Write-Host "Old temp files cleaned successfully."
👥 export-users.ps1
Exports user account details to a CSV file.

powershell
Copy code
Get-LocalUser | Select-Object Name, Enabled, LastLogon | 
Export-CSV "C:\Scripts\users.csv" -NoTypeInformation
Write-Host "User info exported to C:\Scripts\users.csv"
🧩 Git Commands Used
git init — Initialize repo

git add . — Stage all files

git commit -m "Initial commit"

git branch -M main

git remote add origin https://github.com/wais-mus/Week-2-PowerShell-for-Automation.git

git push -u origin main

📘 Resources Used
Microsoft PowerShell Docs

PowerShell Automation Course – YouTube

🗓️ Week Summary
✅ Learned PowerShell automation basics
✅ Practiced with real scripts
✅ Uploaded scripts to GitHub repo
✅ Documented weekly progress

