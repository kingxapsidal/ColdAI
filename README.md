# COLDMC AI — Autonomous Minecraft Java Server Operations Platform

**COLDMC AI** is a complete, production-grade, AI-powered Minecraft Java server management platform designed for Android phones and Windows PCs. It features a hybrid architecture combining direct Pterodactyl Client API integration, an intelligent AI administrator understanding English and Roman Urdu, and a local Python FastAPI gateway for seamless Wi-Fi communication.

---

## ❄️ 22 Complete Application Screens & Capabilities

1. **Splash Screen**: Animated neon cyan cold branding and system initialization.
2. **Welcome Screen**: Architecture overview and instant setup wizard.
3. **Login / Vault Screen**: Zero-exposure local credential encryption for Pterodactyl tokens.
4. **Main Dashboard**: Live telemetry, CPU/RAM/Disk gauges, quick power dispatches, recent console stream, and AI action queue.
5. **Add Panel Screen**: Add unlimited custom Pterodactyl panels from any hosting provider.
6. **Multiple Panel Manager**: Manage unlimited panels, view connection health, edit, test, or delete.
7. **Panel Connection Details**: Status, host URL, masked client credentials, and server discovery.
8. **Add Minecraft Server**: Configure custom server display name, Pterodactyl ID, host IP, and port (default 25565).
9. **Multiple Server Manager**: Cross-panel Minecraft inventory showing which panel owns each instance.
10. **AI Assistant**: Natural language administrator supporting **English and Roman Urdu** (*"Server start kar do"*, *"RAM check karo"*, *"Latest errors batao"*, *"Plugin search karo"*, *"Server crash kyun hua?"*).
11. **Real-Time Console**: Monospace dark terminal streaming live console logs with command dispatch chips (`/list`, `/tps`, `/spark`, `/say`).
12. **File Manager**: In-app file manager to browse, create folders, edit `server.properties` and YAML configs, and delete files with confirmation.
13. **Plugin Manager**: Modrinth search and 1-click installation into `/plugins/` with version compatibility checks.
14. **Mod Manager**: Dedicated Fabric, Forge, and NeoForge mod search and 1-click installation into `/mods/`.
15. **Performance Monitor**: Hardware CPU, RAM, Disk, Uptime, estimated TPS/MSPT, lag warnings, and Aikar's JVM optimization flags.
16. **Backup Manager**: Create on-demand Pterodactyl snapshots, list backups with dates/sizes, and restore/download options.
17. **Player Manager**: Real-time player list, operator privileges, whitelist toggles, kick, ban, and unban desk.
18. **Anti-Cheat Analysis**: Anomaly detection heuristics (Speed, Reach, KillAura, Chat Spam), confidence scores, and operator review workflow.
19. **Discord Integration**: Webhook notification dispatch for server online/offline, crash alerts, player join/leave, and moderation events.
20. **Crash Analysis (Crash Doctor)**: Stack trace parser, OOM diagnosis, Java 21 bytecode version checker, and step-by-step remediation commands.
21. **Activity History / Audit Logs**: Immutable ledger tracking all operator dispatches and AI-executed actions.
22. **Settings & Wi-Fi Gateway**: Configure local PC gateway IP (`http://192.168.1.x:8000`), port, test connection, theme toggles, and security vault status.

---

## 🤖 Bilingual AI Natural Language Administrator

COLDMC AI understands natural language in **English** and **Roman Urdu**:
- *"Server start kar do"* / *"Start my server"*
- *"Mere server ki RAM check karo"* / *"Check my server RAM"*
- *"Latest errors batao"* / *"Find server errors"*
- *"Plugin search karo EssentialsX"* / *"Install EssentialsX"*
- *"Server crash kyun hua?"* / *"Explain why my server crashed"*
- *"Is configuration ko check karo"* / *"Fix this configuration problem"*
- *"Online players dikhao"* / *"Show online players"*
- *"Create a backup"* / *"Backup banao"*

All dangerous operations (Stop, Restart, Kill, File Delete, Player Ban) mandate explicit operator confirmation before execution.

---

## 💻 Windows Support & Local Wi-Fi Gateway

1. Open PowerShell or Command Prompt in `/backend/`:
   ```powershell
   .\start_windows.ps1
   ```
   Or double click `start_windows.bat`.
2. Access the **PC Web Dashboard**: [http://localhost:8000](http://localhost:8000).
3. Access **Interactive Swagger API Docs**: [http://localhost:8000/docs](http://localhost:8000/docs).
4. Connect Android over Wi-Fi: In COLDMC AI on Android -> Settings -> Enter `http://<YOUR_PC_IP>:8000`.

---

## 🛠️ Building Android APK

- **Local Gradle**: Run `gradle assembleDebug` (outputs to `app/build/outputs/apk/debug/app-debug.apk`).
- **Cloud CI/CD**: Pre-configured GitHub Actions workflow at `.github/workflows/android-build.yml` compiles and publishes the APK automatically upon push.
