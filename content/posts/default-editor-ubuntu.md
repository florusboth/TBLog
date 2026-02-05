+++
date = '2026-02-05T14:50:01+01:00'
draft = false
tags = ['editor', 'ubuntu', 'linux']
title = 'Default Editor Ubuntu'
+++
# Default Editor Ubuntu

For some reason Ubuntu comes with the Nano editor as default. Fine for some, just not for me.

I want VI(M)! So we run, as root:
```
update-alternatives --config editor
```

This will show you a list of possible editors on your system:

```
-> # update-alternatives --config editor
There are 4 choices for the alternative editor (providing /usr/bin/editor).
Selection Path Priority Status
------------------------------------------------------------
0 /bin/nano 40 auto mode
1 /bin/ed -100 manual mode
2 /bin/nano 40 manual mode
* 3 /usr/bin/vim.basic 30 manual mode
4 /usr/bin/vim.tiny 15 manual mode
Press >enter< to keep the current choice[*], or type selection number:
```

Choose your favourite!

