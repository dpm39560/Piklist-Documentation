---
title: Building your first Admin Notice
description: Piklist makes it super easy to create admin notices in WordPress.
hidden: true
weight: 1
---

## Description
Piklist makes it super easy to create admin notices in WordPress, usually with no PHP.

In this example, we will add an ADMIN NOTICE, which is an alert dialog that appears whenever someone visits that website. In this example, we will have the dialog display the notice, "The site will be offline tomorrow night for maintenance." and will have an "OK" button so the user can dismiss the notice.

For our example, we will make this alert as a modification to our theme. Be aware, it is also possible to create an admin notice in a plugin you have built. Simply follow the same steps, but put your code in the commensurate folders in your plugin folder instead of the theme folder. 

First, install the Piklist plugin. Then, in your theme folder (let's use "MyTheme" as our theme example), create the following folder structure:

    /MyTheme
      /piklist
        /parts
          /notices

Of course, to fully utilize Piklist, you'll need to create an entire set of folders for Piklist, as illustrated here:

{{< show-tutorial-start-folders >}}

Next, in your `parts/notices/` folder create a new PHP file to hold your notice code. This file can be named anything you want. For this example, we will call it "Offline4Maint.php".

Add the following comment code to the top of this new file:

```
<?php
/*
Notice Type: info
Dismiss: true
*/
?>
```

This comment block creates an admin notice in the WordPress "info" style. And allows the user to dismiss it. To see a complete list of the available styles (types) and the other options available for these comment blocks, see this page {{<comment-block-styles>}}.

 Underneath the comment block add your message:

 ```
 <p>The site will be offline tomorrow night for maintenance.</p>
 ```

 That's all there is to it! With your Piklist plugin activated, whenever anyone visits the website, this admin notice will appear, alerting them to your message, and allowing them to dismiss the message and continue their visit.

## Full Code Snippet


 ```
 <?php
 /*
 Notice Type: info
 Dismiss: true
 */
 ?>
  <p>This website will be offline tomorrow night for maintenance.</p>
  ```
