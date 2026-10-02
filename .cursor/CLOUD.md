# Cloud agents

Local sessions already open the parent and edit the child. Do the same here.

The workspace is the parent. Edit, test, commit, and push the child checkout that owns the fact, then bump that child's pin in the parent. This applies to every parent that pins children. Do not ask to open the child as its own window.

The parent pull request is the pin bump. Push the child with git. Open a child pull request from that child checkout when the child uses pull requests.
