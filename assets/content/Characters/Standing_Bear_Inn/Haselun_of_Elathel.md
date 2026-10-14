---
shortcode: haselunofelathel
name: {full: "312-2 Innkeeper - Haselun of Elathel", aliases: []}
type: being
subType: npc
tags: [draft]
data:
  id: HLDNbWNIX1y379Pl
  templatePriority: null
  archetypes: [trader]
  gender: male
  occupation: "Innkeeper"
  born: "681.237"
  height: '6'' 5"'
  weight: "176 lbs"
  frame: light
  appearance: {eye_color: hazel, hair_color: brown, complexion: [], extra_features: []}
  packFolder: standingbearinn
sohl:
  items:
    - {model: sohl-sohl-attribute-str, system: {scoreBase: 8}}
    - {model: sohl-sohl-attribute-end, system: {scoreBase: 13}}
    - {model: sohl-sohl-attribute-dex, system: {scoreBase: 9}}
    - {model: sohl-sohl-attribute-agl, system: {scoreBase: 8}}
    - {model: sohl-sohl-attribute-per, system: {scoreBase: 11}}
    - {model: sohl-sohl-attribute-snt, system: {scoreBase: 11}}
    - {model: sohl-sohl-attribute-cml, system: {scoreBase: 10}}
    - {model: sohl-sohl-attribute-aur, system: {scoreBase: 9}}
    - {model: sohl-sohl-attribute-wil, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-rea, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-cre, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-emp, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-elo, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-mor, system: {scoreBase: 11}}
    - {model: sohl-sohl-attribute-voi, system: {scoreBase: 10}}
    - {model: sohl-sohl-skill-archery, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-awar, system: {masteryLevelBase: 57}}
    - {model: sohl-sohl-skill-chrm, system: {initSkillMult: 3}}
    - {model: sohl-sohl-skill-clmb, system: {masteryLevelBase: 33}}
    - {model: sohl-sohl-skill-cmd, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-cook, system: {masteryLevelBase: 55}}
    - {model: sohl-sohl-skill-dnce, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-dscr, system: {masteryLevelBase: 63}}
    - {model: sohl-sohl-skill-draw, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-folklr, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-guil, system: {initSkillMult: 3}}
    - {model: sohl-sohl-skill-init, system: {masteryLevelBase: 58}}
    - {model: sohl-sohl-skill-shok, system: {initSkillMult: 3}}
    - {model: sohl-sohl-skill-intr, system: {masteryLevelBase: 66}}
    - {model: sohl-sohl-skill-jump, system: {masteryLevelBase: 34}}
    - {model: sohl-sohl-skill-melee, system: {masteryLevelBase: 34}}
    - {model: sohl-sohl-skill-dge, system: {masteryLevelBase: 44}}
    - {model: sohl-sohl-skill-pysn, system: {masteryLevelBase: 32}}
    - {model: sohl-sohl-skill-ridg, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-sing, system: {masteryLevelBase: 33}}
    - {model: sohl-sohl-skill-stlth, system: {masteryLevelBase: 38}}
    - {model: sohl-sohl-skill-srvl, system: {masteryLevelBase: 43}}
    - {model: sohl-sohl-skill-spirit, system: {initSkillMult: 3}}
    - {model: sohl-sohl-skill-swim, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-thtcs, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-thro, system: {masteryLevelBase: 48}}
    - {model: sohl-sohl-skill-bflkbite, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-bflkgrab, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-bflkheadbutt, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-bflkkick, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-limbblock, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-press, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-bflkpunch, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-trip, system: {initSkillMult: 2}}
    - {model: sohl-sohl-mysticalability-sprt}
    - model: sohl-sohl-skill-lang
      name: "Language: Hârnic"
      system: {shortcode: langharnic, masteryLevelBase: 82}
    - model: sohl-sohl-skill-lang
      name: "Language: Emela"
      system: {shortcode: langemela, masteryLevelBase: 72}
    - model: sohl-sohl-skill-script
      name: "Script: Lakise"
      system: {shortcode: scriptlakise, masteryLevelBase: 82}
    - {model: sohl-sohl-skill-brew, system: {masteryLevelBase: 63}}
    - {model: sohl-sohl-skill-hrld, system: {masteryLevelBase: 40}}
    - {model: sohl-sohl-skill-math, system: {masteryLevelBase: 36}}
    - {model: sohl-sohl-skill-wpnc, system: {masteryLevelBase: 25}}
    - {model: sohl-sohl-weapongear-dgr, system: {quantity: 2}}
    - {model: sohl-sohl-containergear-beltpouchl3, name: "Beltpouch, leather"}
    - {model: sohl-sohl-armorgear-rtunic}
    - {model: sohl-sohl-armorgear-rleg}
    - {model: sohl-sohl-armorgear-ltshoe}
    - {model: sohl-sohl-miscgear-pence, system: {quantity: 122}}
  system:
    body:
      structure:
        zones:
          - {name: Head, shortcode: headzone, probWeight: 1}
          - {name: Arms, shortcode: armszone, probWeight: 4}
          - {name: Torso, shortcode: torsozone, probWeight: 4}
          - {name: Legs, shortcode: legszone, probWeight: 6}
        parts:
          - name: Head
            shortcode: headpart
            bodyZoneCode: headzone
            roles: [vital]
            canHoldItem: false
            probWeight: 1
          - name: Right Arm
            shortcode: rarmpart
            bodyZoneCode: armszone
            roles: [manipulator]
            canHoldItem: true
            probWeight: 2
          - name: Left Arm
            shortcode: larmpart
            bodyZoneCode: armszone
            roles: [manipulator]
            canHoldItem: true
            probWeight: 2
          - name: Torso
            shortcode: torsopart
            bodyZoneCode: torsozone
            roles: [core]
            canHoldItem: false
            probWeight: 4
          - name: Right Leg
            shortcode: rlegpart
            bodyZoneCode: legszone
            roles: [locomotor]
            canHoldItem: false
            probWeight: 3
          - name: Left Leg
            shortcode: llegpart
            bodyZoneCode: legszone
            roles: [locomotor]
            canHoldItem: false
            probWeight: 3
        locations:
          - name: Skull
            shortcode: skullloc
            bodyPartCode: headpart
            bleedingSusceptibility: low
            amputability: none
            shockValue: 5
            probWeight: 500
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Eye
            shortcode: leyeloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 5
            probWeight: 15
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Eye
            shortcode: reyeloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 5
            probWeight: 15
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Nose
            shortcode: noseloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 5
            probWeight: 30
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Cheek
            shortcode: lcheekloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 60
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Cheek
            shortcode: rcheekloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 60
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Ear
            shortcode: learloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 15
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Ear
            shortcode: rearloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 15
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Mouth
            shortcode: mouthloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 30
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Jaw
            shortcode: jawloc
            bodyPartCode: headpart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 60
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Neck
            shortcode: neckloc
            bodyPartCode: headpart
            bleedingSusceptibility: high
            amputability: low
            shockValue: 5
            probWeight: 200
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Shoulder
            shortcode: rshldloc
            bodyPartCode: rarmpart
            isFumble: true
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 3
            probWeight: 30
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Upper Arm
            shortcode: rupaloc
            bodyPartCode: rarmpart
            isFumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 1
            probWeight: 30
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Elbow
            shortcode: relbloc
            bodyPartCode: rarmpart
            isFumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Forearm
            shortcode: rfraloc
            bodyPartCode: rarmpart
            isFumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 1
            probWeight: 20
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Hand
            shortcode: rhandloc
            bodyPartCode: rarmpart
            isFumble: true
            bleedingSusceptibility: none
            amputability: high
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Shoulder
            shortcode: lshldloc
            bodyPartCode: larmpart
            isFumble: true
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 3
            probWeight: 30
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Upper Arm
            shortcode: lupaloc
            bodyPartCode: larmpart
            isFumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 1
            probWeight: 30
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Elbow
            shortcode: lelbloc
            bodyPartCode: larmpart
            isFumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Forearm
            shortcode: lfraloc
            bodyPartCode: larmpart
            isFumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 1
            probWeight: 20
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Hand
            shortcode: lhandloc
            bodyPartCode: larmpart
            isFumble: true
            bleedingSusceptibility: none
            amputability: high
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Thorax
            shortcode: thrxloc
            bodyPartCode: torsopart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 40
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Abdomen
            shortcode: abdmnloc
            bodyPartCode: torsopart
            bleedingSusceptibility: high
            amputability: none
            shockValue: 4
            probWeight: 40
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Pelvis
            shortcode: plvisloc
            bodyPartCode: torsopart
            bleedingSusceptibility: medium
            amputability: none
            shockValue: 4
            probWeight: 20
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Thigh
            shortcode: rthghloc
            bodyPartCode: rlegpart
            isStumble: true
            bleedingSusceptibility: medium
            amputability: low
            shockValue: 3
            probWeight: 40
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Knee
            shortcode: rkneeloc
            bodyPartCode: rlegpart
            isStumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Calf
            shortcode: rcalfloc
            bodyPartCode: rlegpart
            isStumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 1
            probWeight: 30
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Right Foot
            shortcode: rfootloc
            bodyPartCode: rlegpart
            isStumble: true
            bleedingSusceptibility: none
            amputability: medium
            shockValue: 2
            probWeight: 20
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Thigh
            shortcode: lthghloc
            bodyPartCode: llegpart
            isStumble: true
            bleedingSusceptibility: medium
            amputability: low
            shockValue: 3
            probWeight: 40
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Knee
            shortcode: lkneeloc
            bodyPartCode: llegpart
            isStumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 2
            probWeight: 10
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Calf
            shortcode: lcalfloc
            bodyPartCode: llegpart
            isStumble: true
            bleedingSusceptibility: low
            amputability: medium
            shockValue: 1
            probWeight: 30
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
          - name: Left Foot
            shortcode: lfootloc
            bodyPartCode: llegpart
            isStumble: true
            bleedingSusceptibility: none
            amputability: medium
            shockValue: 2
            probWeight: 20
            protectionBase: {blunt: 0, edged: 0, piercing: 0, fire: 0}
      weight: {base: null, calc: (9 * str) + 50}
      reachBase: 0
      bodyScaleBase: 1
      personalFatigue: enc + 5
    currentMoveMedium: terrestrial
    movementProfiles:
      - medium: terrestrial
        feetPerRound: 50
        leaguesPerWatch: 5
        encumbrance: floor(wt/4)
        strMod: -5 * floor((str - 10) / 2)
        disabled: false
