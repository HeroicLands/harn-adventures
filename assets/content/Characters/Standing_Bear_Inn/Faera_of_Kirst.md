---
shortcode: faeraofkirst
name: {full: "312-3 Innkeeper - Faera of Kirst", aliases: []}
type: being
subType: npc
tags: [draft]
data:
  id: 7EUVT1LmOwn7DEun
  templatePriority: null
  archetypes: [trader]
  gender: female
  occupation: "Innkeeper"
  born: "697.272"
  height: '5'' 4"'
  weight: "137 lbs"
  frame: medium
  appearance:
    eye_color: "grey"
    hair_color: "blonde"
    skin_color: "fair"
    complexion: ["clear"]
    extra_features: []
  packFolder: standingbearinn
sohl:
  items:
    - {model: sohl-sohl-attribute-str, system: {scoreBase: 11}}
    - {model: sohl-sohl-attribute-end, system: {scoreBase: 16}}
    - {model: sohl-sohl-attribute-dex, system: {scoreBase: 15}}
    - {model: sohl-sohl-attribute-agl, system: {scoreBase: 11}}
    - {model: sohl-sohl-attribute-per, system: {scoreBase: 11}}
    - {model: sohl-sohl-attribute-snt, system: {scoreBase: 14}}
    - {model: sohl-sohl-attribute-cml, system: {scoreBase: 15}}
    - {model: sohl-sohl-attribute-aur, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-wil, system: {scoreBase: 13}}
    - {model: sohl-sohl-attribute-rea, system: {scoreBase: 10}}
    - {model: sohl-sohl-attribute-cre, system: {scoreBase: 13}}
    - {model: sohl-sohl-attribute-emp, system: {scoreBase: 14}}
    - {model: sohl-sohl-attribute-elo, system: {scoreBase: 18}}
    - {model: sohl-sohl-attribute-mor, system: {scoreBase: 12}}
    - {model: sohl-sohl-attribute-voi, system: {scoreBase: 16}}
    - {model: sohl-sohl-skill-archery, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-awar, system: {masteryLevelBase: 45}}
    - {model: sohl-sohl-skill-chrm, system: {initSkillMult: 3}}
    - {model: sohl-sohl-skill-clmb, system: {masteryLevelBase: 53}}
    - {model: sohl-sohl-skill-cmd, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-cook, system: {masteryLevelBase: 77}}
    - {model: sohl-sohl-skill-dnce, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-dscr, system: {masteryLevelBase: 73}}
    - {model: sohl-sohl-skill-draw, system: {masteryLevelBase: 61}}
    - {model: sohl-sohl-skill-folklr, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-guil, system: {initSkillMult: 3}}
    - {model: sohl-sohl-skill-init, system: {masteryLevelBase: 49}}
    - {model: sohl-sohl-skill-shok, system: {initSkillMult: 3}}
    - {model: sohl-sohl-skill-intr, system: {masteryLevelBase: 69}}
    - {model: sohl-sohl-skill-jump, system: {masteryLevelBase: 48}}
    - {model: sohl-sohl-skill-melee, system: {initSkillMult: 2}}
    - {model: sohl-sohl-skill-dge, system: {masteryLevelBase: 57}}
    - {model: sohl-sohl-skill-pysn, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-ridg, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-sing, system: {masteryLevelBase: 34}}
    - {model: sohl-sohl-skill-stlth, system: {masteryLevelBase: 40}}
    - {model: sohl-sohl-skill-srvl, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-spirit, system: {initSkillMult: 3}}
    - {model: sohl-sohl-skill-swim, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-thtcs, system: {initSkillMult: 1}}
    - {model: sohl-sohl-skill-thro, system: {masteryLevelBase: 51}}
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
      system: {shortcode: langharnic, masteryLevelBase: 74}
    - model: sohl-sohl-skill-lang
      name: "Language: Jarinese"
      system: {shortcode: langjarinese, masteryLevelBase: 64}
    - model: sohl-sohl-skill-lang
      name: "Language: Orbaalese"
      system: {shortcode: langorbaalese, masteryLevelBase: 64}
    - model: sohl-sohl-skill-script
      name: "Script: Lakise"
      system: {shortcode: scriptlakise, masteryLevelBase: 83}
    - {model: sohl-sohl-skill-brew, system: {masteryLevelBase: 90}}
    - {model: sohl-sohl-skill-math, system: {masteryLevelBase: 33}}
    - {model: sohl-sohl-armorgear-wdress}
    - {model: sohl-sohl-armorgear-ltunic}
    - {model: sohl-sohl-miscgear-beltwaist, name: "Belt, leather"}
    - {model: sohl-sohl-armorgear-ltshoe}
    - {model: sohl-sohl-containergear-beltpouchl3, name: "Beltpouch, leather"}
    - {model: sohl-sohl-miscgear-pence, system: {quantity: 99}}
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
**Sex**: Female
**Apparent Age**: Adult
**Culture**: Feudal
**Social Class**: Freeman (guilded)
**Height**: 5 ft 4 in
**Frame**: Medium
**Weight**: 137 lb
**Appearance**: Attractive
**Hair Colour**: Blonde
**Eye Colour**: Gray
**Voice**: Excellent
**Apparent Occupation**: Innkeeper
**Apparent Wealth**: Moderate
**Companions**: Inn staff

