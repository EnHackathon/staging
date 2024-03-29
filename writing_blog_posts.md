---
title: Writing blog posts
---

1. Clone the git repository at `git@github.com:EnHackathon/staging` locally.

   Make sure you've been added as a collaborator with write permission by Lewis or Alex.

2. To add a new post to the blog, create a new .md file in the _posts directory of your local copy of the repository.

   The filename should be "YYYY-MM-DD-NameSurname.md" (this is used to create the URL).

3. Write your blog post:

   1. You must include some YAML metadata at the top of the file.
      - Copy the format used on one of the existing blog posts - the metadata is the lines between the two "---" lines.
      - Specify the author, date, title, and optionally the email address of the author for the post. This data will be used on the published post and for displaying it on the blog home page.
      - Make sure to keep the "layout: post" field.

   2. Format the content of your post using markdown formatting (specifically the 'kramdown' variant).

      You can find a guide for the version of markdown used for the blog at https://kramdown.gettalong.org/quickref.html

      In many IDEs (including VS Code) it is possible to preview markdown side-by-side with the text version you edit.
      In VS Code, this can be done with `Ctrl-K V`.

   3. Suggest to write about the following:
      - What you learnt during the day
      - What you found enjoyable/difficult/tedious/confusing
      - Resources you used/found useful
      - Thoughts for elements of the process that are good/could be better (+ suggestions)
      - What you've achieved, what you'd like to achieve and how achievable you feel it is (compared to yesterday)

4. When you're satisfied with your post, commit and push it to the master branch of the staging repo.

   Visit <https://enhackathon.github.io/staging>, the staging area for the blog.

   Check that your new post appears as you expect it to on the front page, and read your post. Check the formatting (and any emojis...) appear as expected. 

   Make any edits you want to your post, and commit and push them.

5. During EnHackathon, new posts from the staging area of the blog will be released to the main blog regularly.