---

# Appearance {#appearance}

**Species**: Human
**Sex**: Male
**Apparent Age**: Middle Aged
**Culture**: Feudal
**Social Class**: Freeman (guilded)
**Height**: 6 ft 5 in
**Frame**: Light
**Weight**: 176 lb
**Appearance**: Average
**Hair Colour**: Brown
**Eye Colour**: Hazel
**Voice**: Average
**Apparent Occupation**: Innkeeper
**Apparent Wealth**: Well off
**Weapons**: Dagger
**Companions**: Wife and staff

# Dossier {#dossier}

**Title**: FFF 312-2 Innkeeper
**Birthday**: 27 Halane 681
**Appearance**: Age 38, height 6' 5", light frame, weight 176 lb, average appearance, fair complexion, brown hair, hazel eyes
**Size**: 7
**Armor**: Excellent quality cloth tunic and leggings, leather shoes, dagger
**Other Equipment**: Belt pouch
**Valuables**: 122d silver in a coin purse
**Notes**: Haselun affects a very precise, upper class accent and vocabulary.

## Biography

Haselun's grandfather was a knight; the youngest son of a bailiff. The best he
could manage for his third daughter was to marry her off to an innkeeper. She
died when Haselun was just six years old. Since boyhood, Haselun has been
determined to return his family to nobility.

