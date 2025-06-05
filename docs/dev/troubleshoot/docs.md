---
title: Docs
parent: Troubleshoot
last_modified_date: 1.6.2025
---

# Troubleshoot Docs

## Just the Docs

### Image is not rendered in the final doc
Images may not be shown although you see them in a preview. It is likely because the paths are slightly different in the generated files and you might need to go one level back to the parent folder.
e.g. [check here](https://github.com/Linguly/docs/blob/main/docs/setup/how-to-setup.md?plain=1#L40)

### Cross reference path is not working in the final doc
Similar to images, any other path need an extra move to the parent directory (`../`).

