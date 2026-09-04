* goal
  * 💡Anthropic's implementation of skills -- for -- Claude💡
    * ⚠️[Agent Skills standard](http://agentskills.io)⚠️
    * _Examples:_
      * creative applications (art, music, design)
        * [algorithmic-art](./skills/algorithmic-art)
        * [canvas-design](./skills/canvas-design)
        * [theme-factory](./skills/theme-factory)
        * [slack-gif-creator](./skills/slack-gif-creator)
      * technical tasks (testing web apps, MCP server generation)
        * [webapp-testing](./skills/webapp-testing)
        * [mcp-builder](./skills/mcp-builder)
      * enterprise workflows (communications, branding, etc.)
        * [internal-comms](./skills/internal-comms)
        * [brand-guidelines](./skills/brand-guidelines)
        * [doc-coauthoring](./skills/doc-coauthoring)
      * document skills -- [used by Claude Code](https://www.anthropic.com/news/create-files) --
        * [docx](./skills/docx)
        * [pdf](./skills/pdf)
        * [pptx](./skills/pptx)
        * [xlsx](./skills/xlsx)

# documentation

* [what are skills?](https://support.claude.com/en/articles/12512176-what-are-skills)
* [how to use skills | Claude?](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
* [how to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
* [Agent Skills real use cases](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)

# this repo's structure

```
anthropics-skills/
├── skills/                    # skill examples
└── template/                  # Skill template
```

# ways to test

## -- via -- Claude Code

* ways to install
  * choose
    * `/plugin marketplace add anthropics/skills` > select which one 
      * == register this repository -- as -- a Claude Code Plugin marketplace
  * directly the plugin

    ```
    /plugin install <PACKAGE_SKILL_NAME>@anthropic-agent-skills
    # _Examples:_
    # /plugin install document-skills@anthropic-agent-skills
    # /plugin install example-skills@anthropic-agent-skills
    # ...
    ```

* steps to use
  * `claude`
    * mention the plugin
      * _Example:_ "Use the PDF skill to extract the form fields from `path/to/some-file.pdf`"

## | Claude.ai

* if you have got Claude.ai's premium plans -> ALREADY AVAILABLE
* [how to use](https://support.claude.com/en/articles/12512180-using-skills-in-claude#h_a4222fa77b)

## -- via -- Claude API

* [documentation](https://docs.claude.com/en/api/skills-guide#creating-a-skill)

# how to create a basic skill?

* steps
  * create a "<SOME_FOLDER>/SKILL.md" / 
    * contains
      * YAML frontmatter

        ```markdown
        --
        name: <YOUR_SKILL_UID_WITH_LOWERCASE_AND_SPACEWITHHYPENS>
        description: <SKILL_DESCRIPTION_WHATDOES_WHENTOUSE>
        --
        ```

      * instructions
    * _Example:_ [here](template/SKILL.md)

* [MORE](https://support.claude.com/en/articles/12512198-creating-custom-skills)