Tall, gangly, and not very well coordinated; Haselun reached the height of 6'5"
by age 13. His father shipped him off to Tashal to work as an apprentice and
then journeyman innkeeper. While in Tashal, he did a stint in the city militia.
He was not much of a soldier, most relegated to being the company cook. As part
of the feudal levy, his company was assigned to assist the Chelmarch Army
patrolling the Salt Route. The Kath ambushed them. Only the timely arrival of a
squadron of knights saved them, earning his eternal gratitude.

Upon becoming a master, he returned to Olokand to work for his father. During
one of the Royal Chelebin Tournaments, he fell in love with Wynda [FFF 399-3],
the middle daughter of a gentleman. He dreamed they could return their families
to nobility. Their relationship has been stormy, his desire to move up the
social ladder and disdain for commoners clashes with her utter pragmatism and
down-to-earth nature. They have two children, son Celed, 16 (named for his
great-grandfather) and daughter Danisa, 15 (named for her great-grandmother).
Both are doing apprenticeships in other towns, as far from their father as their
mother could arrange.

Haselun's father died of a heart attack at age 50. He left the Standing Bear Inn
(in Olokand) to his son. It is a large, well respected, and successful inn and
the place to stay during the tournament. Haselun insists that only nobility say
in the inn during that time (and their entourages, if they must). During the
rest of the year, to pay the bills, Wynda insists they allow well-to-do
commoners, the great unwashed, to stay there, much to his disgust.

