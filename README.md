# TakeNote

## Demo Development

### Setup github oauth

https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app

Click the **New OAuth App** button.

- **Application name**: TakeNote Development
- **Homepage URL**: `http://localhost:5000`
- **Authorization callback URL**: `http://localhost:5000/api/auth/callback`

### Clone and install.

```bash
git clone git@github.com:taniarascia/takenote
cd takenote
# Build Docker image
docker build --build-arg CLIENT_ID=Ov23liy80Tb3Gfvu6JMT -t suhail_takenote:latest .
# Run Docker container in port 5000
docker run \
-e CLIENT_ID=Ov23liy80Tb3Gfvu6JMT \
-e CLIENT_SECRET=<see_standardnotes> \
-e NODE_ENV=development \
-p 5000:5000 \
suhail_takenote:latest
```

Go to `localhost:5000` to view the app.

the data will be stored in https://github.com/suhailvs/takenote-data