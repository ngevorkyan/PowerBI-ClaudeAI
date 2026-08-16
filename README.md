# Power BI × Claude AI

Connect **Power BI Desktop** with **Claude Desktop** using the **Power BI MCP extension** in VS Code, allowing Claude to interact with your Power BI environment.

<img width="1364" height="374" alt="image" src="https://github.com/user-attachments/assets/3196b17f-cfbf-4d5a-b0be-14b5c91cf9e1" />


## 🛠️ Requirements

You need **3 free applications**:

1. **Power BI Desktop**
2. **Visual Studio Code (For MCP)** 
3. **Claude Desktop**

### 📥 Download

* [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
* [Visual Studio Code](https://code.visualstudio.com/)
* [Claude Desktop](https://claude.com/download)

---

# 🔌 Setup

## 1. Install the Power BI MCP Extension

Open **VS Code** and install the **Power BI MCP** extension.

Once the extension is installed and configured, you **don't need to use VS Code again** for the connection.

---

## 2. Find the MCP Server Directory

Navigate to your VS Code extensions folder:

```text
"C:\\Users\\...\\.vscode\\extensions\\analysis-services.powerbi-modeling-mcp-0.4.0-win32-arm64\\server\\**powerbi-modeling-mcp.exe**",
```

Copy the **full path to this directory**.

This directory contains the MCP server that Claude needs to access.

---

## 3. Configure Claude Desktop

Open **Claude Desktop**.

Go to:

**Settings → Developer → Edit Config**

Open the Claude Desktop configuration file.

And replace it with this code : [Claude Desktop Config](https://github.com/ngevorkyan/PowerBI-ClaudeAI/blob/main/claude_desktop_config.json)

Change existing path with your mcp path.

> **Important:** The exact configuration may differ depending on the Power BI MCP extension version. Use the server/entry-point file provided by the extension.

---

## 4. Restart Your Computer

After saving the Claude Desktop configuration:

1. Close Claude Desktop.
2. Restart your computer.
3. Open **Power BI Desktop**.
4. Open **Claude Desktop**.

Claude should now be able to detect and communicate with the Power BI MCP server.

---

# 🚀 You're Ready!

You can now use **Claude Desktop together with Power BI** to interact with your Power BI environment through MCP. Open your .pbix file and it's ready to go!

The basic architecture looks like this:

```text
Power BI Desktop
       ↓
Power BI MCP
       ↓
MCP Server
       ↓
Claude Desktop
       ↓
Claude AI
```

## 💡 Why This Is Useful

This setup allows you to combine:

* 📊 **Power BI** — data modeling and visualization
* 🤖 **Claude AI** — natural-language reasoning and assistance
* 🔌 **MCP** — communication between Claude and Power BI

Instead of manually explaining your Power BI model to an AI, MCP can provide Claude with a structured way to interact with the Power BI environment.

---

## ⚠️ Notes

* All three applications listed above are free to download.
* You only need VS Code to install/configure the MCP extension.
* Keep the MCP extension installed after setup.
* The exact folder names and configuration can change when the extension is updated.
* Make sure **Power BI Desktop and Claude Desktop are restarted after configuration**.

---

## ⭐ Project

**Power BI × Claude AI**

A simple setup for connecting Power BI with Claude Desktop through the Model Context Protocol (MCP).
