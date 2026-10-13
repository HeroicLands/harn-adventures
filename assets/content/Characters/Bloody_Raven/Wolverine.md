---
shortcode: wolverine
name: {full: "Wolverine", aliases: []}
type: being
subType: creature
tags: [draft]
data:
  id: 9EMwIvbllpyY0HuE
  templatePriority: null
  archetypes: []
  packFolder: bloodyraven
  appearance: {complexion: []}
sohl:
  items:
    - {model: sohl-sohl-attribute-str, system: {scoreBase: 14}}
    - {model: sohl-sohl-attribute-end, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-agl, system: {scoreBase: 18}}
    - {model: sohl-sohl-attribute-per, system: {scoreBase: 18}}
    - {model: sohl-sohl-attribute-snt, system: {scoreBase: 18}}
    - {model: sohl-sohl-attribute-aur, system: {scoreBase: 10}}
    - {model: sohl-sohl-attribute-wil, system: {scoreBase: 18}}
    - {model: sohl-sohl-attribute-rea, system: {scoreBase: 5}}
    - {model: sohl-sohl-skill-awar, system: {masteryLevelBase: 80}}
    - {model: sohl-sohl-skill-stlth, system: {masteryLevelBase: 70}}
    - {model: sohl-sohl-skill-init, system: {masteryLevelBase: 80}}
    - {model: sohl-sohl-skill-dge, system: {masteryLevelBase: 80}}
    - {model: sohl-sohl-skill-shok}
    - {model: sohl-sohl-mysticalability-sprt}
    - name: Raking Claws
      type: skill
      system:
        shortcode: claw
        subType: combattechnique
        masteryLevelBase: 50
        combatCategory: melee
        impairedByRoles: [manipulator]
        strikeMode:
          type: melee
          shortcode: claw
          name: Raking Claws
          minParts: 1
          assocSkillCode: null
          attack: {disabled: false, spread: 2, modifier: 0}
          impactBase: {numDice: 1, die: 8, modifier: 3, aspect: edged}
          lengthBase: 1
          defense:
            block: {disabled: true, modifier: 0, successLevelMod: 0}
            counterstrike: {disabled: false, modifier: 0, successLevelMod: 0}
          traits: {noBlock: true}
    - name: Bone-Crushing Bite
      type: skill
      system:
        shortcode: bite
        subType: combattechnique
        masteryLevelBase: 65
        combatCategory: melee
        impairedByRoles: [manipulator]
        strikeMode:
          type: melee
          shortcode: bite
          name: Bone-Crushing Bite
          minParts: 1
          assocSkillCode: null
          attack: {disabled: false, spread: 1, modifier: 0}
          impactBase: {numDice: 1, die: 6, modifier: 4, aspect: piercing}
          lengthBase: 0
          defense:
            block: {disabled: true, modifier: 0, successLevelMod: 0}
            counterstrike: {disabled: false, modifier: 0, successLevelMod: 0}
          traits: {noBlock: true}
    - {model: sohl-sohl-skill-trak, system: {masteryLevelBase: 80}}
    - {model: sohl-sohl-skill-cmd, system: {masteryLevelBase: 50}}
  system:
    body:
      structure:
        zones:
          - {name: Forequarters, shortcode: fqtrzone, probWeight: 2}
          - {name: Torso, shortcode: torsozone, probWeight: 2}
          - {name: Hindquarters, shortcode: hindqtrzone, probWeight: 2}
        parts:
          - name: Head
            shortcode: headpart
            bodyZoneCode: fqtrzone
            roles: [vital, manipulator]
            canHoldItem: false
            probWeight: 10
          - name: Left Foreleg
            shortcode: lforelegpart
            bodyZoneCode: fqtrzone
            roles: &a1 [locomotor, manipulator]
            canHoldItem: false
            probWeight: 5
          - name: Right Foreleg
            shortcode: rforelegpart
            bodyZoneCode: fqtrzone
            roles: *a1
            canHoldItem: false
            probWeight: 5
          - name: Torso
            shortcode: torsopart
            bodyZoneCode: torsozone
            roles: [core]
            canHoldItem: false
            probWeight: 10
          - name: Left Hind Leg
            shortcode: lhindlegpart
            bodyZoneCode: hindqtrzone
            roles: [locomotor]
            canHoldItem: false
            probWeight: 5
          - name: Right Hind Leg
            shortcode: rhindlegpart
            bodyZoneCode: hindqtrzone
            roles: [locomotor]
            canHoldItem: false
            probWeight: 5
          - name: Tail
            shortcode: tailpart
            bodyZoneCode: hindqtrzone
            roles: []
            canHoldItem: false
            probWeight: 10
        locations:
          - name: Head
            shortcode: headloc
            bodyPartCode: headpart
            isFumble: true
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 5
            probWeight: 3
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Neck
            shortcode: neckloc
            bodyPartCode: headpart
            isFumble: true
            bleedingSusceptibility: high
            amputability: low
            shockValue: 5
            probWeight: 2
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Left Foreleg
            shortcode: lforelegloc
            bodyPartCode: lforelegpart
            isFumble: true
            isStumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Right Foreleg
            shortcode: rforelegloc
            bodyPartCode: rforelegpart
            isFumble: true
            isStumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Thorax
            shortcode: thoraxloc
            bodyPartCode: torsopart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 5
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Abdomen
            shortcode: abdloc
            bodyPartCode: torsopart
            bleedingSusceptibility: high
            amputability: none
            shockValue: 4
            probWeight: 3
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Pelvis
            shortcode: plvsloc
            bodyPartCode: torsopart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 2
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Left Hind Leg
            shortcode: lhindlegloc
            bodyPartCode: lhindlegpart
            isStumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Right Hind Leg
            shortcode: rhindlegloc
            bodyPartCode: rhindlegpart
            isStumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
          - name: Tail
            shortcode: tailloc
            bodyPartCode: tailpart
            bleedingSusceptibility: none
            amputability: high
            shockValue: 1
            probWeight: 10
            protectionBase: {blunt: 4, edged: 3, piercing: 2, fire: 4}
      weight: {base: 50, calc: "50"}
      reachBase: 0
      bodyScaleBase: 1.33
      personalFatigue: enc + 5
    currentMoveMedium: terrestrial
    movementProfiles:
      - medium: terrestrial
        feetPerRound: 50
        leaguesPerWatch: 4
        encumbrance: floor(wt/4)
        strMod: -5 * floor((str - 10) / 2)
        disabled: false
