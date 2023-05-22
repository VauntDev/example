# Example
This is an example repsoitory that demostrates how Vaunt can be applied to projects. 


# Top Contributors 
<p>
  <img src="https://api.vaunt.dev/v1/github/entities/VauntDev/repositories/example/contributors?format=svg&limit=10" width="350" />
</p>


# Achievements 

This repository leverages Vaunt's standard achievements defined in `./vaunt/config.yaml`. 

Refer to the Vaunt [docs](https://docs.vaunt.dev) for more details on how to leverage Vaunt's achievement configurations. 

```yaml
version: 0.0.1
achievements:
  - achievement:
      name: Shooting Star
      icon: https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/shooting_star.png
      description: Awarded for staring our repository, make a wish!
      triggers:
        - trigger:
            actor: author
            action: star
            condition: starred = true
  - achievement:
      name: Every Bit Counts
      icon: https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/every_bit_counts.png
      description: No commit is to small!
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
```

### Awards 
<p>
  <div> Shooting Star </div>
  <img src="https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/shooting_star.png" width="150" />
</p>
<p>
  <div> Every Bit Counts </div>
  <img src="https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/every_bit_counts.png" width="150" />
</p>
<p>
  <div> Pull Request Hero <div>
  <img src="https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/pull_request_hero.png" width="150" />
</p>
<p>
  <div> Closer </div> 
  <img src="https://raw.githubusercontent.com/vauntdev/example/main/.vaunt/closer.png" width="150" />
</p>
