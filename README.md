# Artzoomi Meteor Boilerplate (Meteor 1.2 rc14)

A starting point for beginner MeteorJS developers and simple MeteorJS applications.
Meteor 1.2 rc14 INCLUDED

* [Installation](#installation)
* [File Structure](#file-structure)
* [FAQs and Additional Resources](#faqs)

## <a name="installation"></a> Installation

1. Clone this repo to `<yourapp>`

  `git clone https://github.com/appigram/artzoomi-meteor-boilerplate <yourapp>`

2. Change Directory to `<yourapp>`

  `cd <yourapp>`

3. Remove `.git`

  `rm -rf .git`

4. Create a new github repo (if you want to)

Meteor 1.2 upgrade guide [here](https://quip.com/RXFlAk9Rc2xI)

## <a name="file-structure"></a> File Structure

We have a common file structure we use across all of our Meteor apps. Client-only files are stored in the `client` directory, server-only files are stored in the `server` directory, and shared files are stored in the `both` directoy.

```
.meteor/   *this is where the meteor core application lives. The only file we would touch in here would be the 'packages' file
both/
  ├── collections/    * This folder is for defining collections
  ├── config/   * This folder is to set configurations for packages you added
  └── router/   * This folder helps define your routes (think of them as pages or urls in your application)
client/
  ├── compatibility/    * This folder is for 3rd party plugins like bootstrap.js (and a great place for jQuery plugins)
  └── stylesheets/    * This folder is for organizing your CSS styles
    ├── lib/    * This folder is for bootstrap and font-awesome stylesheets
    └── base.less   * This file defines your global or base CSS styles
  └── templates/    * This folder holds all of your templates
    └── _shared/    * This folder contains shared templates like layout, header, footer, loading, and not found templates
    └── dashboard/
      ├── dashboard.html
      └── dashboard.js
    └── home/
      ├── home.html
      └── home.js
    └── profile/
      ├── profile.html
      └── profile.js
public/   * This folder contains all "public" files. To use, you can just <img src="/images/<filename>"> to get into the images folder
  ├── fonts/
  └── images/
server/
  ├── permissions/    * This folder allows you to write rules for allow/deny rules for collections
  ├── publications/   * This folder holds all publications
  └── templates/    * This folder is for server-only templates like a 404 template
```

## <a name="faqs"></a> FAQs and Additional Resources

##### Where can I learn about Bootstrap?
http://getbootstrap.com

##### How can I create seed data
You can use the [dburles:factory](https://github.com/percolatestudio/meteor-factory) and [anti:fake](https://github.com/anticoders/meteor-fake/) packages to generate fake collection data for testing your UI.

##### How can I use a remote database locally
MONGO_URL="mongodb://<user>:<password>@dogen.mongohq.com:10077/<dbname>" meteor
