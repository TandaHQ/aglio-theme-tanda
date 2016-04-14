# Algio Theme for Tanda API Docs

Theme for [Aglio](https://github.com/danielgtaylor/aglio) in used to generate [Tanda API docs](https://my.tanda.co/api/v2/documentation).

NPM package [here](https://www.npmjs.com/package/aglio-theme-tanda).

## Usage

First install the npm package globally:
```
npm install -g aglio-theme-tanda
```

Then generate your API documentation using your API blueprint.
```
aglio -i your/api/blueprint.apib -t tanda --theme-template triple -o your/api/documentation.html
```

## Differences from Olio

The main core of this theme is from the [Olio theme](https://github.com/danielgtaylor/aglio/tree/olio-theme).

> **Note:** These differences are only supported and tested using the three column template.

Here are the differences:

#### API Overview nav list indentation
Can now use `# STARTLIST` and `# ENDLIST` to define sections to indent in the nav section on the left.

Notes:
- All `# STARTLIST`s need an `# ENDLIST`
- Nesting is untested

#### API Overview content in right hand side
Can use `# LHSCONTENT`, `# RHSCONTENT`, and `# ENDCONTENT` to add content to the right hand side of the API overview section.

Notes:
- `# LHSCONTENT` **must** come first, followed by `# RHSCONTENT`, and finally by `# ENDCONTENT`.
  - If you just want left or right hand side content only, you still must include all three tags.
- Each defined content block will be aligned.
