# GitHub Action Community <img src="https://i.imgur.com/m6EYre1.png" width="50px">

GitHub Action for the Community - from welcoming first timers to logging your activity for badges!

## GitHub Action Features 💡

These GitHub Actions will:
- reply to all new **Issues** and **Pull Requests**
- log statistics of user activity to Firestore DB (Firebase)
  
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

#### Options

`footer` is an optional parameter, which can be used to append the `issue-message` and `pr-message`

### Store community activity

This GitHub Action will log statistics of user activity to Firestore DB (Firebase)

```yaml
  statistics:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v1
      - uses: Devs-Dungeon/gh-action-community/src/statistics@main
        if: ${{ <expression> }}
        with:
          firebase-key: ${{ secrets.FIREBASE_KEY }}
```

## 🔗 Connect with Us
[<img align="left" alt="Subham | Mail" width="80px" src="https://img.shields.io/badge/-Gmail-000000?logo=gmail&Color=0A66C2&style=flat-square" />][mail]
[<img align="left" alt="Subham | LinkedIn" width="100px" src="https://img.shields.io/badge/-LinkedIn-000000?logo=linkedin&Color=0A66C2&style=flat-square" />][linkedin]
[<img align="left" alt="Subham | Discord" width="92px" src="https://img.shields.io/badge/-Twitter-000000?logo=twitter&Color=0A66C2&style=flat-square" />][twitter]
[<img align="left" alt="Subham | Discord" width="92px" src="https://img.shields.io/badge/-Discord-000000?logo=discord&Color=0A66C2&style=flat-square" />][discord]

[mail]: mailto:devs.dungeon.community@gmail.com
[linkedin]: https://www.linkedin.com/company/devs-dungeon/
[twitter]: https://twitter.com/devs_dungeon
[discord]: https://discord.gg/ceMXzhfaka