## Adventure Hooks

Hidden Romantic. Despite their stormy relationship, Haselun really does love
Wynda. He wants to surprise her with a visit from their children. He hires the
PCs to fetch them from where they are currently working (location up to the GM).
Needless to say, they are not thrilled to travel home for a holiday.

Really, The Best Candidate? Haselun is currently the head of the Olokand Mangai,
a largely ineffective organization. The Sheriff of Olokand has little time for
the organization and no one else wanted the job. However, after several years
under Haselun's "leadership" the oth guildsmen want anyone else. Haselun hires
the PCs to help find enough votes to get him returned for another term. It is a
thankless job but he pays very well.

## Credits

This character is taken from "Friends, Foes, and Followers, Part 16 Standing
Bear Inn" on Lythia.com
(<https://www.lythia.com/game_aides/friends-foes-followers-part-16-the-standing-bear-inn/>),
by Kerry Mould and Rob Barnes, with illustrations by Richard Luscheck (sponsored
by Rob Barnes and Patrick Nilsson), and is "fanon", a derivative work of
copyrighted material by Columbia Games Inc. and N. Robin Crossby.

## Conversion notes

This SoHL actor is a first-pass conversion of the HM3 actor of the same name.

- Attributes copy the HM3 scores (Endurance from Stamina, Reasoning from
  Intelligence, Scent from Smell); Perception is derived from Eyesight, Hearing
  and Smell, and Creativity, Empathy and Eloquence are solved from the HM3 skill
  bases of the skills SoHL shares.
- Melee 34 is the mean of the HM3 weapon skills Club 34, Dagger 32, Shield 38,
  Spear 34.
- HM3 skills carried under the SoHL skill nearest to them: Rhetoric 63 as
  Discourse.
- HM3 skills with no SoHL counterpart, left off the sheet: Condition 56, Oratory
  28, Unarmed 37, Foraging 46.
- Gear carried under its HM3 name on the nearest catalogue item: Beltpouch,
  leather as the catalogue's Belt pouch, leather, sm.
- The body and movement are SoHL's Basic Folk; skills the HM3 actor does not
  state open at Basic Folk's initial mastery.
