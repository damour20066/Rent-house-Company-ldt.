# How to Fix Gmail Email Sending

## Step 1: Enable 2-Step Verification
1. Go to: https://myaccount.google.com/security
2. Find **"2-Step Verification"** and turn it ON
3. Follow the steps to verify your phone number

## Step 2: Create App Password
1. Go to: https://myaccount.google.com/apppasswords
   (Or search "App passwords" in Google search)
2. Select **App**: Mail
3. Select **Device**: Other (type "Node.js" or "Computer")
4. Click **Generate**
5. Copy the 16-character password shown (format: xxxx xxxx xxxx xxxx)

## Step 3: Update server.js
1. Open `backend/server.js`
2. Find lines 12-13:
```javascript
user: 'tumenyekwivura@gmail.com',
pass: 'your-app-password'
```
3. Replace `'your-app-password'` with the 16-character code you copied

## Step 4: Restart Server
```bash
cd backend
node server.js
```

Now verification codes will be sent to user emails!
