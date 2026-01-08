# python_mcp
A python tool callable by MCP which can itself make MCP tool calls as well

> **Execute Python locally. Call any MCP tool. Process unlimited data.** Your AI can finally write and run code that 
bridges all your tools together.

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey.svg)](https://github.com/AuraFriday/mcp-link-server)

# Python Execution — The Workflow Automation Killer

> **Replace n8n, Zapier, Make, and every workflow platform.** Your AI writes the integration code in plain English. No subscriptions. No vendor lock-in. No visual spaghetti. Just intelligent automation that works.

---

## The End of Workflow Automation Platforms

**Forget n8n. Forget Zapier. Forget Make. Forget Tray.io.**

You know the drill: Learn the visual interface. Drag nodes. Connect wires. Debug why the webhook didn't fire. Pay $20-$300/month. Watch it break when APIs change. Rebuild workflows from scratch because you can't express your logic in their limited node system.

**There's a better way.**

### Why Workflow Platforms Are Obsolete

**n8n, Zapier, Make (Integromat), Tray.io, Workato** — they all share the same fundamental problems:

1. **Learning Curve Hell**: Each platform has its own visual language, node system, expression syntax, and quirks. Weeks to master. Months to become proficient.

2. **Subscription Treadmill**: $20-$300/month. Forever. Per user. Plus overage charges. Plus premium connectors. Your automation costs compound.

3. **Brittle by Design**: API changes break workflows. Vendor deprecates a node. Rate limits hit. Error handling is an afterthought. You're constantly fixing things.

4. **Expression Language Torture**: Need complex logic? Welcome to their limited expression language. Can't do what you need? Too bad. Build workarounds. Hack together solutions.

5. **Vendor Lock-In**: Workflows aren't portable. Can't version control properly. Can't test locally. Tied to their platform forever.

6. **The Node Doesn't Exist**: Need to integrate with a niche API? Hope they have a node. They don't? Build a custom HTTP request. Debug authentication. Parse responses manually. Repeat for every endpoint.

### The AI-Native Alternative

**Your AI already understands your request in plain language.** Why force it through a visual workflow builder?

```
You: "When I get an email from a customer, extract the order details, 
     check inventory in our database, update the spreadsheet, and 
     send a confirmation via WhatsApp."

Traditional approach: 
- Open n8n/Zapier
- Find email trigger node
- Configure webhook
- Add email parser node
- Add database query node
- Add spreadsheet update node
- Add WhatsApp node
- Connect everything
- Debug for 2 hours
- Pay $49/month

AI + Python approach:
AI: "I'll write that for you." 
[Writes Python code in 30 seconds]
[Runs it]
Done. $0/month.
```

**The AI writes the integration code.** Not you. Not a visual workflow. The AI.

### What This Really Means

**n8n users**: You learned their node system, expression language, and workflow patterns. That knowledge is now obsolete. Your AI can build better integrations by just understanding your request.

**Zapier users**: You're paying $20-$300/month for integrations your AI can write in seconds. For free. With better error handling. And full Python power.

**Make users**: Your complex scenarios with routers and filters? AI writes cleaner logic in Python. No visual spaghetti. No debugging why the router took the wrong path.

**Tray.io users**: Your "low-code" platform costs $600+/month. AI writes actual code. Better code. For $0/month.

### The Comparison That Matters

| Feature | n8n / Zapier / Make | AI + Python Tool |
|---------|---------------------|------------------|
| **Learning Curve** | Weeks to months | Describe in plain English |
| **Monthly Cost** | $20-$300+ | $0 |
| **Vendor Lock-In** | Total | Zero (standard Python) |
| **API Coverage** | Limited to available nodes | Any API, any service |
| **Complex Logic** | Expression language hell | Full Python |
| **Error Handling** | Basic, platform-specific | Full try/catch, custom logic |
| **Local Testing** | Impossible | Run anywhere |
| **Version Control** | JSON exports (barely) | Git, standard code |
| **Data Processing** | Node memory limits | Unlimited (pandas, numpy) |
| **Debugging** | Platform logs | Full Python debugger |
| **Portability** | Locked to platform | Runs anywhere Python runs |
| **Customization** | Limited by nodes | Unlimited |
| **Maintenance** | You fix broken workflows | AI rewrites on demand |
| **Integration Speed** | Hours to days | Seconds to minutes |

### Real-World Example: The n8n Refugee

**Before (n8n):**
- Monthly cost: $50
- Time to build workflow: 4 hours
- Maintenance: 2 hours/month (fixing broken nodes)
- Learning investment: 20 hours
- Limitations: Can't process large datasets, can't use advanced Python libraries, stuck with available nodes

**After (AI + Python):**
- Monthly cost: $0
- Time to build: 2 minutes (AI writes it)
- Maintenance: 0 (AI rewrites if needed)
- Learning investment: 0 (just describe what you want)
- Limitations: None (full Python ecosystem, all MCP tools, including local and/or remote LLMs, included)

### If You're Here From...

**Searching for n8n alternatives?** You found something better. Not another workflow platform — an AI that writes the code for you.

**Looking for free Zapier alternatives?** This isn't just free. It's more powerful. Your AI writes custom integrations that Zapier can't even express.

**Comparing Make.com vs n8n?** Wrong question. The real question is: why use any workflow platform when AI can write the integration code from your plain English description?

**Want self-hosted automation without subscriptions?** This is it. Runs locally. Zero monthly fees. No vendor to shut down your account.

**Tired of vendor lock-in?** Standard Python. Version control with git. Runs anywhere. Your code, your control, forever.

Not another workflow platform. Not another visual builder. **An AI that writes the automation code for them.**

---

## Benefits

### 1. 🔗 Glue All Tools Together
**Not just Python execution — tool orchestration.** Call browser, sqlite, user interface, and any other MCP tool directly from Python. Your AI writes the glue code that connects everything.

### 2. 💾 Persistent Sessions
**Variables survive between calls.** Start a session, load data, process it across multiple executions. No re-loading, no re-initialization. True stateful programming.

### 3. 📦 Process Unlimited Data
**Break free from context limits.** Parse gigabytes of logs, process thousands of database rows, analyze massive datasets. Python handles it, AI orchestrates it.

---

## Why This Tool Changes Everything

**AI context windows have limits.** Even with 1 million tokens, you can't fit an entire database, all browser tabs, or complete log files. Processing large data directly in AI context is impossible.

**Standard MCP tools can't talk to each other.** Browser tool gets tabs. SQLite tool stores data. User tool displays results. But connecting them? That's on you.

**Python libraries are powerful but isolated.** Pandas, NumPy, BeautifulSoup — incredible tools. But they can't call your browser, query your database, or show UI popups.

**This tool solves all of that.**

Your AI writes Python code that:
- Calls the browser tool to get all tabs
- Processes the data with Python (parse, filter, aggregate)
- Stores results in SQLite via the sqlite tool
- Shows a summary popup via the user tool

All in one execution. All locally. All with unlimited data processing capacity.

---

## 🎯 What Your AI Can Actually Control (Products & APIs)

**The Python tool isn't just for data processing - it's your gateway to controlling hundreds of desktop applications and services.**

When you ask your AI to "automate Excel" or "control Photoshop," it needs to know that the **Python tool** is the right choice. This table shows exactly which products your AI can control through Python APIs, COM/ActiveX, and scripting interfaces.

### 🏢 Microsoft Office & Productivity

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Excel** | `win32com.client` (COM) | Create workbooks, manipulate cells, formulas, charts, pivot tables | `excel = win32com.client.Dispatch('Excel.Application')` |
| **Word** | `win32com.client` (COM) | Document creation, formatting, mail merge, content manipulation | `word = win32com.client.Dispatch('Word.Application')` |
| **PowerPoint** | `win32com.client` (COM) | Slide creation, formatting, animations, presentations | `ppt = win32com.client.Dispatch('PowerPoint.Application')` |
| **Outlook** | `win32com.client` (COM) | Email sending, calendar management, contacts, tasks | `outlook = win32com.client.Dispatch('Outlook.Application')` |
| **Access** | `win32com.client` (COM) | Database queries, report generation, form automation | `access = win32com.client.Dispatch('Access.Application')` |
| **Visio** | `win32com.client` (COM) | Diagram creation, shape manipulation, flowcharts | `visio = win32com.client.Dispatch('Visio.Application')` |
| **Project** | `win32com.client` (COM) | Project management, task scheduling, resource allocation | `project = win32com.client.Dispatch('MSProject.Application')` |
| **OneNote** | `win32com.client` (COM) | Note creation, section management, content extraction | `onenote = win32com.client.Dispatch('OneNote.Application')` |

**Example**: "Create Excel report with sales data" → Python uses `win32com` to automate Excel, populate cells, create charts

### 🎨 CAD & 3D Design

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **AutoCAD** | `win32com.client` (COM) | Drawing automation, entity creation, layer management, plotting | `acad = win32com.client.Dispatch('AutoCAD.Application')` |
| **Inventor** | `win32com.client` (COM) | Part modeling, assembly creation, drawing generation | `inventor = win32com.client.Dispatch('Inventor.Application')` |
| **SolidWorks** | `win32com.client` (COM) | Part/assembly modeling, feature creation, simulation | `sw = win32com.client.Dispatch('SldWorks.Application')` |
| **Rhino 3D** | `rhinoscriptsyntax`, `Rhino.Python` | Geometry creation, NURBS modeling, mesh operations | `import rhinoscriptsyntax as rs` |
| **FreeCAD** | `FreeCAD` module | Parametric modeling, scripting, automation | `import FreeCAD` |
| **Blender** | `bpy` module | 3D modeling, animation, rendering, compositing | `import bpy` |
| **SketchUp** | Ruby API (via subprocess) | Model creation, component management | Via Ruby scripts |
| **Fusion 360** | `adsk.core`, `adsk.fusion` | Cloud CAD automation, parametric modeling | Fusion API |

**Example**: "Draw a circle in AutoCAD" → Python uses COM to access AutoCAD's object model, creates circle entity

### 🎬 Adobe Creative Suite

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Photoshop** | `win32com.client` + JSX | Image manipulation, batch processing, layer operations | COM + ExtendScript bridge |
| **Illustrator** | `win32com.client` + JSX | Vector graphics, path manipulation, text operations | COM + ExtendScript bridge |
| **After Effects** | `win32com.client` + JSX | Composition creation, animation, rendering | COM + ExtendScript bridge |
| **Premiere Pro** | `win32com.client` + JSX | Video editing, sequence manipulation, export | COM + ExtendScript bridge |
| **InDesign** | `win32com.client` + JSX | Page layout, text formatting, document generation | COM + ExtendScript bridge |
| **Acrobat** | `win32com.client` (COM) | PDF manipulation, form filling, annotation | `acrobat = win32com.client.Dispatch('AcroExch.App')` |

**Example**: "Batch resize images in Photoshop" → Python uses COM to execute ExtendScript (JSX) in Photoshop

### 🎥 Video & Animation Software

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **DaVinci Resolve** | `DaVinciResolveScript` | Timeline editing, color grading, rendering, project management | `resolve = dvr_script.scriptapp("Resolve")` |
| **Nuke** | `nuke` module | Compositing, node graph manipulation, rendering | `import nuke` |
| **Houdini** | `hou` module | Procedural modeling, VFX, simulation, rendering | `import hou` |
| **Cinema 4D** | `c4d` module | 3D modeling, animation, rendering | `import c4d` |
| **Maya** | `maya.cmds`, `maya.mel` | 3D animation, rigging, simulation, rendering | `from maya import cmds` |
| **3ds Max** | `pymxs` | 3D modeling, animation, rendering | `import pymxs` |
| **Unreal Engine** | `unreal` module | Level editing, blueprint automation, rendering | `import unreal` |

**Example**: "Automate Resolve timeline" → Python uses DaVinci Resolve API to create timeline, add clips, apply grades

### 🎵 Music Production (DAWs)

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Ableton Live** | `python-osc` (OSC protocol) | Track control, clip launching, parameter automation | `from pythonosc import udp_client` |
| **Reaper** | `reapy` | Full DAW automation, plugin control, rendering | `import reapy` |
| **FL Studio** | `flpianoroll` (limited) | MIDI manipulation, pattern editing | Limited API |

**Example**: "Set Ableton tempo" → Python sends OSC message to Ableton Live's OSC server

### 🗄️ Databases (Native Clients)

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **PostgreSQL** | `psycopg2`, `asyncpg` | SQL queries, transactions, bulk operations | `import psycopg2` |
| **MySQL/MariaDB** | `mysql-connector-python`, `PyMySQL` | SQL queries, database management | `import mysql.connector` |
| **SQL Server** | `pyodbc`, `pymssql` | SQL queries, stored procedures | `import pyodbc` |
| **Oracle** | `cx_Oracle` | SQL queries, PL/SQL execution | `import cx_Oracle` |
| **SQLite** | `sqlite3` (built-in) | Local database operations | `import sqlite3` |
| **MongoDB** | `pymongo` | NoSQL operations, document queries | `from pymongo import MongoClient` |
| **Redis** | `redis-py` | Key-value operations, pub/sub, caching | `import redis` |
| **Elasticsearch** | `elasticsearch-py` | Search queries, indexing, analytics | `from elasticsearch import Elasticsearch` |
| **Cassandra** | `cassandra-driver` | Distributed database operations | `from cassandra.cluster import Cluster` |

**Example**: "Query PostgreSQL database" → Python uses `psycopg2` to connect and execute SQL

### 📊 Data Science & Analytics

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Jupyter** | `nbformat`, `nbconvert` | Notebook manipulation, execution, conversion | `import nbformat` |
| **Tableau** | `tableauserverclient` | Dashboard publishing, data source management | `import tableauserverclient` |
| **Power BI** | `msal` + REST API | Report publishing, dataset refresh | Via REST API |
| **MATLAB** | `matlab.engine` | MATLAB script execution from Python | `import matlab.engine` |
| **R** | `rpy2` | R script execution from Python | `import rpy2.robjects as ro` |
| **SPSS** | `savReaderWriter` | SPSS file manipulation | `from savReaderWriter import *` |

**Example**: "Execute MATLAB code" → Python uses `matlab.engine` to start MATLAB and run scripts

### 🎮 Game Engines & Development

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Unity** | `UnityPython` (limited) | Editor scripting, build automation | Limited support |
| **Unreal Engine** | `unreal` module | Editor automation, blueprint scripting | `import unreal` |
| **Godot** | `gdscript` (via subprocess) | Scene manipulation, build automation | Via GDScript |
| **GameMaker** | GML (via subprocess) | Limited automation via command line | Via GML scripts |

**Example**: "Automate Unreal build" → Python uses `unreal` module to trigger builds, package projects

### 🔬 Scientific Instruments & Lab Equipment

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **LabVIEW** | `pyvisa`, COM | Instrument control, data acquisition | `import pyvisa` |
| **National Instruments** | `nidaqmx` | DAQ control, signal generation | `import nidaqmx` |
| **Keysight Instruments** | `pyvisa` | Oscilloscopes, signal generators, multimeters | SCPI over VISA |
| **Tektronix** | `pyvisa` | Oscilloscope control, waveform capture | SCPI over VISA |
| **Agilent** | `pyvisa` | Test equipment control | SCPI over VISA |

**Example**: "Read oscilloscope" → Python uses `pyvisa` to send SCPI commands to instrument

### 🌐 Web Services & APIs

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Salesforce** | `simple-salesforce` | CRM operations, data queries | `from simple_salesforce import Salesforce` |
| **ServiceNow** | `pysnow` | Ticket management, workflow automation | `import pysnow` |
| **Jira** | `jira` | Issue tracking, project management | `from jira import JIRA` |
| **Confluence** | `atlassian-python-api` | Wiki page management, content creation | `from atlassian import Confluence` |
| **SharePoint** | `Office365-REST-Python-Client` | Document management, list operations | `from office365.sharepoint.client_context import ClientContext` |
| **Slack** | `slack-sdk` | Messaging, channel management, bot control | `from slack_sdk import WebClient` |
| **Discord** | `discord.py` | Bot creation, server management | `import discord` |
| **Telegram** | `python-telegram-bot` | Bot automation, message handling | `from telegram import Bot` |
| **Twitter/X** | `tweepy` | Tweet posting, timeline reading, DM automation | `import tweepy` |
| **GitHub** | `PyGithub` | Repository management, issue tracking, CI/CD | `from github import Github` |
| **GitLab** | `python-gitlab` | Project management, pipeline control | `import gitlab` |

**Example**: "Create Jira ticket" → Python uses `jira` library to authenticate and create issue

### 🖥️ Windows System Automation

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Windows Management** | `wmi` | System info, process management, service control | `import wmi` |
| **Active Directory** | `pyad`, `ldap3` | User management, group operations, queries | `from pyad import aduser` |
| **Windows Registry** | `winreg` (built-in) | Registry read/write operations | `import winreg` |
| **Windows Services** | `win32service` | Service start/stop, status queries | `import win32service` |
| **Task Scheduler** | `win32com.client` (COM) | Scheduled task creation, management | `schedule = win32com.client.Dispatch('Schedule.Service')` |
| **Event Log** | `win32evtlog` | Event log reading, filtering | `import win32evtlog` |
| **PowerShell** | `subprocess` + PowerShell | Execute PowerShell scripts from Python | `subprocess.run(['powershell', '-Command', '...'])` |

**Example**: "Query Active Directory" → Python uses `pyad` to search for users, groups, computers

### 📧 Email Clients & Services

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **SMTP Servers** | `smtplib` (built-in) | Email sending | `import smtplib` |
| **IMAP Servers** | `imaplib` (built-in) | Email reading, folder management | `import imaplib` |
| **POP3 Servers** | `poplib` (built-in) | Email downloading | `import poplib` |
| **Gmail API** | `google-api-python-client` | Gmail automation, label management | `from googleapiclient.discovery import build` |
| **Exchange** | `exchangelib` | Exchange server operations | `from exchangelib import Account` |
| **Mailchimp** | `mailchimp3` | Email campaign management | `from mailchimp3 import MailChimp` |

**Example**: "Read emails via IMAP" → Python uses `imaplib` to connect and fetch messages

### 🔧 Development Tools & IDEs

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **VS Code** | REST API | Extension control, debugging | Via HTTP API |
| **JetBrains IDEs** | Plugin API | Limited automation via plugins | Via plugin system |
| **Sublime Text** | Plugin API | Text manipulation, build systems | Via Python plugins |
| **Vim/Neovim** | `pynvim` | Editor automation, plugin development | `import pynvim` |

**Example**: "Control VS Code" → Python sends HTTP requests to VS Code's REST API

### 🎨 Graphics & Image Processing

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **PIL/Pillow** | `PIL`, `pillow` | Image manipulation, format conversion, filters | `from PIL import Image` |
| **OpenCV** | `cv2` | Computer vision, image processing, video analysis | `import cv2` |
| **scikit-image** | `skimage` | Scientific image processing, segmentation | `from skimage import filters` |
| **ImageMagick** | `Wand` | Advanced image manipulation via ImageMagick | `from wand.image import Image` |
| **GIMP** | `gimpfu` (via subprocess) | Batch image processing, scripting | Via Python-Fu scripts |

**Example**: "Batch resize images" → Python uses Pillow to process directory of images

### 🔬 Scientific Computing

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **NumPy** | `numpy` | Array operations, linear algebra, FFT | `import numpy as np` |
| **SciPy** | `scipy` | Scientific computing, optimization, signal processing | `import scipy` |
| **Pandas** | `pandas` | Data analysis, CSV/Excel processing, time series | `import pandas as pd` |
| **Matplotlib** | `matplotlib` | Data visualization, plotting, charts | `import matplotlib.pyplot as plt` |
| **Seaborn** | `seaborn` | Statistical visualization | `import seaborn as sns` |
| **Plotly** | `plotly` | Interactive visualizations, dashboards | `import plotly.graph_objects as go` |
| **SymPy** | `sympy` | Symbolic mathematics, calculus, algebra | `import sympy` |
| **NetworkX** | `networkx` | Graph theory, network analysis | `import networkx as nx` |

**Example**: "Analyze CSV data" → Python uses Pandas to load, process, and visualize data

### 🤖 Machine Learning & AI

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **TensorFlow** | `tensorflow` | Deep learning, neural networks, training | `import tensorflow as tf` |
| **PyTorch** | `torch` | Deep learning, research, model training | `import torch` |
| **scikit-learn** | `sklearn` | Machine learning, classification, clustering | `from sklearn import svm` |
| **Keras** | `keras` | High-level neural networks | `from keras.models import Sequential` |
| **Hugging Face** | `transformers` | NLP, pre-trained models, fine-tuning | `from transformers import pipeline` |
| **OpenAI API** | `openai` | GPT models, embeddings, completions | `import openai` |
| **LangChain** | `langchain` | LLM orchestration, chains, agents | `from langchain import OpenAI` |
| **spaCy** | `spacy` | NLP, entity recognition, text processing | `import spacy` |

**Example**: "Classify text with ML" → Python uses scikit-learn to train and predict

### 🌐 Cloud Services & APIs

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **AWS (Boto3)** | `boto3` | EC2, S3, Lambda, all AWS services | `import boto3` |
| **Azure SDK** | `azure-*` packages | Azure services, storage, compute | `from azure.storage.blob import BlobServiceClient` |
| **Google Cloud** | `google-cloud-*` | GCP services, storage, compute | `from google.cloud import storage` |
| **DigitalOcean** | `python-digitalocean` | Droplet management, networking | `import digitalocean` |
| **Linode** | `linode-api4` | Server management, networking | `from linode_api4 import LinodeClient` |
| **Heroku** | `heroku3` | App deployment, dyno management | `import heroku3` |
| **Cloudflare** | `cloudflare` | DNS, CDN, Workers, security | `import CloudFlare` |

**Example**: "Upload to S3" → Python uses `boto3` to upload files to AWS S3 bucket

### 📱 Mobile Device Control

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Android (ADB)** | `adb-shell`, `pure-python-adb` | App installation, shell commands, file transfer | `from adb_shell.adb_device import AdbDeviceTcp` |
| **iOS (libimobiledevice)** | `pymobiledevice3` | App management, file access, diagnostics | `from pymobiledevice3 import usbmux` |
| **Appium** | `Appium-Python-Client` | Mobile app automation, testing | `from appium import webdriver` |

**Example**: "Install APK on Android" → Python uses ADB library to push and install app

### 🎯 Testing & Quality Assurance

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Selenium** | `selenium` | Web browser automation, testing | `from selenium import webdriver` |
| **Playwright** | `playwright` | Modern browser automation | `from playwright.sync_api import sync_playwright` |
| **Requests** | `requests` | HTTP API testing, web scraping | `import requests` |
| **pytest** | `pytest` | Test framework, fixtures, assertions | `import pytest` |
| **unittest** | `unittest` (built-in) | Unit testing framework | `import unittest` |
| **Locust** | `locust` | Load testing, performance testing | `from locust import HttpUser` |

**Example**: "Run automated tests" → Python executes pytest test suite

### 📊 Business Intelligence & Reporting

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **Tableau** | `tableauserverclient` | Report publishing, data refresh | `import tableauserverclient as TSC` |
| **Power BI** | `msal` + REST | Dataset refresh, report publishing | Via REST API |
| **Looker** | `looker-sdk` | Dashboard management, queries | `import looker_sdk` |
| **Metabase** | HTTP REST | Dashboard creation, queries | Via HTTP API |
| **Apache Superset** | REST API | Dashboard management, SQL queries | Via HTTP API |

**Example**: "Refresh Tableau dashboard" → Python uses Tableau SDK to trigger data refresh

### 🎬 Video Processing & Transcoding

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **FFmpeg** | `ffmpeg-python` | Video transcoding, streaming, editing | `import ffmpeg` |
| **MoviePy** | `moviepy` | Video editing, effects, composition | `from moviepy.editor import VideoFileClip` |
| **OpenCV** | `cv2` | Video processing, frame extraction, analysis | `import cv2` |
| **PyAV** | `av` | Low-level video/audio processing | `import av` |

**Example**: "Extract video frames" → Python uses OpenCV to read video and save frames

### 🗺️ GIS & Mapping

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **ArcGIS** | `arcpy` | GIS analysis, map automation, spatial queries | `import arcpy` |
| **QGIS** | `qgis.core` | GIS processing, map generation | `from qgis.core import QgsApplication` |
| **GeoPandas** | `geopandas` | Geospatial data analysis | `import geopandas as gpd` |
| **Folium** | `folium` | Interactive map generation | `import folium` |
| **Shapely** | `shapely` | Geometric operations, spatial analysis | `from shapely.geometry import Point` |

**Example**: "Analyze geographic data" → Python uses GeoPandas to process shapefiles

### 🔐 Cryptography & Security

| Product | Python Library | What You Can Do | Example |
|---------|----------------|-----------------|---------|
| **OpenSSL** | `pyOpenSSL` | Certificate management, encryption | `from OpenSSL import SSL` |
| **Cryptography** | `cryptography` | Encryption, signing, key management | `from cryptography.fernet import Fernet` |
| **PyCrypto** | `Crypto` | Legacy encryption, hashing | `from Crypto.Cipher import AES` |
| **Paramiko** | `paramiko` | SSH client, SFTP, key management | `import paramiko` |
| **Scapy** | `scapy` | Packet crafting, network security testing | `from scapy.all import *` |

**Example**: "Generate SSL certificate" → Python uses pyOpenSSL to create and sign certificates

---

## 📡 For Network Protocol Products

Many products are better controlled through **raw network protocols** rather than Python libraries. See the `terminal` tool documentation for products like:
- **OBS Studio, vMix** (WebSocket/HTTP)
- **CNC Mills, 3D Printers** (Serial/G-code)
- **PLCs, Industrial Controllers** (Modbus, OPC UA)
- **Smart Home Devices** (MQTT, HTTP)
- **Databases** (Native wire protocols)
- **And hundreds more...**

The `terminal` tool lets your AI connect directly to these services via TCP, UDP, Serial, WebSocket, and more!

---

## Real-World Story: The Data Pipeline Nightmare

**The Problem:**

A data analyst needed to:
1. Extract data from 500+ browser tabs (research links)
2. Parse and categorize each URL by domain and topic
3. Store results in a database
4. Generate a report with statistics
5. Display results in a user-friendly popup

Standard approach: Export tabs to CSV, write Python script, manually import to database, create report, email results. **Estimated time: 4-6 hours.**

AI approach without this tool: "I can see your tabs, but I can't process 500 URLs in my context. Can you export them?" **Estimated time: Still 4-6 hours.**

**With This Tool:**

```python
# AI writes this code in one go:
import json
from collections import Counter
from datetime import datetime

# 1. Get all browser tabs
tabs_result = mcp.call('browser', {
    'input': {
        'operation': 'list_tabs',
        'tool_unlock_token': 'e5076d'
    }
})

# 2. Parse and categorize
tabs_text = tabs_result['content'][0]['text']
domains = []
for line in tabs_text.strip().split('\n')[1:]:
    parts = line.split('\t')
    if len(parts) >= 7 and 'http' in parts[6]:
        domain = parts[6].split('/')[2]
        domains.append(domain)

# 3. Count and analyze
counts = Counter(domains)
total_tabs = len(domains)
unique_domains = len(counts)

# 4. Store in database
mcp.call('sqlite', {
    'input': {
        'sql': '''CREATE TABLE IF NOT EXISTS tab_analysis 
                  (timestamp TEXT, total_tabs INT, unique_domains INT, top_domain TEXT, top_count INT)''',
        'database': 'research.db',
        'tool_unlock_token': '29e63eb5'
    }
})

top_domain, top_count = counts.most_common(1)[0]
mcp.call('sqlite', {
    'input': {
        'sql': 'INSERT INTO tab_analysis VALUES (?, ?, ?, ?, ?)',
        'params': [datetime.now().isoformat(), total_tabs, unique_domains, top_domain, top_count],
        'database': 'research.db',
        'tool_unlock_token': '29e63eb5'
    }
})

# 5. Show results
report_html = f"""
<!DOCTYPE html>
<html>
<head><style>
    body {{ font-family: Arial; padding: 20px; }}
    .stat {{ background: #f0f0f0; padding: 10px; margin: 10px 0; border-radius: 5px; }}
</style></head>
<body>
    <h1>Browser Tab Analysis</h1>
    <div class="stat"><strong>Total Tabs:</strong> {total_tabs}</div>
    <div class="stat"><strong>Unique Domains:</strong> {unique_domains}</div>
    <div class="stat"><strong>Top Domain:</strong> {top_domain} ({top_count} tabs)</div>
    <h2>Top 10 Domains:</h2>
    <ul>
        {''.join(f'<li>{domain}: {count} tabs</li>' for domain, count in counts.most_common(10))}
    </ul>
</body>
</html>
"""

mcp.call('user', {
    'input': {
        'operation': 'show_popup',
        'html': report_html,
        'title': 'Tab Analysis Results',
        'tool_unlock_token': 'a1b2c3d4'
    }
})

print(f"Analysis complete! {total_tabs} tabs across {unique_domains} domains.")
```

**Result:** Complete analysis in **under 30 seconds**. Data extracted, processed, stored, and displayed. Zero manual steps. Zero context limits.

**The kicker:** Same approach now handles daily monitoring. AI saves the script, schedules it to run hourly, tracks trends over time. Fully automated research pipeline.

---

## Side-by-Side: n8n vs AI+Python

Let's build the same automation in both systems. **Watch how absurd workflow platforms become.**

### Task: "Monitor my website, check if it's down, log to database, alert me if offline"

#### The n8n Way

**Time: 45 minutes** (if you know what you're doing)

1. Open n8n
2. Add "Schedule Trigger" node (configure cron expression)
3. Add "HTTP Request" node (configure URL, method, headers)
4. Add "IF" node (check response status)
5. Add "Set" node (extract data)
6. Add "Postgres" node (configure connection, write INSERT query)
7. Add another "IF" node (check if down)
8. Add "Send Email" node (configure SMTP)
9. Connect all nodes with wires
10. Debug why it's not working
11. Realize you need error handling
12. Add "Error Trigger" node
13. Add more nodes for error handling
14. Test each node individually
15. Deploy
16. Pay $20/month

**Result:** 13+ nodes. Visual spaghetti. Breaks when API changes. Limited error handling. Locked to n8n.

#### The AI+Python Way

**Time: 30 seconds** (AI writes it)

**You:** "Monitor my website every 5 minutes, check if it's down, log to database, alert me if offline"

**AI:** "I'll write that for you."

```python
import requests
from datetime import datetime

# Check website
try:
    response = requests.get('https://mywebsite.com', timeout=10)
    status = 'UP' if response.status_code == 200 else 'DOWN'
except Exception as e:
    status = 'DOWN'
    error = str(e)

# Log to database
mcp.call('sqlite', {
    'input': {
        'sql': 'INSERT INTO monitoring (timestamp, status) VALUES (?, ?)',
        'params': [datetime.now().isoformat(), status],
        'database': 'monitoring.db',
        'tool_unlock_token': '29e63eb5'
    }
})

# Alert if down
if status == 'DOWN':
    mcp.call('user', {
        'input': {
            'operation': 'show_popup',
            'html': f'<h1 style="color:red">ALERT: Website is DOWN!</h1><p>{error}</p>',
            'title': 'Website Alert',
            'tool_unlock_token': 'a1b2c3d4'
        }
    })

print(f"Status: {status}")
```

**Result:** Clean code. Full error handling. Easy to modify. Runs anywhere. $0/month.

### When Requirements Change

**n8n:** "Add retry logic with exponential backoff"
- Add "Wait" node
- Add "Loop" node  
- Reconfigure IF nodes
- Reconnect wires
- Debug for 30 minutes
- Hope you got it right

**AI+Python:** "Add retry logic with exponential backoff"
- AI rewrites the code in 10 seconds
- Done

### The Brutal Truth

**Workflow platforms made sense in 2015.** Before AI could write code. Before AI could understand plain language requests.

**In 2025, they're obsolete.** Why learn a visual interface when AI writes better code from your description?

**The only reason to use n8n/Zapier/Make today:** You don't know this exists.

**Now you do.**

---

## The Complete Feature Set

### Code Execution

**Basic Execution:**
```python
# Execute Python code
result = execute(code="""
import json
data = {'message': 'Hello from Python!'}
print(json.dumps(data))
""")
```

**Persistent Sessions:**
```python
# First execution - load data
execute(
    code="import pandas as pd; df = pd.read_csv('data.csv')",
    session_id="analysis",
    persistent=True
)

# Second execution - process data (df still available!)
execute(
    code="print(df.describe())",
    session_id="analysis",
    persistent=True
)

# Third execution - more processing (df still there!)
execute(
    code="filtered = df[df['value'] > 100]; print(len(filtered))",
    session_id="analysis",
    persistent=True
)
```

**Why persistent sessions matter:** Load large datasets once, process across multiple steps. No re-loading, no memory waste, true stateful programming.

**Main Thread Execution:**
```python
# For COM objects (Windows automation) that need to persist
execute(
    code="import win32com.client; excel = win32com.client.Dispatch('Excel.Application')",
    session_id="excel_work",
    persistent=True,
    run_on_main_thread=True  # Required for COM objects
)
```

**Clear Sessions:**
```python
# Free memory when done
clear_session(session_id="analysis")
```

### MCP Tool Integration

**The `mcp` Module:**

Every Python execution automatically has access to an `mcp` module (no import needed) that can call any MCP tool:

```python
# mcp is already available!
result = mcp.call('tool_name', {
    'input': {
        'operation': 'some_operation',
        'param1': 'value1',
        'tool_unlock_token': 'token_here'
    }
})
```

**Browser Tool Integration:**
```python
# Get all browser tabs
tabs = mcp.call('browser', {
    'input': {
        'operation': 'list_tabs',
        'tool_unlock_token': 'e5076d'
    }
})

# Navigate to URL
mcp.call('browser', {
    'input': {
        'operation': 'navigate',
        'url': 'https://example.com',
        'tool_unlock_token': 'e5076d'
    }
})

# Extract page content
content = mcp.call('browser', {
    'input': {
        'operation': 'extract_page_content',
        'tool_unlock_token': 'e5076d'
    }
})
```

**SQLite Tool Integration:**
```python
# Query database
result = mcp.call('sqlite', {
    'input': {
        'sql': 'SELECT name, price FROM products WHERE price > ?',
        'params': [100],
        'database': 'store.db',
        'tool_unlock_token': '29e63eb5'
    }
})

# Parse results
data = json.loads(result['content'][0]['text'])
for row in data:
    print(f"{row['name']}: ${row['price']}")
```

**User Interface Integration:**
```python
# Show popup with results
mcp.call('user', {
    'input': {
        'operation': 'show_popup',
        'html': '<h1>Processing Complete!</h1><p>Results saved.</p>',
        'title': 'Success',
        'tool_unlock_token': 'a1b2c3d4'
    }
})

# Collect API key
mcp.call('user', {
    'input': {
        'operation': 'collect_api_key',
        'service_name': 'OpenAI',
        'tool_unlock_token': 'a1b2c3d4'
    }
})
```

**System Tool Integration:**
```python
# List windows
windows = mcp.call('system', {
    'input': {
        'operation': 'list_windows',
        'tool_unlock_token': 'bd462fdb'
    }
})

# Take screenshot
screenshot = mcp.call('system', {
    'input': {
        'operation': 'take_screenshot',
        'hwnd': '0x00020828',
        'tool_unlock_token': 'bd462fdb'
    }
})
```

**Why this matters:** Python becomes the universal glue. Any tool can talk to any other tool. Unlimited data processing with full tool ecosystem access.

### Script Management

**Save Scripts:**
```python
# Save code for later use
save_script(
    filename="monitor_tabs.py",
    code="""
import json
from datetime import datetime

# Get current browser tabs
tabs_result = mcp.call('browser', {
    'input': {
        'operation': 'list_tabs',
        'tool_unlock_token': 'e5076d'
    }
})

# Count tabs
tabs_text = tabs_result['content'][0]['text']
tab_count = len(tabs_text.strip().split('\\n')) - 1

# Store in database
mcp.call('sqlite', {
    'input': {
        'sql': 'INSERT INTO tab_history (timestamp, count) VALUES (?, ?)',
        'params': [datetime.now().isoformat(), tab_count],
        'database': 'monitoring.db',
        'tool_unlock_token': '29e63eb5'
    }
})

print(f'Logged {tab_count} tabs at {datetime.now()}')
"""
)
```

**Load Scripts:**
```python
# Load previously saved script
script = load_script(filename="monitor_tabs.py")

# Execute it
execute(code=script['code'], session_id="monitoring")
```

**List Scripts:**
```python
# See all saved scripts
scripts = list_scripts()
# Returns: list of filenames with sizes and timestamps
```

**Delete Scripts:**
```python
# Remove old scripts
delete_script(filename="old_script.py")
```

**Why script management matters:** Build a library of reusable automation. Save complex workflows, load and run them later. Create a personal toolkit.

---

## Advanced Use Cases

### Multi-Tool Data Pipeline

```python
# Complete data pipeline across multiple tools
import json
from datetime import datetime

# 1. Extract data from browser
tabs = mcp.call('browser', {'input': {'operation': 'list_tabs', 'tool_unlock_token': 'e5076d'}})
tabs_text = tabs['content'][0]['text']

# 2. Process with Python
urls = []
for line in tabs_text.strip().split('\n')[1:]:
    parts = line.split('\t')
    if len(parts) >= 7:
        urls.append(parts[6])

# 3. Store in database
mcp.call('sqlite', {
    'input': {
        'sql': 'CREATE TABLE IF NOT EXISTS urls (url TEXT, timestamp TEXT)',
        'database': 'research.db',
        'tool_unlock_token': '29e63eb5'
    }
})

for url in urls:
    mcp.call('sqlite', {
        'input': {
            'sql': 'INSERT INTO urls VALUES (?, ?)',
            'params': [url, datetime.now().isoformat()],
            'database': 'research.db',
            'tool_unlock_token': '29e63eb5'
        }
    })

# 4. Query and analyze
result = mcp.call('sqlite', {
    'input': {
        'sql': 'SELECT COUNT(*) as count FROM urls',
        'database': 'research.db',
        'tool_unlock_token': '29e63eb5'
    }
})

count = json.loads(result['content'][0]['text'])[0]['count']

# 5. Display results
mcp.call('user', {
    'input': {
        'operation': 'show_popup',
        'html': f'<h1>Stored {count} URLs</h1>',
        'title': 'Success',
        'tool_unlock_token': 'a1b2c3d4'
    }
})
```

### Persistent Data Analysis

```python
# Session 1: Load and prepare data
execute(
    code="""
import pandas as pd
import json

# Load data from database
result = mcp.call('sqlite', {
    'input': {
        'sql': 'SELECT * FROM sales',
        'database': 'business.db',
        'tool_unlock_token': '29e63eb5'
    }
})

data = json.loads(result['content'][0]['text'])
df = pd.DataFrame(data)
print(f"Loaded {len(df)} rows")
""",
    session_id="analysis",
    persistent=True
)

# Session 2: Analyze (df still available!)
execute(
    code="""
# df is still here from previous execution!
summary = df.groupby('product')['revenue'].sum().sort_values(ascending=False)
print("Top products by revenue:")
print(summary.head(10))
""",
    session_id="analysis",
    persistent=True
)

# Session 3: Generate report (df and summary still available!)
execute(
    code="""
# Both df and summary are still available!
report_html = f'''
<html>
<body>
    <h1>Sales Analysis</h1>
    <p>Total Records: {len(df)}</p>
    <p>Total Revenue: ${df['revenue'].sum():,.2f}</p>
    <h2>Top Products:</h2>
    <ul>
        {''.join(f'<li>{product}: ${revenue:,.2f}</li>' for product, revenue in summary.head(10).items())}
    </ul>
</body>
</html>
'''

mcp.call('user', {
    'input': {
        'operation': 'show_popup',
        'html': report_html,
        'title': 'Sales Report',
        'tool_unlock_token': 'a1b2c3d4'
    }
})
""",
    session_id="analysis",
    persistent=True
)
```

### Automated Monitoring Script

```python
# Save a monitoring script
save_script(
    filename="website_monitor.py",
    code="""
import json
from datetime import datetime

# Navigate to website
mcp.call('browser', {
    'input': {
        'operation': 'navigate',
        'url': 'https://status.example.com',
        'tool_unlock_token': 'e5076d'
    }
})

# Extract page content
content = mcp.call('browser', {
    'input': {
        'operation': 'extract_page_content',
        'tool_unlock_token': 'e5076d'
    }
})

# Parse status
page_data = json.loads(content['content'][0]['text'])
status = 'UP' if 'operational' in page_data.get('text', '').lower() else 'DOWN'

# Store in database
mcp.call('sqlite', {
    'input': {
        'sql': 'INSERT INTO monitoring (timestamp, status) VALUES (?, ?)',
        'params': [datetime.now().isoformat(), status],
        'database': 'monitoring.db',
        'tool_unlock_token': '29e63eb5'
    }
})

# Alert if down
if status == 'DOWN':
    mcp.call('user', {
        'input': {
            'operation': 'show_popup',
            'html': '<h1 style="color:red">ALERT: Website is DOWN!</h1>',
            'title': 'Status Alert',
            'tool_unlock_token': 'a1b2c3d4'
        }
    })

print(f"Status check at {datetime.now()}: {status}")
"""
)

# Later: Load and run the monitoring script
script = load_script(filename="website_monitor.py")
execute(code=script['code'])
```

### Complex Data Transformation

```python
# Process large dataset that won't fit in AI context
execute(
    code="""
import json
import pandas as pd
from datetime import datetime, timedelta

# Get data from database (thousands of rows)
result = mcp.call('sqlite', {
    'input': {
        'sql': 'SELECT * FROM transactions WHERE date > ?',
        'params': [(datetime.now() - timedelta(days=30)).isoformat()],
        'database': 'sales.db',
        'tool_unlock_token': '29e63eb5'
    }
})

# Load into pandas (handles large data efficiently)
data = json.loads(result['content'][0]['text'])
df = pd.DataFrame(data)

# Complex transformations
df['date'] = pd.to_datetime(df['date'])
df['revenue'] = df['quantity'] * df['price']

# Aggregate by multiple dimensions
summary = df.groupby(['product', 'region']).agg({
    'revenue': 'sum',
    'quantity': 'sum',
    'transaction_id': 'count'
}).reset_index()

summary.columns = ['product', 'region', 'total_revenue', 'total_quantity', 'transaction_count']

# Store results back
mcp.call('sqlite', {
    'input': {
        'sql': 'DROP TABLE IF EXISTS sales_summary',
        'database': 'sales.db',
        'tool_unlock_token': '29e63eb5'
    }
})

# Insert summary data
for _, row in summary.iterrows():
    mcp.call('sqlite', {
        'input': {
            'sql': 'INSERT INTO sales_summary VALUES (?, ?, ?, ?, ?)',
            'params': [row['product'], row['region'], row['total_revenue'], 
                      row['total_quantity'], row['transaction_count']],
            'database': 'sales.db',
            'tool_unlock_token': '29e63eb5'
        }
    })

print(f"Processed {len(df)} transactions into {len(summary)} summary rows")
""",
    session_id="etl_job",
    persistent=True
)
```

---

## Usage Examples

### Execute Python Code
```json
{
  "input": {
    "operation": "execute",
    "code": "import json\ndata = {'result': 42}\nprint(json.dumps(data))",
    "session_id": "my_session",
    "persistent": true,
    "tool_unlock_token": "YOUR_TOKEN"
  }
}
```

### Save Script
```json
{
  "input": {
    "operation": "save_script",
    "filename": "my_automation.py",
    "code": "print('Hello from saved script!')",
    "tool_unlock_token": "YOUR_TOKEN"
  }
}
```

### Load Script
```json
{
  "input": {
    "operation": "load_script",
    "filename": "my_automation.py",
    "tool_unlock_token": "YOUR_TOKEN"
  }
}
```

### List Scripts
```json
{
  "input": {
    "operation": "list_scripts",
    "tool_unlock_token": "YOUR_TOKEN"
  }
}
```

### Delete Script
```json
{
  "input": {
    "operation": "delete_script",
    "filename": "old_script.py",
    "tool_unlock_token": "YOUR_TOKEN"
  }
}
```

### Clear Session
```json
{
  "input": {
    "operation": "clear_session",
    "session_id": "my_session",
    "tool_unlock_token": "YOUR_TOKEN"
  }
}
```

---

## Technical Architecture

### Execution Environment

**Isolated Execution:**
- Each execution runs in controlled namespace
- Standard library fully available
- No filesystem restrictions (runs as user)
- Full network access

**Persistent Sessions:**
- Session globals cached in memory
- Thread-safe access via locks
- Survives between executions
- Cleared manually or on server restart

**Main Thread Execution:**
- Optional for COM object persistence (Windows)
- Required for some GUI libraries
- Slightly slower than thread pool execution
- Use only when necessary

### MCP Bridge

**Automatic Injection:**
- `mcp` module injected into every execution
- No import needed, always available
- Direct access to HANDLERS registry
- Calls any registered MCP tool

**Call Signature:**
```python
result = mcp.call('tool_name', parameters_dict)
# Returns: MCP tool response (usually dict with 'content' key)
```

**Error Handling:**
- Tool errors propagated to Python
- Python exceptions captured and returned
- Full traceback available for debugging

### Script Storage

**Location:**
- User data directory (platform-specific)
- `python_scripts/` subdirectory
- Persistent across server restarts
- User-accessible for manual editing

**File Format:**
- Plain Python (.py) files
- UTF-8 encoding
- No size limits
- Standard Python syntax

---

## Performance Considerations

### Execution Speed
- Code compilation: ~1-5ms
- Execution: Depends on code complexity
- MCP tool calls: Add tool-specific latency
- Persistent sessions: No reload overhead

### Memory Usage
- Each session: Holds all variables in memory
- Large datasets: Use pandas/numpy for efficiency
- Clear sessions: Free memory when done
- Server restart: Clears all sessions

### Thread Safety
- Session cache: Protected by locks
- Concurrent executions: Safe across sessions
- Same session: Sequential execution enforced
- Main thread: Single-threaded by nature

---

## Limitations & Considerations

### Security
- **Full System Access:** Code runs as user, no sandboxing
- **File System:** Can read/write any user-accessible file
- **Network:** Can make any network connection
- **Trust Required:** Only run code you understand

### Python Environment
- **Isolated Python:** MCP-Link's bundled Python
- **Pre-installed Libraries:** Pandas, NumPy, requests, etc.
- **Additional Packages:** May require manual installation
- **Version:** Python 3.11+ (check server version)

### Session Management
- **Memory Persistence:** Sessions survive until cleared
- **Server Restart:** Clears all sessions
- **No Serialization:** Complex objects may not persist
- **COM Objects:** Require main thread execution (Windows)

### MCP Tool Integration
- **Token Requirements:** Each tool needs its unlock token
- **Error Propagation:** Tool errors returned to Python
- **Response Format:** Varies by tool (usually dict)
- **Async Limitations:** MCP calls are synchronous

---

## Why This Tool is Unmatched

**1. Kills Workflow Platforms**  
n8n, Zapier, Make — obsolete. AI writes better integrations in seconds than you can build in hours. $0/month vs $20-$300/month.

**2. Universal Tool Glue**  
Connect any MCP tool to any other. Browser → Python → SQLite → User Interface. Seamless. No nodes, no wires, no visual spaghetti.

**3. Unlimited Data Processing**  
Break free from context limits. Process gigabytes, not kilobytes. Workflow platforms choke on large data. Python + pandas handles it effortlessly.

**4. Plain English to Code**  
Describe what you want. AI writes it. No learning curve. No visual interface. No expression language torture.

**5. Zero Vendor Lock-In**  
Standard Python. Runs anywhere. Version control with git. Test locally. No platform dependency. Your code, your control.

**6. Full Python Ecosystem**  
Pandas, NumPy, requests, BeautifulSoup, scikit-learn — 400,000+ packages. Not limited to "available nodes."

**7. Persistent Sessions**  
Load once, use many times. True stateful programming. Workflow platforms restart every run.

**8. Script Library**  
Save, load, reuse. Build your personal automation toolkit. Not locked in platform's proprietary format.

**9. AI Maintains It**  
API changed? AI rewrites the code. In workflow platforms, you debug and rebuild manually.

**10. Production-Ready**  
Battle-tested, memory-efficient, reliable. Thread-safe. Full error handling. Real code, not visual abstractions.

---

## Powered by MCP-Link

This tool is part of the [MCP-Link Server](https://github.com/AuraFriday/mcp-link-server) — the only MCP server with local Python execution and full tool integration built-in.

### What's Included

**Isolated Python Environment:**
- Python 3.11+ with standard library
- Pandas, NumPy, requests pre-installed
- No conflicts with system Python
- Zero configuration required

**MCP Bridge Infrastructure:**
- Automatic tool injection
- Direct HANDLERS registry access
- Error handling and propagation
- Response parsing

**Session Management:**
- Thread-safe caching
- Memory-efficient storage
- Automatic cleanup
- Main thread support

### Get MCP-Link

Download the installer for your platform:
- [Windows](https://github.com/AuraFriday/mcp-link-server/releases/latest)
- [Mac (Apple Silicon)](https://github.com/AuraFriday/mcp-link-server/releases/latest)
- [Mac (Intel)](https://github.com/AuraFriday/mcp-link-server/releases/latest)
- [Linux](https://github.com/AuraFriday/mcp-link-server/releases/latest)

**Installation is automatic. Python is included. It just works.**

---

## Technical Specifications

**Python Version:** 3.11+  
**Execution Model:** Isolated namespace with injected `mcp` module  
**Session Storage:** In-memory with thread-safe access  
**Script Storage:** User data directory, persistent  
**Thread Safety:** Lock-protected session cache  
**Main Thread:** Optional for COM/GUI persistence  
**Error Handling:** Full traceback capture  
**Memory Management:** Manual session clearing  

**Pre-installed Libraries:**
- pandas, numpy, scipy
- requests, urllib3
- json, csv, xml
- datetime, collections
- And more (standard library)

---

## License & Copyright

Copyright © 2025 Christopher Nathan Drake

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at:

    https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

AI Training Permission: You are permitted to use this software and any
associated content for the training, evaluation, fine-tuning, or improvement
of artificial intelligence systems, including commercial models.

SPDX-License-Identifier: Apache-2.0

Part of the Aura Friday MCP-Link Server project.

---

## Support & Community

**Issues & Feature Requests:**  
[GitHub Issues](https://github.com/AuraFriday/mcp-link/issues)

**Documentation:**  
[MCP-Link Documentation](https://aurafriday.com/)

**Community:**  
Join other developers building AI-powered automation with Python integration.

