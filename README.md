# EBI-Framework

This, the EBI Visual Framework, is the successor to the current EBI Compliance Theme and is targeted for an autumn 2016 release.

Homed here are the various assets that make the EBI Visual Framewok (CSS, JS, and a few images and build scripts).

## Do I need to download this?

No. The vast majority of users should link to the EBI hosted files. You'll load three CSS files, seven JS files, and use a wrapper HTML. Have a look at the source of [the simple boilerplate page] (https://ebiwd.github.io/EBI-Pattern-library/sample-site/boilerplate/blank.html).

### Tell me more on using this...

- Quick start: see the [HTML demos in the EBI Pattern Library /sample-site directory] (https://github.com/ebiwd/EBI-Pattern-library/tree/gh-pages/sample-site/boilerplate).
- Guidance and help: check out the [issue queue](https://github.com/ebiwd/EBI-Framework/issues) or contact [Ken Hawkins] (https://www.ebi.ac.uk/about/people/ken-hawkins) on the Web Development team.
- Test for compatibility: if you're migrating an exsisting site [try out the in-browser migration JS] (https://github.com/ebiwd/EBI-Framework/blob/gh-pages/sample-site/migrations/testMigration.js)
- Import legacy style and grids: if you're not able to immediately move away from the exsisting omega grid, or some of the old popular or intro boxes [try loading the legacy CSS] (https://www.ebi.ac.uk/web_guidelines/EBI-Framework/v1.1/css/compliance-legacy-compatibility.css)
- Bonus: once you're up and running, [check out the pattern library] (https://ebiwd.github.io/EBI-Pattern-library/) for guidance on making your site look proper and good.

## About the framework

The project is an evolution of the 2013 EBI Compliance Theme, updating visual styles to better match EMBL-EBI print colours and text, modern web design best practices -- such as responsive design, and to move to a versioned framework for improved maintenance cycles.

The first release is v1.1 -- the current EBI Compliance Theme is the v1.0. Version 1.2 will follow six months after this is released.

This project continues efforts of the existing guidance by providing:

- Modularisation of framework components that will:
  - Require fewer roll-your-own solutions
  - Be more robust out of the box
  - Standardisation of tooling
- Project themes: colour palettes are now themes with flexible spacing, layout options
  - Sync styles and colour palette with corporate EMBL-EBI styles
- Update visual assets to make use of contemporary web browser features for:
  - More consistency with print visual language
  - Enhanced mobile support
- Pattern library for reusable components to speed development and reduce fragmentation (in progress, more targeted for 1.2 release)
  - Page-specific header colours and images through metatags: meta-background-image, meta-background-color
  - Built in [pattern support through Foundation Framework] (http://foundation.zurb.com/sites/docs/grid.html)
- Page lifecycle tracking: An improved meta-tag based model for maintaining and tracking content freshness, ownership, and intent
- Regular updates: A versioning system for the framework to help track changes, features, and usage
  - Sass support (optional)
  - NPM updating (optional)
- Collaboration: A more collaborative code base (note this is on GitHub) to offer a better path for code collaboration and integration

## Considerations
A short list of concerns that need to be kept in mind during the dev process.

- Handling non text-centric web applications/services: need to ensure that audience is considered/brought into fold
  - Design pattern library/kitchen sink is potential mitigation
- There are generally several flavours of any visual tooling, a stronger pattern library would be helpful
- Table functionality is generally very simple; it seems guidance could help push this forward
- Mobile and widescreen support is generally weak throughout
- Layouts are simple/weak/inconsistent; templates and samples would help
- Must be conscious to supply enough vital documentation/patterns, but without recreating the Foundation documentation
- Do we keep documentation as one long file, or split into multiple...
- Presently sample code blocks are kept to a minimum to keep the document shorter and increase our flexibility -- as our audience is devs, we may not need code samples at all, as code source should suffice?
- Many of the colour palette tags ( .primary-*, .secondary-a-*, .secondary-b-*, .complement-* ) appear to have no usage (wget + grep) and could likely be removed from the base style sheets. We should survey, pilot in alpha.
- Standardised feedback capturing

## Outreach
As users of this tooling are spread across the institute, ongoing out reach is vital.

### Methods of outreach
Not all developers are in the same place, so we plan to make use of multiple channels:

- Github: Many developers already live in the Github ecosystem, engaging them here will also fit well into the pull request/issue queue ecosystem.
- Web Guidelines Committee: Not only does this facilitate exposure, but is an active forum for peer review.
- Slack: A strong space for communication that can happen even in distributed teams.
- Clinics: An offline space for developers to chat in depth, current thinking is to run in parallel with External Relations' monthly content clinics.
   - Pattern library workshops: While separate from the core framework, it is interdependent
- Showing: Launching the corporate site in the new framework will not only increase awareness but also lead by example.

With the exception of clinics, all of these can be ongoing support/outreach efforts. Recommend the clinics continue as long as there is interest.

## Versioning
As not all users of the framework will be able to update to the very latest and we do not wish to hold others back, we are using a semantic versioning style of releases.

| Major release | Minor release | Note |
| ------------- | ------------- | ---- |
| (Branch)      | (Tag)         | |
| 1.1           | .0            | Initial release evolving from Compliance theme |
| "             | .1            | Tagged minor release |
| "             | .2            | Tagged minor release |
| "             | .3            | Tagged minor release |
| 1.2           | .0            | Documented, breaking release |
| "             | .1            | Tagged minor release |
| 1.3           | .0            | Documented, breaking release |

Difference between major, minor releases:
- Major releases (1.1, 1.2, 1.3...) can have breaking changes and any such changes will be detailed and tested.
- Minor releases (0.0.X) will not have changes to code structure or parts and will mainly add features or update visual assets (such as logos or icon fonts).

The support for previous major versions (branches) is still being considered, but the current suggestion is that the last three major version will be supported with updates to assets, fonts, and critical EMBl and EBI branding.

Where's version 1.0, you ask? Version 1.0 is the [current EBI Compliance theme] (https://www.ebi.ac.uk/web_guidelines/html/compliance/).

### Deployment
Files are hosted in this pattern:
```
//www.ebi.ac.uk/web_guidelines/[repo-name]/[branch]/[repo-files]
```
That is:
```
//www.ebi.ac.uk/web_guidelines/EBI-Framework/v1.1/js/script.js
```

### Building from NPM
We expect the vast majority of users to link to the built CSS and JS files (as shown in the sample HTML files), however some teams may want to download the EBI Framework and modify it for performance or deeper appearance issues.

We've configured the system to build with NPM (no need for gulp or bower).

To get started, have a look at `package.json`. Likely the the `npm run scss` command will cover 90% of use cases.

## Roadmap
- v1.2: Guidance and templates for wide-screen content engagements;
        Use the masthead image as a skybox promo/feature
- v1.4: Unit testing
- v1.5: Add animation guidance and tooling ([see this] (https://medium.com/@vlh/what-does-disney-know-about-interface-animation-anyway-86b32d01bc4a))
