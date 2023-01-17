# Github Finder App

App to search Github users and display their info. 

---

#### BUG: Linking to users websites

Some users from Github have already prefixed their websites with `http://` or
`https://` so we need to check in [User.jsx](src/pages/User.jsx) if their
website url starts with `http` before constructing the external link.
Code changes can be see in [User.jsx](src/pages/User.jsx#L48)

#### BUG: Light theme RepoItem background is too dark

The theme is set based on a `prefers-colorscheme` media query, so you may have a light theme
if you have a light browser theme or OS theme.
When the browser's preferred color scheme is light, the gray background is too dark on the RepoItem component, and the content is not visible.

Using `base-200` and `base-300` backgrounds, will make the component's background change according to the browser's preference.

> Code changes can be seen in
> [RepoItem.jsx](src/components/repos/RepoItem.jsx#L17)

---

## Usage

You can use the Github API without a personal token, but if you want to use your token, add it to the .env file

Learn how to create a token [here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

### Install Dependencies

```
npm install
```

### Run

```
npm start
```
