# Real User Monitoring (RUM)

## Step 1: What is RUM?

Real User Monitoring (RUM) means monitoring actual user interactions with your application (browser/mobile).

### What it captures:
- Page load time
- User actions (clicks, navigation)
- Errors (JS errors, crashes)
- User sessions
- Geography, browser, device

### Key Idea:
Not synthetic, not backend — real users in real time

## Step 2: Example

User opens your app:
```
Browser → Frontend → Backend → DB
```

RUM captures:
- How long page took to load
- Where user clicked
- If error happened in UI

## Step 3: Two Ways to Enable RUM

### 1. OneAgent-Based RUM (Automatic)

**How it works:**
- You install Dynatrace OneAgent on your server
- It automatically injects JavaScript into HTML responses

**What happens:**
1. User opens webpage
2. OneAgent injects RUM JS
3. Browser sends user data to Dynatrace

**Key Advantages:**
- Zero manual setup
- Auto correlation (frontend ↔ backend)
- Full observability (logs + metrics + traces + user)

### 2. Agentless RUM (Manual Injection)

**How it works:**
You manually add a JavaScript snippet into your app:

```javascript
<script src="dynatrace-rum.js"></script>
```

**Used when:**
- No backend access
- Static websites (CDN, S3)
- Third-party apps
- Security restrictions

**Limitations:**
- No automatic backend correlation
- Limited visibility
- Manual effort

## Core Difference

| Feature | OneAgent RUM | Agentless RUM |
|---------|--------------|---------------|
| Setup | Automatic | Manual |
| JS Injection | Auto | Manual |
| Backend correlation | ✅ Full | ❌ Limited |
| Visibility | End-to-end | Frontend only |
| Effort | Low | Medium |

## Step 4: How RUM Connects to Observability

| Pillar | RUM Contribution |
|--------|-----------------|
| Metrics | Page load time, user timing |
| Logs | JS errors |
| Traces | User → backend request flow |

RUM = entry point of user experience observability

## Real-World Architecture

```
RUM → captures user action
OneAgent → traces backend
Grail → stores everything
DQL → analyze
```

## Memory Trick

- **OneAgent RUM** = Automatic + Deep
- **Agentless RUM** = Manual + Limited