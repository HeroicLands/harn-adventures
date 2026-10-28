---
shortcode: akthulnaragghost
name: {full: "Akthul Narag (Ghost)"}
type: being
subType: npc
tags: [draft]
data:
  id: vD8mcwPLMmHFKFwk
  templatePriority: null
  archetypes: [commoner]
  gender: male
  occupation: "Khuzdul Ghost"
  packFolder: bloodyraven
sohl:
  items:
    - {model: sohl-sohl-attribute-str, system: {scoreBase: 0}}
    - {model: sohl-sohl-attribute-end, system: {scoreBase: 0}}
    - {model: sohl-sohl-attribute-dex, system: {scoreBase: 0}}
    - {model: sohl-sohl-attribute-agl, system: {scoreBase: 0}}
    - {model: sohl-sohl-attribute-per, system: {scoreBase: 0}}
    - {model: sohl-sohl-attribute-snt, system: {scoreBase: 0}}
    - {model: sohl-sohl-attribute-cml, system: {scoreBase: 0}}
    - {model: sohl-sohl-attribute-aur, system: {scoreBase: 9}}
    - {model: sohl-sohl-attribute-wil, system: {scoreBase: 13}}
    - {model: sohl-sohl-attribute-rea, system: {scoreBase: 14}}
    - {model: sohl-sohl-attribute-cre, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-emp, system: {scoreBase: 11}}
    - {model: sohl-sohl-attribute-elo, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-mor, system: {scoreBase: 0}}
    - {model: sohl-sohl-attribute-voi, system: {scoreBase: 0}}
    - model: sohl-sohl-skill-spirit
      name: "Telepathy (F3)"
      system: {shortcode: psitelepathyf3, masteryLevelBase: 62}
    - model: sohl-sohl-skill-spirit
      name: "Sensitivity (F1)"
      system: {shortcode: psisensitivityf1, masteryLevelBase: 59}
    - model: sohl-sohl-skill-spirit
      name: "Mental Conflict"
      system: {shortcode: psimentalconflict, masteryLevelBase: 54}
    - model: sohl-sohl-skill-spirit
      name: "Manifestation"
      system: {shortcode: psimanifestation, masteryLevelBase: 39}
---

# Appearance {#appearance}

No appearance is recorded in the source beyond what the dossier says.

# Dossier {#dossier}

During the rush to close up the outpost, one of the Khuzdul slipped and fell
from the escape ladder. He struck his head, dying instantly. His companions
checked on him and when they determined he was dead, they laid his body to rest
in the hall. Unfortunately, in the rush, his soul was not properly commended to
Siem. As a result, the poor fellow’s soul has been condemned to walk the outpost
forever looking for the way out. The ghost of Akthul Narag will most commonly be
encountered on the upper level, especially in and around the site of his death
at the base of the escape ladder. His next most preferred location is in the
main hall where his body was laid to rest. Nothing remains of his body.

Akthul is one of the Innocent Dead and can be laid to rest by convincing him he
is dead.

## Conversion notes

This SoHL actor is a first-pass conversion of the HM3 actor of the same name.

- Attributes copy the HM3 scores (Endurance from Stamina, Reasoning from
  Intelligence, Scent from Smell); Perception is derived from Eyesight, Hearing
  and Smell, and Creativity, Empathy and Eloquence are set at the population
  mean, since no shared skill fixes them.
- Telepathy (F3) (HM3 psionic, ML 62) is carried as a copy of the Spirit skill
  at that mastery; SoHL has no psionic talents.
- Sensitivity (F1) (HM3 psionic, ML 59) is carried as a copy of the Spirit skill
  at that mastery; SoHL has no psionic talents.
- Mental Conflict (HM3 psionic, ML 54) is carried as a copy of the Spirit skill
  at that mastery; SoHL has no psionic talents.
- Manifestation (HM3 psionic, ML 39) is carried as a copy of the Spirit skill at
  that mastery; SoHL has no psionic talents.
- A ghost has no body, so no body structure is authored and the HM3 zero scores
  for the physical attributes stand.
- The HM3 trait Kleptomania has no SoHL counterpart: SoHL has no matching
  trauma or trait item, so the trait is not recorded in the character's data.
