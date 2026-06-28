# Iconography

Icons in Agent Mesh should communicate function and state without needing text.

Text can still be rendered by the app, but icons should carry the first-glance meaning.

## Icon Rules

- Use simple silhouettes.
- Use consistent stroke weight.
- Keep icons readable at small sizes.
- Combine shape and color for status.
- Avoid logos and brand marks.
- Avoid text inside icons.

## Core Status Icons

```text
healthy       circle/check-style mark, green
busy          rotating ring or dot cluster, cyan
warning       triangle/chevron, yellow
error         diamond/octagon/cross-style mark, red
offline       broken ring/slash, gray
blocked       pause/lock-style mark, amber
complete      check/success pulse, green/cyan
failed        red cross/burst, red
selected      ring/brackets, cyan/blue
```

## System Icons

```text
cpu           chip outline
ram           memory stick
storage       disk stack / drive bay
gpu           card/core block
network       connected nodes
vpn           tunnel/shield
ssh           terminal link / beam
logs          scroll/terminal lines
terminal      command prompt panel
service       gear/cube
container     box/cube stack
backup        archive crate / circular arrow
```

## Service Icons

```text
jellyfin      media screen / play-room shape, no brand logo
arr_stack     cargo crate / manifest board
vaultwarden   vault door / lock, no brand logo
snifferops    radar scope / signal rings
docker_bay    container rack / cube stack, no Docker logo
ai_core       model core / neural reactor
engineering   wrench/tool bench
storage       drive rack / archive shelves
communications network map / relay tower
build_lab     terminal + test flask/gear metaphor
```

## Agent Role Icons

```text
engineer          wrench/tool mark
developer         code brackets or terminal shape
scientist         model core / atom-like data shape
signal_officer    antenna/radar sweep
security_officer  shield/lock
cargo_bot         crate/arrow
maintenance_bot   gear/check
recon_drone       drone/sensor dot
commander         command star/chevrons
```

## Interaction Icons

```text
open          doorway/expand arrow
inspect       magnifier
assign        arrow to target
pause         pause bars
resume        play triangle
stop          square
restart       circular arrow
logs          terminal page
settings      gear
confirm       check
cancel        x
```

## Danger Icons

Danger icons should be visually separated from normal actions.

Use for:

- delete
- wipe
- reset
- expose externally
- change firewall/network
- rotate secrets

Danger icon ideas:

```text
trash can
red octagon
broken chain
flame/critical marker
```

## Do Not Use

Avoid:

- real company logos unless licensing is handled
- tiny detailed illustrations
- text labels baked into icons
- random icon styles from multiple packs
- red for normal actions

## Accessibility

Icons should not rely only on color.

Warning should look like warning by shape even if color is not visible.
