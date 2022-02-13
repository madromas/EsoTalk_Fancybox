# EsoTalk_Fancybox
Light, easy, fancybox for EsoTalk

### Important: You must have "Attachment" plugin installed and enabled.

Upload 
/fancybox/fancybox.css
/fancybox/fancybox.js

To root of the forum.

Edit core/views/default.master.php by placing css in head
```
<link rel="stylesheet" href="fancybox/fancybox.css">
```
And js in body in the same file.
```
<script src="fancybox/fancybox.js"></script>
```

In addons/plugins/Attachments/plugin.php replace function // For images, either show them directly or show a thumbnail.

With:
```
if (in_array($extension, array("jpg", "jpeg", "png", "gif"))) {
				if ($expanded) return "<a data-fancybox='gallery' href='".$url."'><img src='".$url."' alt='".$filename."' title='Click to enlarge'></a>";
				else return "<a data-fancybox='gallery' href='".$url."' class='attachment attachment-image' target='_blank'><img src='".URL("attachment/thumb/".$attachment["attachmentId"])."' alt='".$filename."' title='".$filename."'></a>";
			}
```

Enjoy!





