---
shortcode: baethyr
name: {full: "Baethyr"}
type: being
subType: creature
tags: [draft]
data:
  id: LgSUIAx1RNcDJE9Y
  templatePriority: null
  archetypes: []
  packFolder: threebrothersbarrow
sohl:
  items:
    - {model: sohl-sohl-attribute-str, system: {scoreBase: 10}}
    - {model: sohl-sohl-attribute-end, system: {scoreBase: 14}}
    - {model: sohl-sohl-attribute-agl, system: {scoreBase: 16}}
    - {model: sohl-sohl-attribute-per, system: {scoreBase: 18}}
    - {model: sohl-sohl-attribute-snt, system: {scoreBase: 18}}
    - {model: sohl-sohl-attribute-aur, system: {scoreBase: 15}}
    - {model: sohl-sohl-attribute-wil, system: {scoreBase: 10}}
    - {model: sohl-sohl-attribute-rea, system: {scoreBase: 6}}
    - {model: sohl-sohl-skill-awar}
    - {model: sohl-sohl-skill-stlth}
    - {model: sohl-sohl-skill-init}
    - {model: sohl-sohl-skill-dge}
    - {model: sohl-sohl-skill-shok}
    - {model: sohl-sohl-mysticalability-sprt}
    - model: sohl-sohl-skill-spirit
      name: "Mental Bolt"
      system: {shortcode: psimentalbolt, masteryLevelBase: 90}
  system:
    body:
      structure:
        zones:
          - {name: Head, shortcode: headzone, probWeight: 3}
          - {name: Forebody, shortcode: torsozone, probWeight: 11}
          - {name: Hindbody, shortcode: hindbodyzone, probWeight: 6}
        parts:
          - name: Head
            shortcode: headpart
            bodyZoneCode: headzone
            roles: [vital, manipulator]
            canHoldItem: false
            probWeight: 10
          - name: Forebody
            shortcode: forebodypart
            bodyZoneCode: torsozone
            roles: [core, locomotor]
            canHoldItem: false
            probWeight: 10
          - name: Hindbody
            shortcode: hindbodypart
            bodyZoneCode: hindbodyzone
            roles: [core, locomotor]
            canHoldItem: false
            probWeight: 6
          - name: Tail
            shortcode: tailpart
            bodyZoneCode: hindbodyzone
            roles: [locomotor]
            canHoldItem: false
            probWeight: 4
        locations:
          - name: Head
            shortcode: headloc
            bodyPartCode: headpart
            isFumble: true
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 5
            probWeight: 4
            protectionBase: {blunt: 4, edged: 6, piercing: 5, fire: 4}
          - name: Neck
            shortcode: neckloc
            bodyPartCode: headpart
            isFumble: true
            bleedingSusceptibility: high
            amputability: low
            shockValue: 5
            probWeight: 6
            protectionBase: {blunt: 4, edged: 6, piercing: 5, fire: 4}
          - name: Thorax
            shortcode: thoraxloc
            bodyPartCode: forebodypart
            isStumble: true
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 10
            protectionBase: {blunt: 4, edged: 6, piercing: 5, fire: 4}
          - name: Abdomen
            shortcode: abdloc
            bodyPartCode: hindbodypart
            isStumble: true
            bleedingSusceptibility: high
            amputability: none
            shockValue: 4
            probWeight: 10
            protectionBase: {blunt: 4, edged: 6, piercing: 5, fire: 4}
          - name: Tail
            shortcode: tailloc
            bodyPartCode: tailpart
            isStumble: true
            bleedingSusceptibility: none
            amputability: high
            shockValue: 1
            probWeight: 10
            protectionBase: {blunt: 4, edged: 6, piercing: 5, fire: 4}
      weight: {base: 150, calc: "150"}
      reachBase: 0
      bodyScaleBase: 1.17
      personalFatigue: enc + 5
    currentMoveMedium: terrestrial
    movementProfiles:
      - medium: terrestrial
        feetPerRound: 30
        leaguesPerWatch: 2
        encumbrance: floor(wt/4)
        strMod: -5 * floor((str - 10) / 2)
        disabled: false
---

# Appearance {#appearance}

No appearance is recorded in the source beyond what the dossier says.

# Dossier {#dossier}

## Data

**Habitat**: Aquatic
**Height**: 8-12 feet
**Weight**: 40-60 lb
**Diet**: Carnivore
**Lifespan**: 30-45 years
**Group**: Solitary

## Description

The Baethyr is an aquatic serpentine Ivashu measuring eight to twelve feet in
length and eight to ten inches thick. Its scales are a dark gray coloration with
an irregular pattern of dark red and violet along its underside. A series of
small horn-like protrusions runs along its jaw, while a single horn juts upward
several inches from the top of its skull. The Baethyr’s small dark eyes are
difficult to pick out from its scales.

Because it spends most of its time underground, the Baethyr’s vision is
relatively poor. It possesses excellent hearing, however, and can detect
movement, especially in water. The Baethyr can also detect scents through
receptors in its forked tongue, allowing it to identify and track prey.

Survivors of the Baethyr’s psionic attack describe a sudden, devastating
headache (akin to a migraine), often accompanied by dizziness and nausea.
Victims frequently experience what may seem like flashes of lightning at the
edges of their vision, and many lose consciousness.

The Baethyr is able to navigate the flooded portions of most cave networks with
ease, allowing it access into areas beyond the reach of most foes as well as to
enter and exit the caves through nearby underwater openings. It can exploit this
mobility to its tactical advantage when confronted by threats.

## Special Abilities

_Mental Bolt_ psionic talent. This is a psionic blast directed at a single mind
within line of sight and no more than 45 yards away. A MS causes the victim to
accrue two Fatigue levels (F2); CS inflicts four Fatigue levels (F4), which
manifests as intense headache, dizziness, and nausea (the GM can vary the
description based on how much Fatigue is accrued). After accruing the fatigue,
the victim must immediately make a Shock Roll (see HârnMaster, Skills 22) or
pass out. The symptoms lessen until the Fatigue levels are recovered normally.

## Attacks

The Baethyr has sharp teeth and can bite if necessary. However, it prefers to
employ its psionic talent, Mental Bolt, to subdue prey. It usually feeds on fish
but will sometimes emerge from its underground lair to prey on small animals,
stunning them helpless before devouring them whole. The Baethyr will generally
seek to avoid larger creatures, including humans, but will not hesitate to
defend itself if it is cornered.

## Conversion notes

This SoHL actor is a first-pass conversion of the HM3 actor of the same name.

- Attributes copy the HM3 scores (Endurance from Stamina, Reasoning from
  Intelligence, Scent from Smell); Perception is derived from Eyesight, Hearing
  and Smell. Creativity, Empathy and Eloquence have no HM3 basis and are not
  stated.
- Mental Bolt (HM3 psionic, ML 90) is carried as a copy of the Spirit skill at
  that mastery; SoHL has no psionic talents.
- The body, movement and natural weapons are the SoHL constrictor snake's, with
  the HM3 mastery levels for its attacks; HM3 impact values are not carried.
