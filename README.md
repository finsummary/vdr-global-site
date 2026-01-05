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

#### Option A: Using Apex Domain (vdrglobal.co.uk)

1. In Namecheap dashboard, go to **Domain List** → select your domain → **Advanced DNS**
2. Add/Edit the following DNS records:

   **A Records** (add 4 records):
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

3. Go back to GitHub repository **Settings** → **Pages**
4. Under **Custom domain**, enter: `vdrglobal.co.uk`
5. Check **Enforce HTTPS** (will be available after DNS propagates)

#### Option B: Using Subdomain (www.vdrglobal.co.uk)

1. In Namecheap **Advanced DNS**, add:

   **CNAME Record**:
   ```
   Type: CNAME Record
   Host: www
   Value: yourusername.github.io
   TTL: Automatic
   ```

2. In GitHub Pages settings, enter: `www.vdrglobal.co.uk`

### 3. Update CNAME File

If your domain is different from `vdrglobal.co.uk`, update the `CNAME` file with your actual domain name.

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

