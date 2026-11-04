To protect your Jellyfin server from automated scanners and bots, the industry-standard approach is to implement **Security Hardening** via Reverse Proxying and Access Control Lists (ACLs). These methods are used by administrators worldwide to secure any web-facing application against unwanted traffic and unauthorized access.

Here is how these technical measures work:

### 1. Implement a Reverse Proxy

A reverse proxy acts as an intermediary between the public internet and your Jellyfin server. Instead of exposing your Jellyfin instance directly on port `8096` (or whatever port you use), the proxy handles all external traffic first.

- **Tools:** You can use **Nginx**, **Caddy**, or **Apache**.
- **How it helps:** When a bot scans for "Jellyfin," it typically looks for specific ports and default headers. A reverse proxy terminates this connection using SSL/TLS (HTTPS), meaning the traffic now appears as standard, encrypted web traffic to any outside observer rather than raw media server data.

### 2. Strip Server Fingerprinting

Most bots use automated scanners that send a "HEAD" or simple GET request and look at the **HTTP Headers** returned by your server to identify what software is running (e.g., `Server: Jellyfin`). If it identifies the software, it can then automatically probe for known vulnerabilities or specific endpoints like `/LiveTv/`.

- **The Fix:** By configuring Nginx or Caddy as a reverse proxy, you can configure the "upstream" to strip out these identifying headers and replace them with generic information (like `Server: Cloudflare` or just omitting it entirely).
- **Result:** The bot sees your server as an anonymous web server. While they may still try standard paths (`/api`, `/LiveTv`), the lack of a clear "Jellyfin" label forces the bot to be much more aggressive and less accurate, often causing it to skip over your instance in favor of easier targets.

### 3. Enforce Strict Authentication (ACLs)

You can use your reverse proxy to enforce authentication _before_ the traffic even reaches Jellyfin's internal logic.

- **How it works:** You set up "Basic Auth" or a second layer of password protection at the Nginx/Caddy level.
- **The Benefit:** If a bot tries to scrape an M3U file from your server, the proxy will respond with `401 Unauthorized` before Jellyfin ever processes the request and reveals what files are available.

### 4. IP Whitelisting (Firewalling)

If you do not need to access your media server while away from home, the most effective way to hide it is to block all public traffic entirely via your router or firewall software (like **UFW** on Linux).

- **Remote Access:** If remote access _is_ required, rather than opening a port directly in your router's port forwarding section, you should use a trusted VPN service like **WireGuard** or **Tailscale**.
- **Why it helps:** This creates a "tunnel." The bot cannot see your server because it isn't on the public internet; the traffic only exists within an encrypted, private tunnel that requires a valid key to enter.

### 5. Dynamic/Randomized Paths

While Jellyfin uses standard API endpoints by design (which is great for compatibility), you can use "URL rewriting" in Nginx or Caddy to move those endpoints to obscure paths if your clients support it. However, this is often difficult because many third-party apps and the official client expect specific URL structures (`/System`, `/Users`). The header-stripping method (Step 2) is generally more effective for hiding from bots while keeping your server fully functional.