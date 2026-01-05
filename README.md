# VDR Global Ltd Website

Static company website for Apple Developer Program enrollment.

## Setup Instructions

### 1. GitHub Pages Setup

1. Create a new repository on GitHub (e.g., `vdr-global-site`)
2. Upload all files to the repository
3. Go to repository **Settings** → **Pages**
4. Under **Source**, select **Deploy from a branch**
5. Select **main** branch and **/ (root)** folder
6. Click **Save**

Your site will be available at: `https://yourusername.github.io/vdr-global-site/`

### 2. Namecheap Domain Configuration

**Important:** Configure BOTH apex domain (vdrglobal.co.uk) and www subdomain for best compatibility.

1. In Namecheap dashboard, go to **Domain List** → select your domain → **Advanced DNS**

2. **Remove any existing A or CNAME records** for `@` and `www` that might conflict

3. Add the following DNS records:

   **A Records for Apex Domain** (add 4 records for `@`):
   ```
   Type: A Record
   Host: @
   Value: 185.199.108.153
   TTL: Automatic
   
   Type: A Record
   Host: @
   Value: 185.199.109.153
   TTL: Automatic
   
   Type: A Record
   Host: @
   Value: 185.199.110.153
   TTL: Automatic
   
   Type: A Record
   Host: @
   Value: 185.199.111.153
   TTL: Automatic
   ```

   **CNAME Record for www subdomain**:
   ```
   Type: CNAME Record
   Host: www
   Value: finsummary.github.io
   TTL: Automatic
   ```

4. Go back to GitHub repository **Settings** → **Pages**
5. Under **Custom domain**, enter: `vdrglobal.co.uk` (GitHub will automatically add www as alternate)
6. Click **Save**
7. Wait 1-2 minutes, then click **Check again** to verify DNS configuration
8. Once DNS is verified, check **Enforce HTTPS** (may take up to 24 hours to activate)

### 3. Troubleshooting DNS Issues

If you see "Domain does not resolve to the GitHub Pages server" error:

1. **Verify DNS records are correct:**
   - Use online DNS checker tools (e.g., whatsmydns.net) to verify A records point to GitHub IPs
   - Verify CNAME for www points to `finsummary.github.io`

2. **Wait for DNS propagation:**
   - DNS changes can take 1-48 hours to propagate globally
   - Check again in GitHub Pages settings after waiting

3. **Remove conflicting records:**
   - Make sure there are no other A or CNAME records for `@` or `www` that conflict
   - Remove any URL Redirect records that might interfere

4. **Verify CNAME file:**
   - The `CNAME` file should contain only: `vdrglobal.co.uk` (no www, no trailing slash)
   - GitHub automatically handles www subdomain when apex domain is configured

### 4. Email Setup (Namecheap)

To set up `support@vdrglobal.co.uk`:

1. In Namecheap, go to **Domain List** → your domain → **Email Forwarding**
2. Add email forwarding:
   - **Forward to**: your personal email
   - **Forward from**: support@vdrglobal.co.uk

Or use Namecheap Private Email service for a full email account.

## Verification

After DNS propagation (can take up to 48 hours):

- ✅ Site loads at `https://vdrglobal.co.uk`
- ✅ HTTPS is enabled
- ✅ All pages accessible (index, support, privacy, terms)
- ✅ Email `support@vdrglobal.co.uk` works

## Files Structure

```
/
├─ index.html      (Home page)
├─ support.html    (Support page)
├─ privacy.html    (Privacy Policy)
├─ terms.html      (Terms of Use)
├─ CNAME           (Custom domain)
└─ .nojekyll       (Disable Jekyll processing)
```

