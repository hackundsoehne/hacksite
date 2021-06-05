# Hacksite

[![Netlify Status](https://api.netlify.com/api/v1/badges/27251695-05a8-41e9-8dde-1d8a1ad00193/deploy-status)](https://app.netlify.com/sites/elastic-jackson-156fc6/deploys)

This is the source code of the [HUGO](https://gohugo.io/) based Hack & Söhne organisation website. The website is deployed from this repository via [netlify](https://www.netlify.com/). **Note** that changes are published live from the `main` branch.

## Setup

1. [Install HUGO](https://gohugo.io/getting-started/installing)
2. `git clone --recurse-submodules git@github.com:hackundsoehne/hacksite.git`
3. `cd hacksite`
4. `hugo server`

## Theme

This website uses the [Hackurat](https://github.com/hackundsoehne/hackurat) HUGO theme. It's managed via git submodules. To update the Hackurat theme submodule, run the following command and commit the resulting changes:

```sh
git submodule update --remote --merge
```

## How to add a new event

The Hackurat theme provides an `events` [archetype](https://gohugo.io/content-management/archetypes/). It comes into play when the `hugo new` command is used to create a new content file in the `events` content directory.

Adjust and use the following command to create a new event: `hugo new events/<YYYY-mm-dd-name-of-event>.de.md`. This will create a new file in `content/events`.

Edit the new file by setting `date` in the front matter to the start date of the events. Also adjust all other front matter variables and make sure the `translationKey` ([docs](https://gohugo.io/content-management/multilingual/#bypassing-default-linking)) is unique accross all events.

Now it's time to translate the event, since our website is published in German and English. Copy the previously created `events/<YYYY-mm-dd-name-of-event>.de.md` file and change the `.de.md` extension to `.en.md` to work on the English translation.

Once that's done run `hugo server` and make sure your event is showing up correctly.
