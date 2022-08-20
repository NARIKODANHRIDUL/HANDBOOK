
# SHELL PROMPT CUSTOMISATION USING **PS1**
---
### RESOURCES

- [ WIKI - ALL DETAILS ](https://en.wikipedia.org/wiki/ANSI_escape_code)
- [ FANCY CHARACTORS ](https://en.wikipedia.org/wiki/Box-drawing_character)
- [ GETTING ENV VARIABLES ](https://linuxhint.com/bash-ps1-customization/)
- [ OTHER ](https://www.lihaoyi.com/post/BuildyourownCommandLinewithANSIescapecodes.html)

---

### KEYPOINTS

- PS1=" "
- replace new one with old in ~/.bashrc
- \[\e***** \] - everything which is not printed or everything which is giving style
- this helps the bash to calculate the length of PS1

---

### EXAMPLES
 
```
PS1="╭─────────🮙🮙 NAME\n│\u 🯊 \w\n╰─>> "
```

```
PS1="\[\e[32;1m╭─────────🮙🮙 NAME\n\e[32m│\e[36m\u \e[37m🯊\e[33m\w\n\e[32m╰─>> \e[0m\]"
```

```
PS1="\[\e[32;1m\]╭─────────\[\e[37m\]🮙🮙\[\e[32m\]\[\e[47m\] NAME \[\e[0m\]🭬\n\[\e[32m\]│\[\e[47m\]\[\e[36m\]\u \[\e[0m\]🭬\[\e[0m\]\[\e[37m\] \[\e[33m\]\w\n\[\e[32m\]╰─>> \[\[\e[0m\]"
```

```
PS1="\[\e[32;1m\]╭─────────\[\e[37m\]🮙🮙\[\e[32;47m\] NAME \[\e[0m\]🭬\n\[\e[32m\]│\[\e[90m\]🭨\[\e[36;100;1m\]\u \[\e[0;42;90m\]🭬\[\e[0;30;42;1m\]\w\[\e[0;32m\]🭬\[\e[0;32m\]\n╰─>> \[\e[0m\]"
```

```
PS1="\[\e[32;1m\]╭─────\[\e[38;2;200;200;160m\]🮙🮙\[\e[38;2;50;50;50;48;2;200;200;160m\] NAME \[\e[0;38;2;200;200;160m\]🭬\n\[\e[32m\]│\[\e[38;2;0;30;30m\]🭨\[\e[32;48;2;0;30;30;1m\] \u \[\e[0;42;38;2;0;30;30m\]🭬\[\e[0;42;38;2;0;40;40;1m\]\w \[\e[0;32m\]🭬\[\e[0;32m\]\n╰─>> \[\e[0m\]"
```









---
---
---

SHELL PROMPT (LESS IMPORTANT)
---

- STARTSHIP - https://starship.rs/guide/#%F0%9F%9A%80-installation
>> curl -sS https://starship.rs/install.sh | sh
- Copy paste as last line of bashrc
>> nano ~/.bashrc
>>- eval "$(starship init bash)"
- Create a toml file and copy paste configuration from GOOOOOOOOGLE
>> nano ~/.config/starship.toml

