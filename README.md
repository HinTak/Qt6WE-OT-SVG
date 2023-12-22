`rpm --rebuild ...` takes 5 hours 23 minutes (NINJAFLAGS=-v -j4):

```
2023-12-16T23:51:23
2023-12-17T05:14:09

2023-12-21T11:22:12
2023-12-21T16:39:38
```

github container inherited environment:

```
HOME=/github/home
GITHUB_ACTIONS=true
CI=true
```

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 60572268  26615752  70% /
```

source rpm is 378MB.

`dnf builddep`: Total download size: 420 M

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 62927984  24260036  73% /
```

After build:

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 63227136  23960884  73% /
```
