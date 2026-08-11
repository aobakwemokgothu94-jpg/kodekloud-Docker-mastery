# Level 2 – Task 5: Restart Policies

## Step 1: Run a Container with Restart Policy
docker run -d --name web --restart=always -p 8080:80 nginx:latest

- --restart=always → container will restart automatically if it crashes or when Docker restarts

## Step 2: Other Restart Policy Options
- no → default, never restart
- on-failure → restart only if container exits with non-zero status
- always → always restart regardless of exit status
- unless-stopped → restart unless explicitly stopped by user

Example:
docker run -d --name app --restart=on-failure:3 myapp:latest

## Step 3: Verify Restart Policy
docker inspect -f "{{ .HostConfig.RestartPolicy }}" web

## Step 4: Test Restart Behavior
- Stop Docker service, then start it again
- Container with `--restart=always` will come back automatically

