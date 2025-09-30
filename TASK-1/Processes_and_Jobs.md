# Processess And jobs

## Listing Process 

### Solve
**Flag:** `pwn.college{QEGjqW50ZTYTFNqOiLvsD6ERgGz.QX4MDO0wSM1EzNzEzW}`

for this we had to use the ps command together with -ef and then from the path of the process running i had to figure out the run file and use that path to obtain the flag in the terminal.

```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 08:21 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/p
root           7       1  0 08:21 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 08:21 ?        00:00:00 /challenge/4912-run-18322
root         135     132  0 08:21 ?        00:00:00 sleep 6h
hacker       146       1  0 08:21 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893
hacker       150     146  0 08:21 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       164     150  0 08:22 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/4912-run-18322
Yahaha, you found me! Here is your flag:
pwn.college{QEGjqW50ZTYTFNqOiLvsD6ERgGz.QX4MDO0wSM1EzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

### New Learnings
I learnt how to see which process is running in the shell together with its detaols.
### References 
-NA


## Killing Process

### Solve
**Flag:** `pwn.college{k9-fZ5FNbn-Ijz3gjcIFnh0kerg.QXyQDO0wSM1EzNzEzW}`

TO solve this challenge i had to first use the "ps -ef" command to obtain the PID of the processs then used that PID to kill that process and then run the /challenge/run command to obtain the flag.

```bash
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 08:28 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/p
root           7       1  0 08:28 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 08:28 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 08:28 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 08:28 ?        00:00:00 sleep 6h
hacker       148       1  0 08:28 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893
hacker       152     148  0 08:28 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       162     152  0 08:28 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run 
Great job! Here is your payment:
pwn.college{k9-fZ5FNbn-Ijz3gjcIFnh0kerg.QXyQDO0wSM1EzNzEzW}
```

### New Learnings
I learnt how to kill a process from a shell.
### References 
-NA-


## Interrupting Process

### Solve
**Flag:** `pwn.college{IaGECHUi3VRW4WAB8LyCh4k6Aj0.QXzQDO0wSM1EzNzEzW}`

For this I just had to run the command and give the ^c to interrupt and obtain the flag.

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{IaGECHUi3VRW4WAB8LyCh4k6Aj0.QXzQDO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Killing Misbehaving Processes

### Solve
**Flag:** `pwn.college{kgygVaRLxHcM7PELxOhY6EgNAeQ.0FNzMDOxwSM1EzNzEzW}`

first I found out the PID of the decoy process and then killed it then i run the /challenge/run but it didnt give me any output so i interrupted the process and run the cat function on the file and it had many decoys so i waited untill all the decoyed were pipped out and then again run the .challenge/run command and this time i got the correct flag.

```bash
hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 08:42 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/p
root           7       1  0 08:42 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 08:42 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 08:42 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 08:42 ?        00:00:00 su -c exec /challenge/decoy > /tmp/
root         140     138  0 08:42 ?        00:00:00 sleep 6h
root         141     137  0 08:42 ?        00:00:00 sleep 6h
hacker       142     139  0 08:42 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       153       1  0 08:42 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893
hacker       157     153  0 08:42 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       167     157  0 08:42 pts/0    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run 
Sending the flag to /tmp/flag_fifo!
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run 
Sending the flag to /tmp/flag_fifo!
^C
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{9MumwurbHbUdpQL-1Oh.5ZcgvB8dBW63mrlgZp0LiNEKhLg}
pwn.college{5SoSrjWHiYQDEyWVGO4UtVCHE4CnkHaeMgHM73iz-RedNuY}
pwn.college{ZvyhH6VzE7H1QmpXlMe4vJb21mz6QtIBbpCpswgOm4vWApq}
pwn.college{dWpd1QgxfiuA2Qy22EKSL3t9UmdOVYbFSIOGBovm8KeLvKM}
pwn.college{JgrdxPbR6HewwyXZxQlJyEyfHOIJ6IIq5nc-aXrUnA-1b6A}
pwn.college{YQtW7XpQLmbq5JynXqCyi4R5yGk7pm61KO8-8FOJDjXVN9H}
pwn.college{bmkaTobXn4ZDISr14xcvXaRSA3lyqzbvDhNjbotFmfi2EPE}
pwn.college{1DuSZO2OlM1ZyftQ8kB3TaFdUeJNuJ2yBOO03uaXADnX-kz}
pwn.college{vZR43rHpaDRY8rvCgfy.hrutgfP1j1GIXfoOfkH0wS71798}
pwn.college{jVvRzRWu4oLTU5ETy0Km9OrMiYzspS874BOIMugoW.5DtCY}
pwn.college{63KNRiT0h0AhLAem8z4pfQTiNk3MSYFrmwbQgw7RUVp5SZv}
pwn.college{sA9hzGDNgvAi5c68dK3usp2jx.2ZPch1CtUw3WznIXPYcnA}
pwn.college{diSyp6lkRdsjV59s6PglOHH4CkxYtwMR6-Mwmzw.-PlYmMb}
pwn.college{J0OhlwTX7FKU014O3iI7L66LR6W9WH9tnAgC1UJswWz1n1a}
pwn.college{dVgMJMYBFdNaGjfAxLKHde1vblWsy-XQklYLUGkwZ2hIhC0}
pwn.college{u2UoxZi.6ii5JO3iKReHAWNfdmX1NLYQpKEBEtOvzMniE79}
pwn.college{UdC3-KMBEwUv87uAuVvN3hFka-KFWM3TrSDyFanYljzH.3w}
pwn.college{.YjHWx3eilc9-lM30cQybk.0i.rAS26PEP-Jjl5DAa5wtZ3}
pwn.college{DknjdpzHznfHJ9QIxkPltdXvJ19NjgiDDQni4cVX7ECNKy-}
pwn.college{HSXGPfl2.sws7CjPbqYO43.cwV.9oWUKZc47H.xBA0-FOkh}
pwn.college{bE4W1BiBsFHws3LT5QP-sCtoe6XnMWj8A-Bf0sDV1BN96rD}
pwn.college{m7OiVKaE4hc2AS6MKCoOicWk.2ePlS-fYu0SixbK4kiFAQ8}
pwn.college{PGjUISqg5omc93RsI0pkuujrRphlUQE6r5pH2SueQbGPKnM}
pwn.college{iW0zI0bSIZuHHAa1KZqQ7gXltCHveBKHXSEMwfq-HiPytOr}
pwn.college{d-mah5XcDtwDzVVsPlzqC56eYxHhC-NYD.G.nYrNpaF1SLT}
pwn.college{yDJ3STsh2pPp8UZDipvqP2CoeYU6NPkIKwvwDp9ETdVL6Qe}
pwn.college{Iu.vyaxwOnQTwsc1OZhsKE2WC-qBIlRGtYX0xvurIenEXkG}
pwn.college{359FiAoa3-U4FNRVGol-WQ7NYuVis-bpvQx5DZFwnTYkH7W}
pwn.college{8XtLjo8pEtC2QpOWgn8tXdBOwB2Jq718Fgvb4y2pbyTHXgZ}
pwn.college{haMdTQ3ttdfuBkOxwwZNz0sy2Sa4pGdhk6b5vqau5IDhbvY}
pwn.college{.i3dn3XQ2zfSzuF.tBqWrlGcbPT6VLdcwEqQc6ihyywfJ2F}
pwn.college{Df5iM.q6FOyXp2SjsInq7kEf8iu8dcymM2Q7kkQYJAUMtte}
pwn.college{KPpDo7uKDeQVYuWZ1vKBtW0siJlGwaM0kGvQ9Ih3enZXmH.}
pwn.college{h9jJaRkBxlcczpVaOG.7jy44MvD69CqgMiVCqlxeTgawvap}
pwn.college{JPpngxJoFf.9eBfaltKLTNZeHgRCQHLeAmRQjrJvnlnfAbU}
pwn.college{8j7zMrc4W64GZdEmOTVdS72MG9VR8.LU0EgpbqAc4HqerNG}
pwn.college{3JDNswB5zNEjAZVlIsKQLl73VfMWGcAUe8a.4eQwBvpgFJ5}
pwn.college{tNEpWIPzwlVD36FncD3gJ-uzlS0M4NyrgJCTx9woClQztY3}
pwn.college{0Hs-Sq-4P5f0uDkbITv-imJKcvb3X5X4fSnPz0zMRB2owUv}
pwn.college{8U-XDgp8h0CxHMGFyhUCnsw5.MfDRUBr1mywBgUQeKe6Z40}
pwn.college{kFubQXrPLtvqctnd34eTDPCntv26I08Or6q9R98mAv8ObdT}
pwn.college{dgvZ5jdpMXZrTFAn1tq1ovhcLcjpQ9fwtqCNrWmfY2rza-3}
pwn.college{IqfOsCVJjj69F1unkKblxg.g2b9XcJOsWILT32RjY.dmTEF}
pwn.college{jMc6rvTvpN9xNY3s.UTW1TUqcEc25cqKbDWkJuayxoy2nxj}
pwn.college{PZztqkhzmuTnkINYG6Ew-YFWgd0hEslADbb2CMJMXm5R2v0}
pwn.college{HX.I7upKh.ZjilRVZUkDDfyHOmH8OC.kNl-x8n6OkSkV5v7}
pwn.college{1XnT8A2kyvOujMC5Hp1l2hr1pptXw.CUcQHpUWb6WXwadVx}
pwn.college{7rjGIRraTsXEykjkpPSmxDRNSPcZnzKcaMFbOjMnMnBKka6}
pwn.college{e8rq3jdih23GRqTE-sx0GjwzGFsDkwGNjm330iPcgOXhMwe}
pwn.college{qefGl8hCZB.MT8mO7Dt0ja6HBzzfmQLDYQ7X5wpIeigQ0fC}
pwn.college{lyo88H28u8yVnZUl2jH2ndHkh4SuOjbYXMaJ2xNK7gWrHSA}
pwn.college{i6olj.5zRZyf.DVqO3h4fALad6MB6-C32NK32uThDEd8iYM}
pwn.college{qpa3B8kYbor8Nvcy.GLnScGlWP5YuYCMLbT0OCt6-liHfYf}
pwn.college{44szrc4i20fJviEzGSprOvreCvZCt-zOANSnKuAu.9nXBzd}
pwn.college{0hH5g9EGE6TiHkeb-4ME5E3sDS6vB8yY3d7sDMIuCdLodpD}
pwn.college{Jb5.IyV4gRb4mVOZiB0qx0Dwxx3U3JXtlcqqdWNmfNxgkkI}
pwn.college{fcqEErlpG-YuYagVUkwlmACXC.OljDeJIRiImKwOr3tF4-a}
pwn.college{lR4.gAFXTg-wQx9WLcC58u6gm7EWb2vYJwdPDXRdtBRMTqz}
pwn.college{fk8xVeCCjDf9RAeSoZ1Gfyo6u5jHDH6e-L.FsosTumOB0wx}
pwn.college{gt-aD876fwT96r5tkzw7oxm9xGCfjbThjPo53y21bwQiPGJ}
pwn.college{YJWzPJbf0U-R6Nq5BRxDeSiiUxFOFkjGPxKjhrviN27XH-y}
pwn.college{d9PVIdRSovjQaPnELphFzMJuhhRSFp13RRJrBNTuGpeti9p}
pwn.college{WgDCcHFFlQV6ebE41aVDbweHe7TAnjOSeSRiAXRjg4dMLPY}
pwn.college{v2tTKZPR-145uUDFxI4ksVMSJv8y1KkQV3J9DrWNVUxxh07}
pwn.college{.E9JVCnVafInZeGw8oqQeHr.TUUJrztp95N7tlopPRJ2mju}
pwn.college{.JJq4maNDo.zkCwprcSs.xbJpdyiCp4urWNQbRKV1xYgJvw}
pwn.college{Jf03.yA8nNiMnahvDZpofU3828oghC4IDW.sdJ809zbVtwO}
pwn.college{MAbahvRNzoKGoU3lcfRxxE3k7Y7Q-mcyOlLn1QzPKFsbNZD}
pwn.college{5EIj716rmAokgn8RkmqeFboGMfIJeGKOjEUoRXTkyBVjB5w}
pwn.college{dx0vIvjtaU0lUylP0Tz0i9t7HXQN3pZl3YYoRrHN1VlX2Jp}
pwn.college{VWxeiqKYeEBKcfEeE-VhJstNqQ6jjsGvzPbga9nPbCIhmoP}
pwn.college{SZJsTyzTm0KAzMRE1LYcjZ5qG0fgY1gRwIhnyYDA-JFpcRu}
pwn.college{r2xjmB1wymOQgEJok3KYGHZOgZUlkftt5aKu8kVuwle5RFL}
pwn.college{A4oYqvVr9Nx9jNbJysQmH3AG9hHQ92D5qLKJrjt6qSuy4Oq}
pwn.college{3Jp9NY60g0erwDFrNnV4ApJP0B3.a4kaW2VMNVpwMQjVroo}
pwn.college{pU3VQkcarGsqatFpX49Rn358akTK5GZDRnG7zF5jh4V.UMv}
pwn.college{3r0SJUmBcVkIY17syHfBa6Ss8OGnSURZ.4HbjX.qyYvMu62}
pwn.college{sa-wVWKB.2Rt2AxQKxfm-PxwxZWkYiPJQiL668P5PCH1YOl}
pwn.college{4TFNrS1R1OOxVJkdWQkXOVIjwoMJcpRhrkb7YvLLtN5YzZ0}
pwn.college{AqjAubqodFArgjoz3Owv.r2IarTLHBTMAcJ83zMRH6k3Ny9}
pwn.college{9epuYdKk3ikKT3rmHRVgmCP9nM4l5d05EVIOVGwqOa8ZMEP}
pwn.college{qldCVMh2R31c5EIf40UQMp8FHAwUdQ3Nh8ixEcdp8LCdju7}
pwn.college{vXQeo2DY3uqpGdH-vxCXWHELPqukg0Ummn0QlRrQjSqzq3b}
pwn.college{JkYSoPi3mhoRT0uJ1KdCqeLtmHHZXjBXdtbXldEcwqtbQ0p}
pwn.college{mzXJS.IRFFVz2obSSdgGnxE45uEvmxRulytzCoK5rzhsFh-}
pwn.college{RyiBhIYzHN9y250.DOAQ4Muc4FEQF3RBnlTmtj26eRS6xM1}
pwn.college{VgJWOIoney2Cz2NNAfcPj2U29dlpxR0A6Gg5m--G-B5gVJb}
pwn.college{G4UK0DO6DSPVSMHG-ARlVBrHyAamC5IuTsGqbSXN3509Z9L}
pwn.college{3vhVi1u6kN9tf2AO6.V-yz-RZFs68ehBAuEcc-ItgKZU45R}
pwn.college{u8CdOCtjMZfa10wYURUQ3lkbtvHmZQt2k3dpitrKLzFg7WY}
pwn.college{KlZAkLaYwJiQqjh6c5HfbydojZ8Iwh6FaW1QzFSNqx1RZyY}
pwn.college{udn1mJ5PqEDPVQ5ueo3TU9oQCiYMKkejifwxmAJEcPg6e8y}
pwn.college{f1qypKSr1AQcyufnX-KGGH3esD54FH8oB293x0Kp7lFHzsN}
pwn.college{PqwaUEjrbYtM1alpgl5LtJKsT2J-xIPGwNTYDibF73J5Aei}
pwn.college{iQ9uHH0K-KhM0NrnTxNB4TbJ2fBTLd05HXhnGg04tFyzxyN}
pwn.college{WpZzX2Yplr8XgKzfYuMK3ZGB9U5WkwJYNEPUp9KcurUobnc}
pwn.college{2F5oYVdfPiAimyfZPwstXq6M20UVQyGA40Z8jOzm906J.kF}
pwn.college{TKjcERjqFAhY-aqrHrYz.DLXfDYPOEkNIVVi-JChmmKLu4Q}
pwn.college{MzD.--MjCwsZR-NR9GyXaruMjipXdeWufC5UwXgKTs3-sMv}
pwn.college{5YXSamRhgORQaifhXr-a6u7BeIiUNZCGOVgGr9aHyB67yxs}
pwn.college{gsliYL5xFwfB0efROYikITD7kEbDPpspED-wXKGfcwd-D5R}
pwn.college{VEs-V2utpMhOog-rQVqSZ.ICuA-V9L7eVnOEIVbe-vk.vax}
pwn.college{RRf51pia2ebUSVeYyJAxUZNu1s-c-6siKOE6AyEk.gWNPL1}
pwn.college{xHjoiP2oWLnrfQh6XiicCaIe34MhfO335x0D.04Po-fcjA4}
pwn.college{LssUEjPVI2gNcCGC0P3gz7.IVDhlwi1nNiMpG66qvS8umdq}
pwn.college{kD2nsUlD8s8M8MP15t2fw91FMOUE3xT8188KOev7HQaO3Cw}
pwn.college{Ik7tJwxsrFqaGooNKApeWGj1JknyWQy588jLWlihNd-xWPM}
pwn.college{VGHEfB04.j1CMTpdsyr3FcB8gmIwh6bgVxr8zu3DzfcF0uV}
pwn.college{odNq1hNse6nwZGb4G12aFfjDEaw1J7g0L0JWQd-15HL9Zml}
pwn.college{K-yRcX6B9qkVFYh5dwI3G6PdjQ4Y2ilg5dwSprKmYeqLBoa}
pwn.college{8hZzrXF1u0R-Vpc1xj6CsnfMDzba9lsPoyhgGDrAt-AVnES}
pwn.college{-mXjIndk8MxyqzjOVAzycZuIcPSuaEZkdj9lc7FS5I8.lic}
pwn.college{uE61hIFL0kCcnOelFBurYplnE9.7ukk.FpR8kCqw.EsA2uV}
pwn.college{IxWtnHDG2gKty8DDlyFQbj.dOeHfQIcbZo53dqD5UN2tE0x}
pwn.college{h0tas39husfOA1AC1pU3Oj3TSLnwXHB7VLm0r22Qg6asPVJ}
pwn.college{397yWPFMcu6IJeTPb-JdEbrZtojW9A5xABxH1OO3ycHWI41}
pwn.college{2TBWKGnkWOBWk315M8.Iq9bSzEAINU0hmyJI6y1ymZPUopR}
pwn.college{4syTita0z0xa.t7j-wVJsUtexZkc9ZB04Qc2FWudlbxWYHG}
pwn.college{wvxVs27fbodWWCNC6bC0LDZ9iYdT6mpiR2Zj5.TvoVztXQ2}
pwn.college{XRhSLy.V-mnwOyuyXGXf-g30agd7-TcbSYrsob70oT26uId}
pwn.college{iKeRg3to5Nn.kOElS5SP2xobUb7WJC2KI5tqWDqiqYBTY6s}
pwn.college{VbkcumUC7pKZGPG-Lyl.g8UjkikJd9DvIj.fz7LNZpuwHb4}
pwn.college{UugQPdS1wXejAfbwcDzA7i78rryGtalogygyCTxw0C6cWwo}
pwn.college{.4qKKUaOCSqvLd4dSHu8qmDYwMHt6B2I3swmXmTf0MZHf5r}
pwn.college{Zlkhjg0fbBmEGdfmgRL2pXGTiwQi1cjSs0rquVS7efQaQOS}
pwn.college{gRy60wTgll88NMqhi3urZBr9tM-nXlTt8rgoZAPpNFKMeT6}
pwn.college{D1sicw.llidB72fQAC9hTD8KcDHvMzJXpoUUsmlKvfkpwLS}
pwn.college{FmV.tuHA5r1vnvxRWN2Xa1OC4opwCgSdapBKZUKDbhP4HbI}
pwn.college{.35k-jPvZmuJwT8ccjfpPiAUyrcSdJrZMMYOsvXjZVnuhb-}
pwn.college{sdXqN3INTwVNHsIQSBu.gkHl3S.cWSeuB9M1P3Dz7YtJElZ}
pwn.college{WNcny4Dt-Zr0oKzwyb5IayFEq445XLK5tAzPu8kcjasYRCH}
pwn.college{pj6ViYcyLSKRZwKolf3YuyNTcZADMuBLHr6web31cHDNBtk}
pwn.college{YflvszQLbWZ-N.PyJz10sG4ZVUWvhhlm6sQlKA2plNFKMJ9}
pwn.college{EkuIDB2h1iYoRyNETK5MEFXCx7szF2Loyyn1OLR10tTD32i}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run 
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{kgygVaRLxHcM7PELxOhY6EgNAeQ.0FNzMDOxwSM1EzNzEzW}
```

### New Learnings
I learnt from this challenge that even after killing a function it might be still adding text to the file untill the piping is completed.
### References 
-NA-


## Suspending processes

### Solve
**Flag:** `pwn.college{glcMU1ZRm-Q0EyMz4v0sMzzapdp.QX1QDO0wSM1EzNzEzW}`

For this challenge I first implemented the run command then suspended it using the "ctrl z" and then implemented another copy og the same run command to obtain the flag.

```bash
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 08:49 pts/0    00:00:00 bash /challenge/run
root         148     146  0 08:49 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         146     136  0 08:49 pts/0    00:00:00 bash /challenge/run
root         153     136  0 08:49 pts/0    00:00:00 bash /challenge/run
root         155     153  0 08:49 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{glcMU1ZRm-Q0EyMz4v0sMzzapdp.QX1QDO0wSM1EzNzEzW}
```

### New Learnings
I learnt that rather then suspending the command completely we can suspend it in the backgroud and then resume it later using the "ctrl -z" command.
### References 
-NA-


## Challenge Name

### Solve
**Flag:** `pwn.college{c9-RDdydmur2wITesypWs7FBxvR.QX2QDO0wSM1EzNzEzW}`

For this challenge i first implemented the run command and then suspended it and then again run it using fg command and giveing the command path as an argument to the -fg command.

```bash
hacker@processes~resuming-processes:~$ /challenge/run 
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg /challenge/run 
/challenge/run
I'm back! Here's your flag:
pwn.college{c9-RDdydmur2wITesypWs7FBxvR.QX2QDO0wSM1EzNzEzW}
Don't forget to press Enter to quit me!
```

### New Learnings
I learnt how to resume the process using "-fg" command after suspending it using "ctrl z" command.
### References 
-NA-


## Background Processes

### Solve
**Flag:** `pwn.college{I67ClzwLJXsSjFEYTvn224xBnUt.QX3QDO0wSM1EzNzEzW}`

for this question i invoked the command then suspended it and then kept it running in th background using the bg command and then invoked another copy of the same command to obtain the flag.

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         146 S+   bash /challenge/run
root         148 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         146 S    bash /challenge/run
root         156 S    sleep 6h
root         157 S+   bash /challenge/run
root         159 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{I67ClzwLJXsSjFEYTvn224xBnUt.QX3QDO0wSM1EzNzEzW}
```

