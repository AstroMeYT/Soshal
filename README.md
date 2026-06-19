# Soshal

Soshal is a privcy-focused social network built from the ground up. It is made for scalability and the ability to make your own network. This repo is the client file.

## How to use Soshal

Soshal is like any other social network. It has the same look as Facebook's UI, just for ease of switching. Other clients created by other people may also be available.

## Accounts

When you create an account, that account is saved locally. Every time you log on, you will be signed in sutomatically. The only time that may not happen is if the server has restarted, or you are running out of storage.

## Security

This is some nitty gritty stuff you are about to read. When you create an account, a cryptographic (hash) key is created that is signed with your username, passowrd, and a random key that is reset on logout for security. The cool thing about this hash key is that it cannot be unhashed, making it impossible to get your password out of it. If you suspect someone is in your account, log out, and log back in. This generates a new key that is still hashed with the same details, but a different overall key. All secure API calls, such as posting, following, liking, or anything like those require a valid hash in the header.
