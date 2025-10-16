# ⚡ PowerShell Cheat Sheet

## 🧰 Basics
| Command | Meaning | Example |
|----------|----------|---------|
| `Get-Command` | Lists all available commands. | `Get-Command *service*` |
| `Get-Help` | Displays help info about a command. | `Get-Help Get-Service -Examples` |
| `Get-Alias` | Shows command shortcuts. | `Get-Alias -Definition Get-ChildItem` |

---

## 📁 File System Navigation
| Command | Meaning | Example |
|----------|----------|---------|
| `Get-Location` | Shows current directory. |  |
| `Set-Location` | Changes directory. | `Set-Location C:\Scripts` |
| `Get-ChildItem` | Lists files and folders. | `Get-ChildItem -Recurse` |
| `New-Item` | Creates a new file or folder. | `New-Item -Path . -Name notes.txt -ItemType File` |

---

## 👥 System & User Management
| Command | Meaning | Example |
|----------|----------|---------|
| `Get-Process` | Lists running processes. |  |
| `Stop-Process` | Kills a process. | `Stop-Process -Name notepad` |
| `Get-Service` | Lists system services. |  |
| `Restart-Service` | Restarts a service. | `Restart-Service -Name Spooler` |

---

## 🧩 Variables & Output
| Command | Meaning | Example |
|----------|----------|---------|
| `$variable = "text"` | Creates a variable. | `$name = "Wais"` |
| `Write-Output` | Prints to console. | `Write-Output "Hello $name"` |
| `Get-Content` | Reads file contents. | `Get-Content .\notes.txt` |
| `Out-File` | Writes output to a file. | `Get-Service | Out-File services.txt` |

---

## 🔁 Loops & Logic
```powershell
# For loop
for ($i=1; $i -le 5; $i++) {
  Write-Host "Number $i"
}

# If statement
if ($uptime -gt 10) {
  Write-Host "Server has been running long!"
}
