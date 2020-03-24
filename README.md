# dockertraining

C:\Users\Alfredo\Desktop\dockertraining_alfredo_medina>docker build -f "C:\Users\Alfredo\Desktop\dockertraining_alfredo_medina\dockertraining_alfredo_medina\Dockerfile" --force-rm -t dockertrainingalfredomedina:dev "C:\Users\Alfredo\Desktop\dockertraining_alfredo_medina"
C:\Users\Alfredo\Desktop\dockertraining_alfredo_medina>docker run --name Site1 -p 8085:80 c1a9d987e34b
C:\Users\Alfredo\Desktop\dockertraining_alfredo_medina>docker run --name Site2 -p 8086:80 -e "storename"="Plano" c1a9d987e34b

C:\Users\Alfredo\Desktop\dockertraining_alfredo_medina>docker images
REPOSITORY                                       TAG                   IMAGE ID            CREATED             SIZE
dockertraining2020/dockertrainingalfredomedina   dev                   6ad84aed9240        5 minutes ago       351MB
dockertrainingalfredomedina                      latest                6ad84aed9240        5 minutes ago       351MB
<none>                                           <none>                b99542807619        5 minutes ago       756MB
dockertrainingalfredomedina                      dev                   c1a9d987e34b        9 hours ago         351MB
<none>                                           <none>                919baab856f6        9 hours ago         756MB
dockertraining_alfredo_medina                    dev                   2fda7a9465f9        10 hours ago        351MB
<none>                                           <none>                9ddcc62c3466        11 hours ago        346MB
<none>                                           <none>                fd1fb0ca98a0        14 hours ago        346MB
mcr.microsoft.com/dotnet/core/sdk                3.1-nanoserver-1903   fc0cc7349c8e        4 days ago          736MB
mcr.microsoft.com/dotnet/core/aspnet             3.1-nanoserver-1903   5e02b17ec74f        4 days ago          346MB
hello-world                                      latest                bc5d255ea81f        4 weeks ago         251MB

C:\Users\Alfredo\Desktop\dockertraining_alfredo_medina>docker ps -a
CONTAINER ID        IMAGE               COMMAND                   CREATED             STATUS                    PORTS                  NAMES
7dc0deced6f0        c1a9d987e34b        "dotnet dockertraini…"    58 minutes ago      Up 58 minutes             0.0.0.0:8086->80/tcp   Site2
aa62a3556521        c1a9d987e34b        "dotnet dockertraini…"    9 hours ago         Up 9 hours                0.0.0.0:8085->80/tcp   Site1
bcf62a484c93        hello-world         "cmd /C 'type C:\\hel…"   17 hours ago        Exited (0) 17 hours ago                          magical_benz
0a1d869698c0        hello-world         "cmd /C 'type C:\\hel…"   17 hours ago        Exited (0) 17 hours ago                          jovial_spence
3f9e6d5e9a2a        hello-world         "cmd /C 'type C:\\hel…"   13 days ago         Exited (0) 10 hours ago                          vigorous_wescoff
