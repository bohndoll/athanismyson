---
author: Athan's Dad
title: Post 5
date: 2021-09-07T01:07:13.000Z
description: Another testing
categories:
  - Tutorial
tags:
  - Testing
image: slide21.png
license: Free
---
Ujicoba seteah perubahan `config.yml` menjadi:

```yaml
media_folder: 'content/post/{{slug}}' # Folder where user uploaded files should go
public_folder: '/img'

collections: 
  - name: 'post'
    label: 'Post'
    folder: 'content/post'
    path: '{{slug}}/{{slug}}'
    media_folder: ''
    public_folder: ''
    create: true
    fields:
```

Semoga benar setelah ini.



Ganbatte.
