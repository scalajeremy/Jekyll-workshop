# 3. Start a new project

To start a new project, first we need to create it. Go to the folder where you want to create it.

```bash
jekyll new myblog
# Where "myblog" is the name of your project.
```

Now we can go inside the project and build it with a default configuration and make it available on local.

```bash
cd myblog && bundle exec jekyll serve
```

> :warning: Maybe you've seen a little error in the console. Something about a favicon missing. Just add one in the root folder of your project. 
>
>You don't have one? Here you go (it a "J" for Jekyll... but also for Jeremy & Jonathan :laughing: )
>
> ![favicon](favicon.ico)

There we can browse to  [localhost:4000](http://localhost:4000)

You should see your website

![jekyll minima theme](jekyll_minima.png)

## Next step: [4. Plugins](4_plugins.md)
