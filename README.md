# EECS151 Tapeout Decal Website

EECS151 Tapeout is a Decal (student-run course) giving a hands-on, end-to-end experience in SoC design and implementation culminating in a tapeout.

Students with a background in the fundamentals of digital design and VLSI CAD tools (EECS151 + ASIC lab) will learn how to use the Chisel hardware description language and Chipyard (an agile hardware design framework) to integrate their EECS151 ASIC core or a custom IP block of their own design into a full-scale System-on-Chip (SoC). While covering the basics of agile SoC design concepts and methodology, the course is primarily a hands-on experience. One (or more, depending on student interest) class SoCs are planned to be taped out in the open-source Skywater 130nm process at the end of the semester. Extra chip area is available for motivated students with unique, large-scale projects.

The course aims to give all students hands-on experience in every step of the SoC design process from system-level design (interfaces, modular decoupling), to toplevel integration and physical design with commercial CAD tools though Berkeley’s Hammer tool. Students will participate in a class project consisting of one or more physically realized and fabricated SoCs in the open-source Skywater 130nm process node. Student contributions to the designs may range from a chipyard-integrated version of their EECS 151 ASIC core to custom accelerators or off-chip peripheral interfaces. It is emphasized that while multiple students may collaborate on a single SoC (or even within a module), every student will receive hands-on experience with the full tapeout process, from system architecture to GDSII signoff.

This course spans 13 weeks. Class meets for two hours once a week. Each class will generally consist of a short mini lecture, overview of project status, and check-ins with each team on milestones and obstacles. Students are expected to spend a bit more time each week outside of class time working on their project. The semester will culminate in chip tapeout through Efabless’ chipIgnite, student presentations, and a class poster.