# Dossier {#dossier}

**Title**: FFF 312-3 Innkeeper
**Birthday**: 2 Ilvin 697
**Appearance**: Age 22, height 5' 4", medium frame, weight 137 lb, attractive appearance, fair complexion, blonde hair, gray eyes
**Size**: 6
**Armor**: Good quality wool dress and linen under tunic, leather belt and shoes
**Other Equipment**: Belt pouch
**Valuables**: 99d silver in a coin purse

## Biography

Faera has been around inns her whole life. Her parents and siblings all work at
inns; though none of them have taken the risky step of seeking promotion to
master. Once promoted, the new master must either seek their own franchise (an
expensive proposition, far beyond the means of a simple journeyman), or become a
bonded innkeeper, cellarer or brewer (positions that often require high-level
personal or family connections). Most guild members find the security of being a
journeyman more appealing than such risky endeavors; it gives them steady
employment and legal status as a (junior) guildsman.

Faera's clan on her father's side comes from Bidow. Her grandparents on her
mother's side are Jarinese refugees, originally from Lethwyn (now Geldeheim).
They fled the Ivinian invasion in 667, arriving in Kaldor in 668. Faera's father
works at an inn in Bidow. Her mother keeps their small cottage. Her two brothers
work in inns somewhere in southern Hârn. She is not too sure where.

Employed as a server, chambermaid and general assistant at the Standing Bear Inn
(in Olokand, Kaldor), Faera is level-headed and intelligent. She is by far the
most sensible member of the staff. Loyal to a fault, she often goes along with
the innkeeper's Haselun [FFF 312-2], latest hare-brained schemes. Faera takes
his side over that of his wife, Wynda [FFF 399-3], to avoid being fired.

Besides being a journeyman innkeeper, Faera is surprisingly talented with
languages, speaking fluent Jarinese (which she learned from her grandparents)
and Orbaalese (learned from the many traders from the north). In her spare time,
she is teaching herself to draw and paint. Faera sleeps above the brewery.

## Adventure Hooks

I'm Not That Kind Of Girl. The PCs are staying at the inn. While not above
showing a little skin to encourage tips, Faera is not a prostitute. If a PC gets
too cheeky, she responds with a slap and a mug of ale over his head.

Discrete Likeness. The PCs are following a suspect. They want an image they can
show to others. They find out that Faera is an accomplished artist. She will
sketch them a very good likeness, for a reasonable fee. Haselun will have a fit
if he sees her sketching when she should be working. The PCs will have to keep
him busy.

Excuse Me, Mister. The PCs are being followed by a group of Orbaalese
mercenaries. They are seated several tables away and talking amongst themselves
in Orbaalese. Little do they know, the pretty server can understand everything
they are saying. She passes a note to one of the PCs who look literate informing
them that the mercenaries intend to ambush them once they are well out of town,
making it look like a brigand attack.

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
- HM3 skills carried under the SoHL skill nearest to them: Rhetoric 73 as
  Discourse.
- HM3 skills with no SoHL counterpart, left off the sheet: Condition 69, Oratory
  33, Unarmed 57.
- Gear carried under its HM3 name on the nearest catalogue item: Belt, leather
  as the catalogue's Belt, Waist; Beltpouch, leather as the catalogue's Belt
  pouch, leather, sm.
- The body and movement are SoHL's Basic Folk; skills the HM3 actor does not
  state open at Basic Folk's initial mastery.