### New Learnings
I learnt how to run the command in the background hile still running new commands in the shell.
### References 
-NA-

## Challenge Name

### Solve
**Flag:** `pwn.college{UltAW6UCexiSgFwL3HHvdFT8SUs.QX4QDO0wSM1EzNzEzW}`

for this challenge I invoked he run command suspended it, then kept it running in the background, then used the fg command to call the background process in the foreground to obtain the flag.

```bash
hacker@processes~foregrounding-processes:~$ /challenge/run 
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg /challenge/run
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.

hacker@processes~foregrounding-processes:~$ fg /challenge/run
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{UltAW6UCexiSgFwL3HHvdFT8SUs.QX4QDO0wSM1EzNzEzW}
```

### New Learnings
I learnt that we can call any background running process in the foreground with the fg command.
### References 
-NA-


## Strating background processes

### Solve
**Flag:** `pwn.college{wq544mpaDUTP6ih_DKoBMHpAODW.QX5QDO0wSM1EzNzEzW}`

For this challenge I just had to invoke the process in the background using the "&" at the end of the syntax.

```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 146
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{wq544mpaDUTP6ih_DKoBMHpAODW.QX5QDO0wSM1EzNzEzW}
```

### New Learnings
I learnt that we dont need to always invoke a command and then send it to the background we can directly invoke a command in the background by appending the "&" at the end of the command.
### References 
-NA-

## Process exit code.

### Solve
**Flag:** `pwn.college{QaWzDuEq7zSzpBPpyWc5jj-O9FT.QX5YDO1wSM1EzNzEzW}`

For this first i had to run the command mentioned in the instruction then obtain its exit code and then use that code as an argument for the next command to obtain the flag.

```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
95
hacker@processes~process-exit-codes:~$ /challenge/submit-code 95
CORRECT! Here is your flag:
pwn.college{QaWzDuEq7zSzpBPpyWc5jj-O9FT.QX5YDO1wSM1EzNzEzW}
```

### New Learnings
I learnt about what are the exit code of a command and how to read them.
### References 
-NA-