[//]: <> (meow :3)
[//]: <> (MEOW >:3)

<!--
# CS 161 Template Website

![Your Repository's Version - v1.1](https://img.shields.io/badge/Version-v1.1-blue?style=flat)
[![The Latest Version]](https://github.com/cs161-staff/course-site-template)


A course website template used by various large upper-division CS courses at UC Berkeley, including: [CS 161](https://cs161.org), [CS 168](https://cs168.io), [CS 188](https://inst.eecs.berkeley.edu/~cs188), [CS 61B](https://datastructur.es), and others.

The template is built on Just the Docs (https://just-the-docs.com), so check out their documentation for features such as [ordering pages in the sidebar](https://just-the-docs.com/docs/navigation/main/order/), [Markdown syntax](https://just-the-docs.com/docs/index-test/), etc.

The tags at the top of this document represent information about the template version. **You should not change this unless you are maintaining the template.** The left tag represents the version of the template that you cloned, and the right tag represents the latest version of the template. If your repository version does not match the latest version, you should return to the template again next semester.

<!------------------>
[The Latest Version]: https://img.shields.io/github/v/release/cs161-staff/course-site-template?sort=date&display_name=release&label=Latest

## Creating Repo

### Recommended: From Template
> [!TIP]
> If it is not your first semester using the template, and your `Version` matches the `Latest` in the tags above, you can safely clone from the previous semester (option 2). This will be faster than starting from scratch.

We suggest [creating a new repository from this template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) every semester, since the template is being actively maintained for accessibility.

There are two ways to do this. If you already use the GitHub CLI, there is a one-line command to create and clone the repository from this template. If not, we recommend using the web editor to create the repository. We have provided both methods below:
<details open>
  <summary>GitHub Web</summary>

  * In the top left of this repo, click on `Use this Template`, then press `Create a new repository`.
  * Select your staff organization as the Owner
  * Name the repository `{sp/su/fa}XX-site` (replacing `{sp/su/fa}XX` with your semester and year)
  * Make the repository private and press `Create repository`.
  * Clone locally

  Then, you can copy over any relevant files from your previous semester's repo into the newly-created template.
</details>

<details>
  <summary>GitHub CLI</summary>

  * Navigate to the folder where you would like the repo created.
  * Run the following command:
    ```bash
      gh repo create {class-org}/{sp/su/fa}XX-site --private -p cs161-staff/course-site-template --clone
    ```
    * Make sure to replace `{class-org}` with your course's github organization name
    * Make sure to replace `{sp/su/fa}XX` with your semester and year.

  Then, you can copy over any relevant files from your previous semester's repo into the newly-created template.
</details>


### Not Recommended: From Previous Semester

> [!WARNING]  
> If `Version` is not equal to `Latest` above, this method will require you to update the template by hand, which may require a more involved understanding of Jekyll.

If you instead choose to copy the previous semester's repo, then you'll need to take any updates to this template repo, and *manually copy those updates into your own repo*.
- Clone the previous semester's repo
- Rename the folder (e.g. from `fa24-website` to `sp25-website`)
- Delete the `.git` folder, e.g. `rm -rf .git`
- *Delete all bulky files from the repo*, we don't need those clogging up the Git history. Look out for big PDFs like lecture slides, discussion worksheets, staff photos etc.
- Create a new Github repo
  - On your Github organization page, click *New*
  - *Repository name*: `sp25-website` (or whatever naming convention you use)
  - *Description*: [https://inst.eecs.berkeley.edu/~cs188/sp25](https://inst.eecs.berkeley.edu/~cs188/sp25) (or whatever your URL will be)
  - *Private* (not Public)
  - Leave everything else untouched => *Create repository*
  - Back in your terminal, follow the steps under *create a new repository on the command line* while cd'd into your `sp25-website` repo. Should be init, add, commit, branch, remote add, and push.
- Manually copy all new updates from the `course-site-template` repo into your newly-created repo.


### Configuring New Repo

Recommended: Set dummy-proof PR rules.
- On the Github repo page, to go *Settings*
- *Pull Requests*:
 - *Allow merge commits*: `false`
 - *Allow squash merging*: `true`
 - *Default commit message*: Pull request title (others are also ok)
 - *Allow rebase merging*: `false`
- *Automatically delete head branches*: `true`
- Should auto-save

Once you've created the new website, you should mark the old website as outdated. Assuming the old website also uses this template:
- Go to `_config.yml` in the old website repo
- Set `outdated: true`


## Installation

### Jekyll

Anybody updating the website should have [Jekyll installed](https://jekyllrb.com/docs/installation/) so that you can check that the site builds locally before you push any changes.

After installation, `cd` into the website repo and run `bundle exec jekyll serve` to build the website locally. The local website will automatically re-build every time you edit files.


### Pushing updates

> [!IMPORTANT]
> You should *always build locally* and check before pushing any changes. Don't be that person who pushes broken code to production.

> [!IMPORTANT]
> You should always [use pull requests](https://github.blog/developer-skills/github/beginners-guide-to-github-creating-a-pull-request/#creating-your-pull-request) for non-trivial updates. Don't push potentially-breaking changes directly to main.

To update the website, just push to this repo, and the website will automatically build and update in around a minute.

Always remember to **build locally first** with `bundle exec jekyll serve` to make sure that your edits work before committing and pushing them.

To keep the repo clean, **please tag your commit messages** by adding an assignment tag at the beginning. Examples:
- `[disc02] release`
- `[hw02] add electronic hw`
- `[proj1] fix typo in spec`


### Custom domain deploy

> [!NOTE]
> Before you can proceed with this step, make sure to [verify your domain in GitHub](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#about-custom-domain-configuration). This amounts to adding a `CNAME` record aliasing the subdomain you want to your `.github.io` domain.

To deploy from the GitHub repository to a domain using Github Pages, the first step is to open your repository and navigate to `Settings > Pages`. In the "Source" dropdown, select `Github Actions`. From there, you just have to type the domain that you verified (IE: `sp25.cs161.org`) into the "Custom Domain" box, and press save.

After you have done this, the site will be built and published at the domain you entered the next time that you push to main. If you want the current commit to be built, go to the `Actions` tab, click on `Deploy Jekyll site to Pages` in the sidebar, and press `Run Workflow`.

**Guides for Common DNS Providers**
> [!TIP]
> If you are setting up your course website for the first time, we recommend using [Cloudflare](https://www.cloudflare.com/) as your DNS provider. If you do not have a domain and do not mind being locked into Cloudflare DNS, [Cloudflare sells domains at-cost](https://www.cloudflare.com/products/registrar/) as well.

In order to keep this process as easy as possible, we have documented how to add a `CNAME` record using some common DNS providers. If your DNS provider is not documented, feel free to PR and add it below.

<details>
  <summary>Cloudflare</summary>


  **Navigating To Your DNS Dashboard**
  1. [Log in to your cloudflare account](https://dash.cloudflare.com/login). From your dashboard, click on the domain that you wish to edit.
  2. On the sidebar, click `DNS`.

  **Adding a Record**
  1. Navigate to your DNS Dashboard with the above steps.
  2. Press `Add Record`.
  3. Enter the desired Type, Name, and Content. For everything in this guide, you can ignore `TTL`.
  4. Decide whether to leave [Proxying](https://developers.cloudflare.com/dns/proxy-status/#proxied-records) on, if applicable.
  5. Add a note describing what the record is for if it is not clear.
  6. Press `Save`.

  **First-Time Setup**
  
  First, we will verify your domain with GitHub. This prevents third parties from hosting anything using your site:
  1. In GitHub, navigate to `Organization Settings > Pages`.
  2. Press `Add a Domain` and enter your domain (e.g. `cs161.org`)
  3. Add a DNS Record with Type `TXT`. Copy the `Name` and `Content` from the GitHub page.

  Next, we will set up your domain for GitHub Pages.
  1. Navigate to [this page](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain).
  2. For each IPv4 address in Step 5 on the above page, add a DNS Record with Type `A`. Set the Name field to `@` and the Content field to the IPv4 address.
  3. For each IPv6 address in Step 5 on the above page, add a DNS Record with Type `AAAA`. Set the Name field to `@` and the Content field to the IPv6 address.
  4. Add a DNS Record with Type `CNAME` and Name `www`. Set the Target to your domain (e.g. `cs161.org`).
  5. Our recommended way to use your root domain is to set up a [Site Redirect](https://github.com/cs161-staff/site-redirect-template) to your current semester.
  5. To set up your semester-specific page, continue to the section below.
  

  **Continuing Setup**
  1. Navigate to your DNS Dashboard with the above steps.
  2. Add a DNS Record with Type `CNAME`. Set the Name to the domain you'd like to use and the Target to your `.github.io` domain. This will work with either Proxy setting, so whether you use Proxying is up to preference. If you already have previous semesters, it is likely a good idea to mirror what has been done in the past.
  3. Proceed to GitHub to deploy.
</details>

<details>
  <summary>Google DNS</summary>


  **Navigating To Your DNS Dashboard**
  1. Sign into Google with your Course SPA (or the Google Account that owns your DNS).
  2. Click [here](https://console.cloud.google.com/net-services/dns/zones) to access your DNS Zones page.
  3. In the top left, make sure the correct resource is selected. We recommend naming your resource something obvious, e.g. `cs161-www`.
  4. From your dashboard, click on the domain that you wish to edit.

  **Adding a Record**
  1. Navigate to your DNS Dashboard with the above steps.
  2. Press `Add Standard`.
  3. Enter the desired DNS Name, Resources Record Type, Content. Whenever you select a Resources Record Type, the specific content changes to reflect the expected value of that record.
  4. For everything in this guide, you can ignore `TTL`.
  5. Press `Create`.

  **First-Time Setup**
  
  First, we will verify your domain with GitHub. This prevents third parties from hosting anything using your site:
  1. In GitHub, navigate to `Organization Settings > Pages`.
  2. Press `Add a Domain` and enter your domain (e.g. `cs161.org`)
  3. Add a DNS Record with Resource Record Type `TXT`. Set the `DNS Name` field to the `hostname` from the Github page. Set the `TXT data 1` field to the `value` from the GitHub page.

  Next, we will set up your domain for GitHub Pages.
  1. Navigate to [this page](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain).
  2. Add a DNS Record with Resource Record Type `A`. Leave the DNS Name field empty. Copy each IPv4 address in Step 5 on the above page, and add each one as a separate IPv4 address (using the `Add Item` button).
  3. Add a DNS Record with Resource Record Type `AAAA`. Leave the DNS Name field empty. Copy each IPv6 address in Step 5 on the above page, and add each one as a separate IPv6 address (using the `Add Item` button).
  4. Add a DNS Record with Resource Record Type `CNAME` and DNS Name `www`. Set Canonical Name 1 to your domain (e.g. `cs161.org`).
  5. Our recommended way to use your root domain is to set up a [Site Redirect](https://github.com/cs161-staff/site-redirect-template) to your current semester.
  5. To set up your semester-specific page, continue to the section below.
  

  **Continuing Setup**
  1. Navigate to your DNS Dashboard with the above steps.
  2. Add a DNS Record with Resource Record Type `CNAME`. Set the DNS Name to the domain you'd like to use and Canonical Name 1 to your `.github.io` domain.
  3. Proceed to GitHub to deploy.
</details>


### inst.eecs deploy

For UC Berkeley classes only: Refer to this [GitHub gist](https://gist.github.com/ashmchiu/797f80d9d4c1d674b9868c0a01b633c0) for information on setting up the website to deploy on an inst.eecs URL like https://inst.eecs.berkeley.edu/~cs188/sp25.


### Scheduling assignment release

For assignment releases, we recommend the GitHub workflow, [gr2m/merge-schedule-action](https://github.com/gr2m/merge-schedule-action). The configuration that they provide in the "Usage" section of their documentation is what we recommend. Make sure to update your timezone to reflect the timezone you are teaching the course in.

The workflow activates when a PR is made or edited, and checks if the last line includes the `/schedule` command. If so, it will attempt to merge the PR at the time specified after the command. The command accepts:
 - A date in YYYY-MM-DD format (2025-06-15), which will merge at midnight in the timezone you specify.
 - A timezone-sensitive `ISO 8601` date string (2025-06-15T09:00:00.000Z)
 - Nothing, which will merge the next time the cron job is ran.

For example, to schedule a PR to merge on June 16th at midnight in your specified timezone, the last line of a PR should be `/schedule 2025-06-16`. The workflow will add a comment to your PR confirming that it is scheduled.

## Accessibility

This template, as a whole, is built and tested to comply with WCAG 2.2 AA. Most default colors on the site are WCAG 2.2 AAA compliant, but we have not rigorously tested for AAA compliance. As you develop and add features to the template or to your own course website, you should make an effort to validate that your changes continue to comply with WCAG. The best way to do this is to utilize an automatic accessibility checker. We recommend using Axe Devtools ([Chrome Webstore](https://chromewebstore.google.com/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US&pli=1), [Firefox Add-Ons](https://addons.mozilla.org/en-US/firefox/addon/axe-devtools/)), and the built-in Firefox Accessibility tab.

While having a complete understanding of WCAG is difficult, and utilizing automatic checking can help, here are some common pitfalls to look out for:
* All interactive material should be keyboard accessible, and should have a unique label. This is to say, all link text and button text should be unique. Wherever it is not convenient to have the physical text that appears on the page be unique, the `aria-label` property may be used to specify a different message that is shown to accessibility devices (e.g. `Slides` may appear on the page many times, so long as each instance has a unique aria-label, such as `Slides for Lecture 1`).
* All interactive material should be self-descriptive.
  * It is bad practice for your markdown to look like this:
    ```markdown
    Sign in by filling out the Google Form [here](https://forms.google.com).
    ```
    Instead, you should aim to have descriptive labeling such as this:
    ```markdown
    Use the [Weekly Attendance Form](https://forms.google.com) to sign in.
    ```
* All headings should proceed in logical order (e.g. The heading that follows an `h2` should be an `h3`, or anything above an `h3` if the content is semantically not a sub-heading. The heading that directly follows an `h2` should never be an `h4`, `h5`, or `h6`).
* All colors on the page must meet [minimum contrast guidelines](https://www.w3.org/WAI/standards-guidelines/act/rules/afw4f7/) for AA compliance and [enhanced contrast guidelines](https://www.w3.org/WAI/standards-guidelines/act/rules/09o5cg/) for AAA compliance.
* All images must have an `alt` tag set, which offers a detailed description of the image for someone who is visually impaired.

If you are interested in learning more about WCAG, you can check out the [WCAG 2.2 Standard](https://www.w3.org/TR/WCAG22/).

## Start of Semester Setup

### Configuration

> [!NOTE]
> If you've used this template before, you can check your previous semester's config and syllabus files to see how they were filled out last time.

Go to `_config.yml` and follow instructions in that file to update all relevant fields. (Note: You will need to re-run `bundle exec jekyll serve` every time you update this file.)

Next, go to `_data/syllabus.yml` and follow instructions in that file to update all relevant fields.


### Calendar

The calendar page pulls and displays events from a Google Calendar.

Set up your calendar:
- Go to https://calendar.google.com
- Sign in. For UC Berkeley classes, you should sign in as your class [SPA account](https://calnet.berkeley.edu/calnet-departments/special-purpose-accounts-spa), e.g. cs188@berkeley.edu, so that multiple TAs can edit the calendar.
- Click `+` next to *Other calendars* in the right sidebar --> *Create new calendar*
- *Name*: `[CS188 SP25] Website` or similar
- *Description*: blank is fine
- *Time zone*: `GMT-07:00 Pacific Time - Los Angeles`
- Click *Create calendar*

Now go to `_data/calendar.yml`:
- Follow the steps in that file to fill out the four Google Calendar fields.
- Follow the steps in that file to update `remove_prefix`.
- You probably do not need to touch `categories`.

Populate some Google Calendar events to check that it works (using lecture below as an example):
- Back to https://calendar.google.com
- Uncheck everything except `[CS188 SP25] Website` in the sidebar
- Create the lecture calendar event
- *Title*: `[CS188 SP25] Lecture`
- *Location*: `Dwinelle 155` or whatever the room on https://classes.berkeley.edu is
- Note: You want *Location* filled in, but *Room* can be blank
- Click *More options*
- Replace *Does not repeat* with *Custom*
- Fill in your lecture times, e.g. `every Tu/Th`, ending on `May 5, 2025`
- Save, and see if the event appears on the website (if not, you did something wrong, so go back and fix it)

Once the calendar is set up, you can populate Google Calendar with events throughout the semester, and they'll sync on the website.


### Staff

Updating the staff page happens in the `_staffers` folder. Make one `.md` file per member of course staff, following the template provided.

The documentation (and some extra configuration) lives in `_data/staff.yml`.

**Compressing staff images**: Please don't put enormous 4096x4096 staff images in the website repo and force staff/students to load those every time.

> [!WARNING]
> Skipping this step may lead to substantially longer load times, and a much larger Git repository.

Our recommended way to compress images is with the script below, which relies on [ImageMagick](https://imagemagick.org/), a command-line image manipulation program which supports Windows, MacOS, and Linux. It automatically resizes each image, and saves them as a `.webp`. If you do not wish to use ImageMagick, the same thing can be accomplished manually using [GIMP](https://gimp.org), Photoshop, or any other image editor.

There is a different script for each common shell. If you do not know which shell you are using, you can type `echo $0` into your terminal to find out.

Do this before committing them into the repo (otherwise the large image just ends up in the Git history and defeats the point). Make sure to remove the old files, since the command does not do this for you.

<details open>
  <summary>BASH Script</summary>

  ```shell
  shopt -s nullglob
  for i in *.{png,PNG,gif,GIF,heic,HEIC,jpg,JPG,jpeg,JPEG,jfif,JFIF}; do magick "$i" "${i%.*}.webp"; done
  for i in *.{WEBP}; do mv "$i" "${i%.*}.webp"; done
  mogrify -resize '512x512^>' -gravity center -crop '512x512+0+0' -strip *.webp
  shopt -u nullglob
  ```
</details>

<details>
  <summary>ZSH Script</summary>

  ```shell
  setopt CSH_NULL_GLOB
  for i in *.{png,PNG,gif,GIF,heic,HEIC,jpg,JPG,jpeg,JPEG,jfif,JFIF}; do convert "$i" "${i%.*}.webp"; done
  for i in *.{WEBP}; do mv "$i" "${i%.*}.webp"; done
  mogrify -resize '512x512^>' -gravity center -crop '512x512+0+0' -strip *.webp
  setopt NOMATCH
  ```
</details>

<details>
  <summary>Other</summary>

  If you are using a shell like `fish` which does not support complicated globbing, your best bet is just to break into bash temporarily.
  ```shell
  bash -O nullglob -c "for i in *.{png,PNG,gif,GIF,heic,HEIC,jpg,JPG,jpeg,JPEG,jfif,JFIF}; do convert '$i' '${i%.*}.webp'; done"
  bash -O nullglob -c "for i in *.{WEBP}; do mv '$i' '${i%.*}.webp'; done"
  mogrify -resize '512x512^>' -gravity center -crop '512x512+0+0' -strip *.webp
  ```
</details>


## Updates Throughout Semester

### Syllabus

To edit the syllabus (the big table on the homepage), follow the instructions in the relevant file. No other files should need to be edited.
- `_data/lectures.yml`
- `_data/readings.yml`
- `_data/homeworks.yml`
- `_data/projects.yml`
- `_data/labs.yml`


### Weekly Announcements

To add a new weekly announcement, just add a new Markdown file in `_announcements`. See the sample files in that folder for examples.

The homepage defaults to showing the most recent announcement.


### New Pages

When making a new Markdown page (e.g. a new project spec), you can use [Jekyll front matter](https://jekyllrb.com/docs/front-matter/) to configure the page.

We suggest using `layout: page` for all your pages. We currently don't support other layouts.

Just the Docs has many built-in front matter features you can use:
- [Ordering Pages](https://just-the-docs.com/docs/navigation/main/order/)
- [Excluding Pages](https://just-the-docs.com/docs/navigation/main/exclude/)
- [Page Levels](https://just-the-docs.com/docs/navigation/main/levels/)
- [Toggling a list of child pages at the bottom of the page](https://just-the-docs.com/docs/navigation/children)

Note that we are on Just the Docs v0.10.1, so those "New (v0.10.0)" tags are relevant to this repo.

### Additions on top of JTD

Instead of the JTD Built-in Callouts, we have provided the Alerts implementation from [SensEdu](https://shiegechan.github.io/SensEdu/Contributing/docs/#calloutsalerts) with some additional configuration options. By default, you have access to the following Alerts: `NOTE`, `TIP`, `IMPORTANT`, `WARNING`, `CAUTION`, and an unlabeled alert (`ALERT`).

To use Alerts, append `{: .NAME }` to the line above the message you'd like to place into an Alert. For example, to make a Tip Alert:

```liquid
{: .TIP }
This is a Tip Alert!
```

If you need a multi-line Alert, you can wrap your content in a blockquote:
```liquid
{: .TIP }
> This
> 
> is a multi-line Tip Alert!
```

If you are fine with the default colors (blue, green, purple, yellow, or red) but require a custom message, you can define a custom callout in `_sass/custom/custom.scss` by using a mixin. The mixins available are `color-alert($name, $title)` (where `color` is replaced with a color from the list above).

For example, if you want a blue alert titled "Story", put this in `_sass/custom/custom.scss`:
```scss
@include blue-alert(STORY, "Story");
```

And do this to display an alert titled "Story":
```liquid
{: .STORY }
This is a custom blue alert!
```

Not recommended unless you know what you're doing: We also provide an `alert($name, $foreground-color, $background-color, $title)` if you require a custom color for any reason. To use this mixin, you should edit `wider.scss` and `dark-wider.scss` in order to make sure the colors are accessible in both light and dark mode.

If you want to have an alert with a customizable title, you can leave the `$title` argument as `null`. This is done by default for the pre-defined `ALERT` option. In this case, the following syntax will allow you to set whatever title you want on a per-alert basis:
```liquid
{: ALERT }
> Alert Title
>
> Alert Body
```

We also have some custom front matter variables in this template:

**`hide_right_toc`**:
- By default, we render a table of contents on the right side of the page which is automatically generated based on the headings in the markdown file, and has scrollspy enabled.
- When `hide_right_toc: true`, we skip rendering that right table of contents.
- When `hide_right_toc` is any other value (e.g. blank or not in the front matter), then we render the right table of contents.
- The Right TOC does not look good with too many headings. The third-party scrollspy that we use doesn't work well if your Right TOC is too long. If you have too many headings, consider decreasing `toc_max_heading` to hide some of them from the right TOC (see below).

**`hide_content`**:
- When `hide_content: true` is set on the current page or ANY of the current page's ancestors, we render the message "This page has not been released yet" and we do not render the contents of the page.
- When `hide_content` is a non-true value (anything but `true`) on the current page and ALL of the current page's ancestors, we render the page's content as usual.
- In other words, `hide_content` values are inherited from parent to child. If a parent has `hide_content: true`, all of its children, grandchildren, etc. will also not be rendered, regardless of their `hide_content` values. The only way for a page to render is if the page itself and all ancestors do not have `hide_content: true`.
- See "Page Levels" above for what we mean by a page's ancestors.
- This can be useful if, for example, you have a project spec that exists in your repo, but you don't want students to find the spec on the website yet. Also, if your projects are organized into parent/child pages, then hiding the parent page will also hide all children page.
- Edit `_layouts/page.html` if you want to change what the message says, or if you want to change this behavior.
- Disclaimer: This feature involves some cursed code in `_includes/check_ancestors.html`, and may not always work as intended.

**`unreleased_warning`**:
- Basically the same as `hide_content` above, but instead of replacing the contents with a message, this feature simply adds a warning "This page is in an unreleased state." to the top of the page.
- When `unreleased_warning: true` is set on the current page or ANY of the current page's ancestors, we render the warning.
- When `unreleased_warning` is a non-true value (anything but `true`) on the current page and ALL of the current page's ancestors, we don't render the warning.
- In other words, `unreleased_warning` values are inherited from parent to child. If a parent has `unreleased_warning: true`, all of its children, grandchildren, etc. will get the warning rendered, regardless of their `unreleased_warning` values. The only way to make the warning go away is if the page itself and all ancestors do not have `unreleased_warning: true`.
- Edit `_layouts/page.html` if you want to change what the message says, or if you want to change this behavior.
- Disclaimer: This feature also involves some cursed code in `_includes/check_ancestors.html`, and may not always work as intended.
- Note: `hide_content` and `unreleased_warning` are implemented independently (see `_layouts/page.html`) and it is possible to mix-and-match them. Some pages could have the warning and others could be totally hidden. You could even have a page with both set to true, so that the contents are hidden and both the hidden message and unreleased warning are rendered.

**`toc_min_heading`**:
 - An optional parameter that determines the minimum depth heading to capture in the right TOC for that page
 - Does nothing when `hide_right_toc: true`
 - When unset, defaults to the value of `toc_min_heading` in `_config.yml`

**`toc_max_heading`**:
 - An optional parameter that determines the maximum depth heading to capture in the right TOC for that page
 - Does nothing when `hide_right_toc: true`
 - When unset, defaults to the value of `toc_max_heading` in `_config.yml`

**`toc_collapse_depth`**:
 - An optional parameter that determines the collapse depth of the right TOC for that page
   - All headings below the collapse depth do not appear on the TOC by default, but when they are scroolled into view on the page, they uncollapse in the sidebar.
 - Does nothing when `hide_right_toc: true`
 - When unset, defaults to the value of `toc_collapse_depth` in `_config.yml`
 - Note: `toc_collapse_depth: 1` (showing only h1 headers) doesn't work and leads to the same behavior as `toc_collapse_depth: 2` (showing h1 and h2 headers).

When writing pages, we recommend a single h1 header with the page title, and then h2-h6 headers for your content. Also, headers should be continuous, e.g. below h2, you should use h3, not h4 (then under h3, you can use h4). Using other header structures can lead to undefined TOC behavior.

```markdown
# Title of your page

The h1 title of your page should be identical to the title in the front matter.
Some minor abbreviation (e.g. "proj" vs "Project") might be okay.

## Setup

### Windows

Blah blah blah.

### Mac/Linux

Blah blah blah.

## Your Task

Blah blah blah.

#### Don't do this

The header below h2 should be h3.

### Do this instead

And if you want more headers under the h3, then you can use h4.

#### A sub-sub section

Nesting too deeply may cause long TOCs (which render badly), so we discourage it.

## Submission

Blah blah blah.

# Don't do this

The only h1 header should be the title at the top of your page.
```


### Templating

Jekyll allows you to write Markdown pages that reference variables defined in `_data` files.

For example, in `proj1_assignment.yml` we listed assignment-specific attributes, and used them in `proj1/index.md`. This allows you to re-use project specs across semesters, without worrying that you're forgetting to update a submission link or due date.

Another example of data is in `_data/exams.yml`, which lists exam dates that get used in `exam.md`.

Another example of data is in `_data/faqs.yml`, which lists next-semester dates that get used in `resources/faqs.md`.
   

## Customization

> [!WARNING]  
> Some competency in Jekyll and HTML required for this step. We don't recommend attempting this unless you know what you're doing.

If you want to change the layout of the syllabus (the big table on the homepage), you will need to manually edit some more obscure files.


### Syllabus Files

Files used to build the syllabus (each file has more documentation):
- `_includes/lecture.html` has the code for rendering a single box in the "Lectures" column, using a single entry from `_data/lectures.yml`.
- `_includes/readings.html` has the code for rendering a single box in the "Readings" column, using a single entry from `_data/lectures.yml` (lectures and readings share a data file).
- `_includes/discussion.html` has the code for rendering a single box in the "Discussion" column, using a single entry from `_data/discussions.yml`.
- There is just a single piece of code for rendering assignments, used in `_includes/homework.html`, `_includes/lab.html`, and `_includes/project.html`. For simplicity, we suggest keeping these files all identical. Each assignment box is rendered using a single entry from `_data/homeworks.yml`, `_data/labs.html`, and `_data/projects.html`, respectively. The usage of these data files is identical (since the code for rendering all three is the same).
- `_includes/syllabus.html` actually builds the table by using all of the other `_includes` files to build individual boxes, and then putting those boxes together. It also accepts data from `_data/week_extra.yml` (see that file for more documentation).


### Customizing Syllabus

This section some possible changes you might want to perform, and how to implement them.

**Add a separate readings column?** (by default, readings appear in the Lectures column)
- In `_includes/syllabus.html`, uncomment the Readings header and the code for rendering the column (Ctrl+F the word "uncomment" for the two places you need to edit).
- Edit `_data/syllabus.yml` to configure your new Readings column. The config variables are already there, they just go unused by default (when there's no Readings column).

**Add a new assignments column?** (e.g. for labs or vitamins)
- In `_includes/syllabus.html`, uncomment the Labs header and the code for rendering the column (Ctrl+F the word "uncomment" for the two places you need to edit).
- In `_includes/syllabus.html`, you can rename the header you just uncommented - right now it's Labs but it can be whatever else. The other variables can still be called lab, e.g. "lab_element", and they won't show up on the website, so it's probably easiest to leave them unchanged.

**Add a new column for something else? (easier)** (e.g. a second readings column)
> [!CAUTION]
> If you're using `extra` in every cell, you should make sure that the text in each cell is distinct, for accessibility reasons. (e.g. don't make every link say "Slides")
- If you aren't already using the Labs column, the easiest way to add a new column is to repurpose the Labs column for your purposes.
- First, follow the two steps above (in the "Add a new assignments column") section. This enables the Labs column and renames the column header.
- Now, in `labs.yml` (which also doesn't need to be renamed), you can add data to feed into your new column, even if that data isn't an assignment.
- For example, you can use `extra` to put arbitrary Markdown in each cell, use `nonumber` to disable auto-numbering the cells, and use `rowspan` to control the size of each cell. See example below.

```
labs:
  - nonumber: true
    extra: |
      [How to make pancakes](https://www.example1.com)

      [How to make syrup](https://www.example3.com)
    rowspan: 1
  - nonumber: true
    extra: |
      [How to make waffles](https://www.example2.com)
    rowspan: 2
  - nonumber: true
    extra: |
      [How to brownies](https://www.example4.com)
    rowspan: 1
```


**Add a new column for something else? (harder)** (e.g. adding both a Labs and a Vitamins column)
> [!CAUTION]
> You should be manually validating WCAG AA accessibility of your new code. If you're not sure how to do these steps, try the easier approach above.

> [!WARNING]
> Adding too many columns will make the table hard to read, especially on smaller screens (e.g. mobile).
- In `_includes/syllabus.html`, add a new header near the top of the file.
- In `_includes/syllabus.html`, below the headers, initialize new counters, e.g. `vitamin_index`, `vitamin_rowspan`, `vitamin_number`, `default_vitamin_number`.
- In `_includes/syllabus.html`, the second half of the file has mostly-identical codeblocks for rendering each column (e.g. look for "Render the homework column."). Copy-paste this codeblock for the new column in the appropriate place (e.g. if your column is between Homework and Project, then your new codeblock should be between the homework-rendering and project-rendering codeblocks).
- Don't customize the codeblock in `_includes/syllabus.html`. Instead, make a new includes file, e.g. `_includes/vitamin.html`, and write your custom code for rendering a single box here. Look at other files like `_includes/homework.yml` for inspiration.
- Make a new data file, e.g. `_data/vitamins.yml`, for feeding data into your new includes file. Look at other files like `_data/homeworks.yml` for inspiration.


**Rearrange columns?**
- In `_includes/syllabus.html`, reorder the headers near the top of the file.
- In `_includes/syllabus.html`, the second half of the file has mostly-identical codeblocks for rendering each column (e.g. look for "Render the homework column."). Reorder these codeblocks to match your desired order.


**Change the discussion types?** (e.g. add a third type of discussion)
- By default, we support up to 3 types of discussions. Each type can link to worksheet, solutions, videos, and slides, and there's no inherent difference between the types (they share the same rendering code).
- In `_data/discussions.yml`, update `discussion_filename_bases` with the names of your discussion types.
- It's okay if the variables don't match, e.g. `bridge_name: Mega-Discussion` is fine. The variables don't render onto the website. If the variable names really bother you, carefully change the variable names in both `_data/discussions.yml` and `_includes/discussion.html`.
- See `_data/discussions.yml` for instructions on how to render each type of discussion.
- If you want more than 3 types, or you want to change what gets rendered (e.g. make it say "Recording" instead of "Video"), see the question below this.


**Change the way lectures/discussions are rendered?**
- All the code for rendering a single lecture box and a single discussion box are in `_includes/lecture.html` and `_includes/discussion.html`, so you should only need to modify those two files.


**Change the way assignments are rendered?**
- All the code for rendering a single assignment is in `_includes/homework.html`. For simplicity, the other assignment files (`_includes/project.html` and `_includes/lab.html`) are identical. You should only need to edit these files.
- These files are already made to be fairly extensible (e.g. `parts` for rendering any list of links, and `extra` for any arbitrary Markdown), so you may be able to achieve the desired behavior without changing these HTML files.


**Render multiple lectures/discussions/assignments on a single day?**
- If you only need this once (e.g. there's only one day all semester with two lectures), the easiest solution is probably to use `extra_days` in `syllabus.yml`. The day will render twice in the "Date" column. This is much easier than the `day_rowspan` alternative below.
- If you only need this once, a solution is to use the `extra` field in `lectures.yml`. If the extra lecture has the same formatting (e.g. linking to Slides/Recording) as all the others, this is less recommended (see the note about aria-labels in the Accessibility section of this documentation). But if you want custom Markdown on your extra lecture, this could be a good option. This is also easier than the `day_rowspan` alternative below.
- If you need this repeatedly (e.g. there's two lectures on every day), then change `day_rowspan` in `syllabus.yml`. Note that all the other rowspans must now be calculated relative to your updated `day_rowspan`.
- Example of `day_rowspan` usage: Suppose you have two lectures on each of MWF, and two discussions per week. Then you want `day_rowspan: 2` and `default_lecture_rowspan: 1` so that two lectures get rendered per day. Since a week now spans 6 rows, you want `discussion_default_rowspan: 3` so that two discussions are rendered per week.
- More generally, if you change `day_rowspan` to `n`, then you want to multiply every other `default_rowspan` by `n` to get the original table unchanged. But now you can get multiple rows per day by setting some rowspans to be less than `n`.
- The `day_rowspan` feature can be confusing so we don't recommend using it unless you know what you're doing.

-->
