## How to use Open AI Codex in CLI mode for Smart Working

### Step 0 - Ubuntu Setup
- Install Ubuntu and WSL - Codex only works 

### Step 1 - To start Ubuntu
```
wsl -d Ubuntu
```

### Step 2 - To install NodeJS and curl
```
sudo apt update
sudo apt install -y curl nodejs npm
```

### Step 3 - Check versions
```
node -v
npm -v
curl --version
```

### Step 4 - To install Codex
```
sudo npm install -g @openai/codex
codex --version
```

### Step 5 - To Set UP a project
```
mkdir codex-demo
cd codex-demo
```

### Step 6 - To Start a project 
```
codex --sandbox workspace-write
```

### Step 7 - Set API Key
```
echo 'export OPENAI_API_KEY="Your OpenAI API Code"' >> ~/.bashrc
source ~/.bashrc
```

### Step 8 - To check the API
```
echo $OPENAI_API_KEY
```

### Others
- **To check Usage**
Link: https://platform.openai.com/usage
- **To set soft limits**
Link: https://platform.openai.com/account/billing/limits

