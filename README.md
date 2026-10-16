# tito-auth

Telegram Mini App that asks for Face ID / Touch ID before my personal Telegram bot runs a sensitive action on my Mac.

The page holds no secrets. On enrollment it creates a P-256 key pair in the browser, stores the private key in the phone's secure storage through Telegram's `BiometricManager`, and sends only the public key to the bot. Each approval signs a one-time nonce after Face ID; the bot verifies the signature.
