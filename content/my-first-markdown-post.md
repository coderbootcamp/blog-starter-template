---
title: 'My First Markdown Post in Gridsome'
---

Hey, this is the first post using markdown. The top portion of the file is called **frontmatter**. Here are the step to make the blog for your gridsome site.

## Setup

- Create a separate folder for all your markdown posts. You are free to organise the posts in any way you like.
- Install the file-source by running ```npm install @gridsome/source-filesystem --save-dev```.
- We also need a transformer. Install it by running ```npm install @gridsome/transformer-remark --save-dev```
- Now we need to setup the config to compile our markdown files. We need to add the configuration inside our **gridsome.config.js** file.
- Use the source-filesystem config and add it to plugins array. Now we need to setup the folder structure we like to use. Two important things to remember.
  - The *typeName* will be used to query the data using Graphql. So, keep it easy. We shall name it **Post** so that we can query all posts with **allPosts** and individual post with **post** keyword. We will see that in next steps.
  - Next the path. Give the path to your markdown files. In our case, we just added the files inside the *content* folder.
  - We also need to setup the template on how to render the type. In our case **Post**.
- Now we need to use the transformer for these files, without which gridsome will throw and error while compiling. We can leave the defaults without overriding any configuation settings.

## Render Individual Post with Template

Now we have setup the compilation. We now need to make the posts using gridsome.

- To render individual elements of the type, we need to add a template file inside our tempates folder. SInce it is a single element, we will keep the singular name. We will identify the posts with title. So we will change the default template.
- After this we can render the posts by running ```gridsome develop``` again.

## Show all posts in a Page

All posts are rendered inside a page. So we will create a new component called **Posts.vue** inside pages directory. And we will query all the posts and render inside the template.
