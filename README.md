# python_mcp
A python tool callable by MCP which can itself make MCP tool calls as well

# Python Execution — Your AI's Programming Superpower

> **Execute Python locally. Call any MCP tool. Process unlimited data.** Your AI can finally write and run code that bridges all your tools together.

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey.svg)](https://github.com/AuraFriday/mcp-link-server)

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

**1. Universal Tool Glue**  
Connect any MCP tool to any other. Browser → Python → SQLite → User Interface. Seamless.

**2. Unlimited Data Processing**  
Break free from context limits. Process gigabytes, not kilobytes.

**3. Persistent Sessions**  
Load once, use many times. True stateful programming.

**4. Script Library**  
Save, load, reuse. Build your personal automation toolkit.

**5. Full Python Power**  
Pandas, NumPy, JSON, CSV, XML — all available. No restrictions.

**6. Zero Configuration**  
Python environment included. Libraries bundled. Just works.

**7. Thread-Safe**  
Multiple sessions, concurrent execution, no conflicts.

**8. Main Thread Support**  
COM objects, GUI libraries — special cases handled.

**9. Complete Error Handling**  
Tracebacks, error messages, debugging support.

**10. Production-Ready**  
Battle-tested, memory-efficient, reliable.

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

