# My WorkLog

# 📑 Worklog – ALX Projects

This worklog documents the progress, steps taken, issues encountered, and resolutions for the **ALX Intermediate Frontend** and **ALX Backend Python** projects.

---

## 🖌️ Frontend Project: 0x03-sass_scss

### **Date:** 2025-09-13  
### **Goal:** Learn and implement Sass features (variables, nesting, mixins)

| **Task** | **Steps Taken** | **Outcome** | **Notes / Issues** |
|---------|----------------|-------------|--------------------|
| **Sass Installation** | - Installed Node v20.16 via `nvm` <br> - Installed Sass v3.7.4 via `npm install sass -v 3.7.4` <br> - Created `0-installation-script` documenting steps | ✅ Sass installed successfully | No issues |
| **Debug Output** (`0-debug_log.scss`) | - Wrote SCSS using `@debug` directive <br> - Tested with `npx sass 0-debug_log.scss | head -n 0` | ✅ Printed `Hello world` to debug output | Learned how `@debug` works |
| **Variables** (`1-color_variable.scss`) | - Declared `$text-color: #3D3D3D` <br> - Applied to `body` and `p` tags | ✅ Compiled CSS applied color properly | Great intro to variables |
| **Nested Declarations** (`2-nested_tag.scss`) | - Removed margin & padding for `body` <br> - Added nested `p` selector with margin | ✅ Output matches expected format | Practiced nesting syntax |
| **Mixins** (`3-mixin_margins.scss`) | - Created `@mixin set-margins($value)` <br> - Applied with different values to `body` & `div` | ✅ Generated correct CSS | First experience with mixins |

---

## 🖥️ Backend Project: python-decorators-0x01

### **Date:** 2025-09-13  
### **Goal:** Learn decorators for logging, DB handling, transactions, retries, caching

| **Task** | **Steps Taken** | **Outcome** | **Notes / Issues** |
|---------|----------------|-------------|--------------------|
| **Query Logging** (`0-log_queries.py`) | - Implemented `log_queries` decorator <br> - Used `datetime.now()` to timestamp SQL logs | ✅ Logs query before execution | Needed to add `from datetime import datetime` after checker failed |
| **Auto DB Connection** (`1-with_db_connection.py`) | - Implemented `with_db_connection` decorator <br> - Opened connection, passed to function, closed automatically | ✅ Connection opened/closed safely | Learned `functools.wraps` preserves function metadata |
| **Transactions** (`2-transactional.py`) | - Added `transactional` decorator <br> - Used `conn.commit()` & `conn.rollback()` in `try/except` | ✅ Transactions now atomic | Critical for preventing partial writes |
| **Retry on Failure** (`3-retry_on_failure.py`) | - Implemented decorator with retries & delay <br> - Used `time.sleep()` between attempts | ✅ Retries query up to 3 times | Good intro to resilience patterns |
| **Caching** (`4-cache_query.py`) | - Added in-memory `query_cache` dictionary <br> - Returned cached result if query seen before | ✅ Subsequent calls avoid redundant DB fetch | Major performance boost |

---

## 🗄️ Backend Project: python-context-async-perations-0x02

### **Date:** 2025-09-13  
### **Goal:** Master context managers and async database operations

| **Task** | **Steps Taken** | **Outcome** | **Notes / Issues** |
|---------|----------------|-------------|--------------------|
| **DatabaseConnection Context Manager** (`0-databaseconnection.py`) | - Created class with `__enter__` & `__exit__` <br> - Managed open/close connection automatically | ✅ Query results printed successfully | Very clean resource management |
| **ExecuteQuery Context Manager** (`1-execute.py`) | - Accepted query & params in constructor <br> - Executed query in `__enter__` and returned results | ✅ Cleaned up code by reusing logic | First experience passing params to context manager |
| **Async Concurrent Queries** (`3-concurrent.py`) | - Used `aiosqlite` for async DB access <br> - Implemented `async_fetch_users()` & `async_fetch_older_users()` <br> - Used `asyncio.gather()` for concurrency | ✅ Both queries fetched in parallel | Learned `asyncio.run()` entry point |

---

## ✅ Final Actions
- **Staging & Commit:** Staged only required project files, excluded `.json` and environment files using `.gitignore`.
- **Push:** Successfully pushed all tasks to GitHub.
- **Verification:** Passed all checker requirements after fixes.

---

## 🎯 Lessons Learned
- How to use **Sass features**: variables, nesting, mixins
- Writing **Python decorators** for logging, connection handling, retries, caching
- Implementing **context managers** for database safety
- Running **asynchronous database operations** with `asyncio.gather`
- Using Git effectively for **staging, committing, and pushing** changes

---