---

# Appearance {#appearance}

No appearance is recorded in the source beyond what the dossier says.

# Dossier {#dossier}

## Data

**Habitat**: Woodland and Forest
**Height**: 45" (male), 36" (female)
**Weight**: 18" (male), 14" (female)
**Diet**: Carnivore
**Lifespan**: Generally 8-10 years (maximum 17 years)
**Cost**: 300d (healthy cub)

## Special Abilities

Describe any special abilities.

## Attacks

Worrying: Wolverines have powerful jaws. When they bite, they can hold on and
"worry" the wound. After a successful bite attack, the wolverine rolls its bite
EML again the next turn: CF = lose grip, MF = no re-roll, MS = re-roll damage,
same dice as previous hit, CS = re-roll dice + 1d6 (max 4d6). If re-roll
indicates worse wound, wound is reset to higher level. Otherwise, wound remains
the same.

## Behavior

The wolverine is a fierce creature and not afraid to stand its ground, even
against the largest bears, wolves, or humans. If cornered, they will attack.
Built low to the ground, they are extremely agile and hard to hit. They are
excellent climbers and burrowers. They have a strong, offensive musky odor. They
cannot be domesticated or trained and the cubs (extremely rare) are only raised
for sport in the Pamesani Games.

## Conversion notes

This SoHL actor is a first-pass conversion of the HM3 actor of the same name.

- Attributes copy the HM3 scores (Endurance from Stamina, Reasoning from
  Intelligence, Scent from Smell); Perception is derived from Eyesight, Hearing
  and Smell. Creativity, Empathy and Eloquence have no HM3 basis and are not
  stated.
- HM3 skills carried under the SoHL skill nearest to them: Intimidate 50 as
  Command.
- The body, movement and natural weapons are the SoHL wolverine's, with the HM3
  mastery levels for its attacks; HM3 impact values are not carried.
