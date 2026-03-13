# Phone OTP Setup

## Option 1: Africa's Talking (Recommended for Rwanda)
1. Go to https://account.africastalking.com
2. Create an account (free)
3. Get your API Key from Settings
4. Update `backend/server.js`:
```javascript
const africaTalking = at({
    apiKey: 'YOUR_ACTUAL_API_KEY',
    username: 'YOUR_USERNAME'
});
```

## Option 2: Twilio
1. Go to https://www.twilio.com
2. Create account and get free $15 credit
3. Get phone number, Account SID, and Auth Token

## How Phone OTP Works:
1. User enters phone number during signup
2. System sends 6-digit code via SMS
3. User enters code to verify phone
4. Only verified users can login

## Testing:
Until you configure SMS, the OTP code will be shown in an alert for testing.
