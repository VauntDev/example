# Example
This is an example repository that demonstrates how Vaunt can be applied to projects.

# Top Contributors
<p>
  <img src="https://api.vaunt.dev/v1/github/entities/VauntDev/repositories/example/contributors?format=svg&limit=12" width="600" />
</p>

# Achievements

This repository leverages Vaunt's standard achievements defined in `./vaunt/config.yaml`.

Refer to the Vaunt [docs](https://docs.vaunt.dev) for more details on how to leverage Vaunt's achievement and notifications configurations.

```yaml
version: 0.0.1
achievements:
  - achievement:
      name: Shooting Star
      icon: https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/shooting_star.png
      description: Awarded for starring our repository, make a wish!
      triggers:
        - trigger:
            actor: author
            action: star
            condition: starred = true
  - achievement:
      name: Every Bit Counts
      icon: https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/every_bit_counts.png
      description: No commit is too small!
      triggers:
        - trigger:
            actor: author
            action: commit
            condition: count() >= 1
  - achievement:
      name: Pull Request Hero
      icon: https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/pull_request_hero.png
      description: You're a PR hero, rock on!
      triggers:
        - trigger:
            actor: author
            action: pull_request
            condition: merged = true
  - achievement:
      name: Closer
      icon: https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/closer.png
      description: Only closers get coffee!
      triggers:
        - trigger:
            actor: author
            action: issue
            condition: closed = true
webhooks:
  - webhook:
      name: achievements
      type: github
      metadata:
        discussion:
          repository: VauntDev/example
          title: Vaunt Achievements
      events:
        - event:
            type: achievement
            value: Shooting Star
        - event:
            type: achievement
            value: Every Bit Counts
        - event:
            type: achievement
            value: Pull Request Hero
        - event:
            type: achievement
            value: Closer
```

### Available Awards

| Name | Icon | Description |
| ---- | ---- | ----------- |
| Shooting Star | <img src="https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/shooting_star.png" width="150" /> | Awarded for starring our repository, make a wish! |
| Every Bit Counts | <img src="https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/every_bit_counts.png" width="150" /> | No commit is too small! |
| Pull Request Hero | <img src="https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/pull_request_hero.png" width="150" /> | You're a PR hero, rock on! |
| Closer| <img src="https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/closer.png" width="150" /> | Only closers get coffee! |

### Embed in your README (or in your website)

Add the following line and replace YOUR_GITHUB_USERNAME with your username:

```html
<p>
  <img src="https://api.vaunt.dev/v1/github/entities/{{YOUR_GITHUB_USERNAME}}/achievements?format=svg&limit=3" width="350" />
</p>
```
