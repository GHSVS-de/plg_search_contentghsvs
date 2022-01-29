# plg_search_contentghsvs

- Joomla com_search plugin. Enables searching in articles. Like Joomla's core plugin plg_search_content but you can disable title prioritisation (\"matching titles always first in serch results\").
- <b style='color:red'>Before usage: Disable Joomla's core plg_search_content!</b>

-----------------------------------------------------

# My personal build procedure (WSL 1, Debian, Win 10)
- Prepare/adapt `./package.json`.
- `cd /mnt/z/git-kram/plg_search_contentghsvs`

## node/npm updates/installation
- `npm install` (if never done before)

### Update dependencies
- `npm run g-npm-update-check` or (faster) `npm outdated`
- `npm run g-npm-update` (if needed) or (faster) `npm update --save-dev`

## Build installable ZIP package
- `node build.js`
- New, installable ZIP is in `./dist` afterwards.
- All packed files for this ZIP can be seen in `./package`. **But only if you disable deletion of this folder at the end of `build.js`**.

### For Joomla update and changelog server
- Create new release with new tag.
- - See and copy and complete release description in `dist/release.txt`.
- Extracts(!) of the update and changelog XML for update and changelog servers are in `./dist` as well. Copy/paste and make necessary additions.
