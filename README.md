### Download release version
2025a

### Update
1. With do the modification to official docker image `sharelatex/sharelatex`, the docker image now have full TexLive pkgs, namely `ichinana-seu/sharelatex-modi:2025a`. 
2. Chinese fonts (simsun, simhei, simkai, simfang, etc.) are extracted from windows, and added into `ichinana-seu/sharelatex-modi:2025a`. 
3. overleaf-toolbox (i.e. `sharelatex-modi-2025a-manager` here) has been modified with: 
    a) `??/config/ ` files in this folder has been modified to link a full-version `sharelatex/sharelatex` (i.e. `ichinana-seu/sharelatex-modi:2025a` here)
    b) `??/bin/up` has been modified to ignore version detection and allow irregular version like `2025a`

### Quick to Start
1. Extract `sharelatex-modi-2025a.tar.7z.001` and `sharelatex-modi-2025a.tar.7z.002` to `sharelatex-modi-2025a.tar` first.
2. To see how to setup your own overleaf server, refer to `README.MD`
3. Step One: `docker load -i .\mongo-6.0.tar`, `docker load -i .\redis-6.2.tar`, `docker load -i .\sharelatex-modi-2025a.tar`
4. Step Two: Extract `sharelatex-modi-2025a-manager.tar.gz`.
5. Step Three: `cd /????/????/sharelatex-modi-2025a-manager`, check `??/config/overleaf.rc ` to change the default 80/TCP port. next, run `bin/up`, wait, then ctrl+c to terminate debug interface. `bin/start` to start. `bin/stop` to stop.
6. Try `http://ip:host(80 default)` to visit overleaf. Try` http://ip:host(80 default)/lauchpad` to set an admin account

### Tips
1. If you are using Docker Desktop on Windows, it is recommended that you install a docker in WSL by which you can control the same docker both on Docker Desktop Windows and WSL. 
2. `sharelatex-modi-2025a-manager (overleaf-toolbox)` should be run under Linux environment.
3. Attention: user data stored in `/????/????/sharelatex-modi-2025a-manager/data`
