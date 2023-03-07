# GitHub Action Community

GitHub Action for the Community - for welcoming first timers!

## GitHub Action Features

These GitHub Actions will:
- reply to all new **Issues** and **Pull Requests**
  
## Quickstart

You can use 1 or all of these GitHub Actions.

To create a GitHub Action
1. In the folder `.github/workflows/`
2. Create a file `welcome.yaml` (or another name you prefer)
3. Add the Action config

### Welcoming message

This GitHub Action will reply to all new **Issues** and **Pull Requests** with a custom message

Example usage (you can change the replies for `issue-message` and `pr-message`)
```yaml
  welcome:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v1
      - uses: Devs-Dungeon/gh-action-community/src/welcome@main
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          issue-message: '<h1>It''s great having you contribute to this project</h1> Feel free to raise an <strong>Issue</strong>! Welcome to the community :nerd_face:'
          pr-message: '<h1>It''s great having you contribute to this project</h1> Feel free to create a <strong>Pull Request</strong>! Welcome to the community :nerd_face:'
```


## 🔗 Connect with Us
[<img align="left" alt="Subham | Mail" width="80px" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" />][mail]
[<img align="left" alt="Subham | LinkedIn" width="100px" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />][linkedin]
[<img align="left" alt="Subham | Discord" width="92px" src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" />][twitter]
[<img align="left" alt="Subham | Discord" width="92px" src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" />][discord]

[mail]: mailto:devs.dungeon.community@gmail.com
[linkedin]: https://www.linkedin.com/company/devs-dungeon/
[twitter]: https://twitter.com/devs_dungeon
[discord]: https://discord.gg/ceMXzhfaka

