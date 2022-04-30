---
title: README
---

<script src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>

# gitbook-boilerplate-netlify-cms

![Netlify](https://img.shields.io/netlify/99309378-24da-4731-951c-2bf0e4d1dc08)
![GitHub](https://img.shields.io/github/license/DemoMacro/gitbook-boilerplate-netlify-cms)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://www.contributor-covenant.org/version/2/1/code_of_conduct/)

> Gitbook boilerplate integrated with Netlify CMS, powered by Demo Macro.

[![](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/DemoMacro/gitbook-boilerplate-netlify-cms&stack=cms)

## Manual start

### [Fork](https://github.com/DemoMacro/gitbook-boilerplate-netlify-cms/fork) on Github

More info: [GitBook Toolchain Documentation](https://github.com/GitbookIO/gitbook/tree/master/docs)

### Deploy to Netlify

More info: [A Step-by-Step Guide: GitBook on Netlify](https://www.netlify.com/blog/2015/12/08/a-step-by-step-guide-gitbook-on-netlify/)

### Enable Identity and Git Gateway

Netlify's Identity and Git Gateway services allow you to manage CMS admin users for your site without requiring them to have an account with your Git host or commit access on your repo. From your site dashboard on Netlify:

1. Go to **Settings > Identity**, and select **Enable Identity service**.
2. Under **Registration preferences**, select **Open** or **Invite only**. In most cases, you want only invited users to access your CMS, but if you're just experimenting, you can leave it open for convenience.
3. If you'd like to allow one-click login with services like Google and GitHub, check the boxes next to the services you'd like to use, under **External providers**.
4. Scroll down to **Services > Git Gateway**, and click **Enable Git Gateway**. This authenticates with your Git host and generates an API access token. In this case, we're leaving the **Roles** field blank, which means any logged in user may access the CMS.

More info: [Git Gateway](https://docs.netlify.com/visitor-access/git-gateway/)

### Congratulations

You can now manage the content of your website at https://yoursite.netlify.com/admin/.

## License

[MIT](LICENSE) &copy; [Demo Macro](https://github.com/DemoMacro)

<script>
  if (window.netlifyIdentity) {
    window.netlifyIdentity.on("init", user => {
      if (!user) {
        window.netlifyIdentity.on("login", () => {
          document.location.href = "/admin/";
        });
      }
    });
  }
</script>
