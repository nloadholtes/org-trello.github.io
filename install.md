---
layout: post
title:  "Install"
date:   2014-03-16 11:01:52
---

Add this in your emacs configuration file (`~/.emacs` or `~/.emacs.d/init.el`).

``` lisp
(require 'org-trello)
;; to have org-trello activated for each org file, uncomment this
;; (add-hook 'org-mode-hook 'org-trello-mode)
;; otherwise, M-x org-trello-mode
```

### Marmalade (recommended)

Add this to your emacs configuration file.

``` lisp
(require 'package)
(add-to-list 'package-archives '("marmalade" . "http://marmalade-repo.org/packages"))
(package-initialize)
```

Then hit <kbd>M-x eval-buffer</kbd> to evaluate the buffer's contents.

### Melpa - ~snapshot

Add this to your emacs configuration file.

``` lisp
(require 'package)
(add-to-list 'package-archives '("melpa" . "http://melpa.milkbox.net/packages"))
(package-initialize)
```

Then hit <kbd>M-x eval-buffer</kbd> to evaluate the buffer's contents.

*Note*
Melpa and Marmalade repositories provide the same org-trello code.
The divergence comes from the org-trello dependencies which are not the same versions.

### Github

Clone org-trello from GitHub

```sh
git clone http://github.com/org-trello/org-trello.git
```

Add the org-trello directory to your load path and then add

``` lisp
(add-to-list 'load-path "/path/to/org-trello/")
(require 'org-trello)
```