---
layout: post
title: update grub entries after uninstalling linux
date: 2023-05-18 17:14:28+0545
description: a description about how i removed menu entry of os after uninstalling operating system.
categories: efibootmgr booloader_entry_deletion
giscus_comments: true
related_posts: false
toc:
  sidebar: left
---

<!--
## Adding a Table of Contents

To add a table of contents to a post as a sidebar, simply add
```yml
toc:
  sidebar: left
```
-->

I used linux **efibootmgr** command line tool to my UEFI boot menu. This post is all about what i have done to remove the menu entry from the grub bootloader.

you can install efibootmgr with following command.

Debian/Ubuntu/linux mint
```
sudo apt install efibootmgr
```
<br>
### See Current Entries

run following to see current entries or settings.

```
efibootmgr
```

This shows the Bootorder of entries,boot number of each entry which is identified by hexadecimal number. (*) means that the boot entry is active.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/efibootmgr.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


You can see more information adding -v to show verbose information.

```
efibootmgr -v
```

<br>
### Deleting Boot Entry

After deletion of linux disturbution on a hard disk (in my case it was rhel linux) i still had boot entry for the linux distro. To remove the boot entry for the distro you need to run the following.

```
sudo efibootmgr -b <bootnum> -B
```

example:
```
sudo efibootmgr -b 0001 -B
```

-b option specify the boot number. -B option delete respective boot number.

<p> You can now see the boot entries by running <b>efibootmanager</b> or by rebooting the system.</p>

<br>
### Referenced From
For more detail visit: 
[Use Linux efibootmgr Command to Manage UEFI Boot Menu](https://www.linuxbabe.com/command-line/how-to-use-linux-efibootmgr-examples)
<br>

<!---

## Customizing Your Table of Contents
{:data-toc-text="Customizing"}

If you want to learn more about how to customize the table of contents of your sidebar, you can check the [bootstrap-toc](https://afeld.github.io/bootstrap-toc/) documentation. Notice that you can even customize the text of the heading that will be displayed on the sidebar.

### Example of Sub-Heading 2

Jean shorts raw denim Vice normcore, art party High Life PBR skateboard stumptown vinyl kitsch. Four loko meh 8-bit, tousled banh mi tilde forage Schlitz dreamcatcher twee 3 wolf moon. Chambray asymmetrical paleo salvia, sartorial umami four loko master cleanse drinking vinegar brunch. <a href="https://www.pinterest.com">Pinterest</a> DIY authentic Schlitz, hoodie Intelligentsia butcher trust fund brunch shabby chic Kickstarter forage flexitarian. Direct trade <a href="https://en.wikipedia.org/wiki/Cold-pressed_juice">cold-pressed</a> meggings stumptown plaid, pop-up taxidermy. Hoodie XOXO fingerstache scenester Echo Park. Plaid ugh Wes Anderson, freegan pug selvage fanny pack leggings pickled food truck DIY irony Banksy.

### Example of another Sub-Heading 2

Jean shorts raw denim Vice normcore, art party High Life PBR skateboard stumptown vinyl kitsch. Four loko meh 8-bit, tousled banh mi tilde forage Schlitz dreamcatcher twee 3 wolf moon. Chambray asymmetrical paleo salvia, sartorial umami four loko master cleanse drinking vinegar brunch. <a href="https://www.pinterest.com">Pinterest</a> DIY authentic Schlitz, hoodie Intelligentsia butcher trust fund brunch shabby chic Kickstarter forage flexitarian. Direct trade <a href="https://en.wikipedia.org/wiki/Cold-pressed_juice">cold-pressed</a> meggings stumptown plaid, pop-up taxidermy. Hoodie XOXO fingerstache scenester Echo Park. Plaid ugh Wes Anderson, freegan pug selvage fanny pack leggings pickled food truck DIY irony Banksy.

-->
