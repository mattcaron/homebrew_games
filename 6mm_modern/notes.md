# Game designer's notes

This is mainly for my own benefit so I can keep things straight as I work
through the design process.

## A note on units

All real world measurement is in meters, kph, and so forth, because that's what
most of the military datasheets are given in, and I hate mixing units.

All game movement is in inches, because that's what OPR and, it seems, most of
the wargaming world, uses.

Yes, the mixing of two systems bothers me. Yes, I'm still going to do it.

## Weapon range scale

If we take the general OPR limit of 48" (which is a longstanding limit that I
discussed with Gaetano years ago when he took away my long-range artillery) as a
functional limit for the tabletop (I'll eventually add special offboard
artillery rules to tickle that spot and we'll just hand-wave the points on
that), and we peg that to the commonly used Rheinmetall Rh-120 (120 L/55 aka
M256)'s 4km effective range, then we end up with the following common weapon
range measurements:

| Measurement (in) | Range (m) |
| ---------------  | --------- |
| 48               | 4000      |
| 42               | 3500      |
| 36               | 3000      |
| 30               | 2500      |
| 24               | 2000      |
| 18               | 1500      |
| 12               | 1000      |
| 6                | 500       |
| 3                | 250       |

Note that there isn't a 3" point value in the point calculation document, though
that can be readily determined from the existing progression. This is important
because many disposable light antitank weapons have a maximum effective range of
between 200m and 300m, so we'll need to make use of that range band as well.

## Movement scale

Given the above, and assuming a turn represents approximately 5 minutes (giving
us engagements lasting 20 minutes to half an hour, given a 4-6 turn game, which
seems reasonable), if we take the basic rules for small scales from the full
rulebook, we get a base infantry movement of 3", which translates to 250m. Given
an average adult human pace of walking at 1m/s for a casual stroll, we'd be able
to cross 500m in 5 minutes. Factor in being shot at, a bit of cautious movement
and broken ground, and a 250m move in 5 minutes (or 500m at a run) becomes
perfectly reasonable.

Pivoting to vehicles, which are almost always Fast, with a movement of 9 / 18 in
the original scale, which is halved to 4.5 (rounded to 5) and 9 as a result of
the scale conversion. As a first change, I'm going to change the rush to 10, so
that it is double the base movement, just to keep things easy). This means that,
flat out, a vehicle will be moving 800m in 5 minutes, which equates to 9.6kph
(assuming I can math). Given that a T-55 has an average cross country speed of
25kph (See https://www.globalsecurity.org/military/world/russia/t-54-specs.htm),
and it is a relatively slow vehicle, I'm not worried that this is
unrealistically fast - if anything, we might be disadvantaging faster vehicles.

## Armor and small arms

One of the recurring conversations on the OPR forums is the whole "but infantry
can shoot a lot at a tank and eventually kill it". This is generally resolved as
"yes, it can, but it takes a lot to do and uses up precious turns shooting so
we're not going to add a rule to make it impossible". These rules retain that
position, though I note that it is even less of an issue here because the
infantry small arms in question will have, in general, a 6" range, which is also
the unit's charge range. Tanks do not like being within infantry charge range
because infantry tends to do things like throw hand grenades in hatches and so
forth. It also puts them in range of any antitank weapons carried by the
infantry, especially if they let the infantry get within 3".

## Melee combat

In the time period covered by these rules, swords are not a thing in any
practical sense, and pistols are typically used as backup weapons, by officers,
and by vehicle crew. As such, neither are really represented in game - it's all
assumed to be part of the same "boots, rifle butts, and bayonets" fight.

It is further assumed that all troops have bayonets and grenades and will use
them in close combat in addition to their normal longarms - indeed, that's one
of the benefits of the modern assault rifle - it's actually usable in a close
quarter battle situation. Plus, we're talking an assault over a 500m charge
range and 5 minutes of movement.

As a result, melee combat represents more of a close range firefight and
therefore the "determine attacks" phase of melee combat is the same as that of
ranged combat, as the charging unit fights with all their small arms. The
principal difference is that the defending unit gets to shoot back.

Further, the principal CCW in this ruleset will end up being the submachine gun,
as it is more compact and manueverable in close quarters, but the tradeoff for
this is effective range, which is 100m or less. Thus, in this scale, it is a
CCW.

I'm fully comfortable with this because this is going to be primarily a vehicle
focused game, so...

## Splitting fire

Individual weapons may not split fire, but it is assumed that there is one
dedicated person for each weapon system - one infantryman per rifle, one tank
crew position per weapon, etc. While this may not always be accurate (for
example, in some IFVs, the gunner may change between the main gun and the ATGM,
but in others, they may be independent systems and the vehicle commander might
shoot it.) If this is not the case, we're going to hand wave and ignore it.

Explicitly stated, this does mean that, in a given turn, an M1 Abrams' main gun
can fire at 1 target, the skate mount 7.62mm MG can shoot at some infanty, and
the commander's M2 can shoot at some helicopters. Is this realistic? Not really.
The commander would probably be commanding and the loader would probably be
loading, but we're going to err on the side of more shooting in this case. More
shooting means stuff dies faster, which means we get a faster game, despite
splitting fire. Yay.

## Defense

As a result of the pivot of this version of the rules to being more vehicle
focused, the defense recommendations of the Point Calculator are being slightly
violated. The logic here is that we don't have fancy powered armor in any of the
covered time periods. And, since these rules are less infantry focused, we
really only care about things that protect against rifle rounds (as discussed
above, pistol caliber weapons are close combat weapons). Many soldiers are
unarmored, and modern, well equipped forces will have soft armor with hard
ceramic trauma plate inserts. Unarmored vehicles are things like pickup trucks,
humvees, etc. Armored vehicles are things like uparmored humvees, armored cars
(of the type that protect dignitaries), APCs, lightly armored scout cars and so
forth. IFVs are for more heavily armored vehicles which fall short of tanks -
proper fighting vehicles, more heavily armored scout cars, and even some light
tanks. Finally, tanks are for proper tanks.

Anyway, the guidelines for this ruleset are as follows:

| Description                           | Value |
| -----------                           | ----- |
| Unarmored infantry                    | 6+    |
| Armored infantry / Unarmored vehicles | 5+    |
| Armored vehicles                      | 4+    |
| IFVs                                  | 3+    |
| Tanks                                 | 2+    |

The robustness of the vehicle will be handled by its Tough(X) value as is
typical.

## AP

The AP value only starts at .50 cal / 12.7mm guns. Referencing the table in the
previous section, the logic is that your Unarmored Infantry always relies on
dumb luck if they're being shot at, and the armor plates for armored infantry
are typically rated to protect against 7.62mm rifle rounds. Armored vehicles are
on that transition point where they may be rated up to (but not including) .50
cal, or might actually protect against .50 cal rounds. IFVs protect against over
.50 cal rounds, and so forth. Everything is scaled from there.

| Description                                          | Value |
| -----------                                          | ----- |
| .50 BMG / 12.7mm                                     | 1     |
| 20mm - 30mm AP cannon rounds, older RPG warheads     | 2     |
| Basic ATGM / Kinetic tank round, modern RPG warheads | 3     |
| Advanced / Modern ATGM / Kinetic tank round          | 4     |

I realize that "Basic" and "Advanced" are somewhat relative, but that's
intentional, so it can be a judgement call based on the stats of the weapon
system. But, generally, the 105mm gun from the M1 firing an APFSDS round will
get AP(3) and the 120mm gun on the M1A2 firing an APFSDS will get AP(4).

How much damage it does will be scaled with Deadly(X) as is typical as well.

## Weapons stats

In researching various modern world military systems, patterns and commonalities
emerge. At the scales we're discussing, assault rifles end up basically being
the same, as do light, heavy, and medium machineguns. Main gun systems differ
between NATO and former Warsaw systems but, within those divisions, are broadly
similar. As such, much like the reference table on page 12 of the Points
Calculator, we end up with the following table of common infantry and light
support weapons:

| Weapon                                      | Stats          | Base Cost |
| ------                                      | -----          | --------- |
| Infantry Rifle (M16/M4, AK series, FAL, G3) | 6" , A1        | 0.125     |
| Squad Automatic Weapon (M249, RPD, RPK)     | 6", A3         | 0.375     |
| Medium Machinegun (M240, PKM)               | 12", A3        | 0.75      |
| Heavy Machinegun (M2, DSHK, Kord)           | 24", A3, AP(1) | 2.25      |

There are some variations in ammunition in the above (tracer, armor piercing,
etc.) but such variations have minimal impact at this game scale.

Once you get into larger bore guns (around 20mm and up) then you start to see
serious differences in weapon performance based on differences in ammunition.
For example, the BMP-2M uses a 30mm automatic cannon which has a 4000m range
when firing Frag-HE ammunition, but the best AP ammo (circa 2016) is only rated
for 2000+m (source: WEG 2016, Vol 1, p. 169). Further, these gun systems tend to
be dual feed allowing easy switching between ammunition.

In isolation, this is not tremendously complicated - stat out 2 systems as
options and cost the unit based on the highest one, as per the Point Calculator
rules. However, modern variants of many such vehicles will also frequently mount
ATGM systems. Since ATGMs are expensive relative to various types of Armor
Piercing ammunition, most combat doctrines dictate reserving the ATGMs for
actual tanks, and recommend the use of the main gun for APCs, IFVs and similar
lightly armored vehicles. As wargamers, however, we don't have to answer to
theater commanders wondering where all the missiles have gone, and therefore we
are likely to shoot the most effective weapon against a given target. This leads
to the ATGM flatly replacing the AP ammunition, and hence it should be treated
as an upgrade rather than an addition.

Further, it is not uncommon for vehicles to mount multiple weapons systems in a
combination of turrets, pintle mounts, remote weapons stations, and so forth.
Depending on the era from which the vehicle dates, the disposition of the crew
while under fire, and the specific mounting points of the various guns, not all
weapons can realistically be fired simultaneously. In these situations, the
mutually exclusive weapons will be treated as a combined entry. The most common
case is that of a main battle tank which has a coaxially mounted machine gun,
where that gun is fired instead of the main gun. This approach would result in
the following entry for an M1 Abrams Main gun, featuring 2 types of ammunition
and the coaxially mounted machinegun, and the base cost of each option listed in
brackets after it:

* 120mm gun / 7.62mm coaxial MG - Choose one:
  * AP: 48", A1, AP(4), Deadly(6) [12]
  * HEAT: 36", A1, AP(3), Blast(3), Deadly(3) [11.25]
  * MG: 12", A3 [0.75]

Since the AP ammunition is the most expensive, it is what is applied to the base
unit cost.

As another example, the above 2 rules lead to the following entry for a BMP-2,
its coaxial MG, and the ATGM upgrade (there's a 40mm grenade launcher, but I
didn't list that here).

* 30mm gun / 7.62mm coaxial MG - Choose one:
  * AP: 24", A2, AP(2) [2]
  * Frag-HE: 48", A2, AP(1), Blast(3) [9]
  * MG: 12", A3 [0.75]
* Add Kornet ATGM system
  * ATGM: 48", A1, AP(4), Deadly(6) [12]

So in the above, the unit will be costed with the Frag-HE ammo, with the ATGM as
a (relatively expensive) upgrade.

## Ammunition

It is assumed that units all carry sufficient ammunition for an engagement, as
even add-on anti-tank missile systems carry extra stowed missiles which can be
reloaded into the launcher, sometimes even under fire via retractable launchers,
flip up ballistic protection, or even simply hiding behind a hill. Tanks are
better suited for this role, carrying more rounds and having them more readily
accessible.

The notable exception here are various one-shot "disposable" launchers which are
generally issued to infantry at a rate of one per squad or section, to give them
a limited anti-tank capability. This is useful, but not modeled in the current
rules. Hence I will have to add a Limited(X) rule, at a cost of X/4 (assuming a
4 turn game).

## Gun stabilization, computers, and quality

One of the major technological changes in this time period was the multi-axis
gyrostabilized gun. You can see this in videos when comparing footage of WWII
tanks with that of modern tanks. Watch them going over uneven terrain and see
how the tank barrel moves with the chassis in the older tanks and remains flat
on the modern tanks.

Another, less famous, but certainly no less important advancement is that of
ballistic computers. They were used on naval vessels for decades - even before
digital computers, there were analog computers built into the ship - but at the
same time home computers became available in the late 1970's, specialized
digital computers started to be employed in production military vehicles. As
these systems evolved, more and more data got fed into the computer, with
factors such as type of projectile, wind, barrel wear, barrel droop, and range
all being used to increase the probability of a first round hit. This was widely
conveyed in stories from the two Gulf Wars, where US Abrams tanks would hit
Iraqi targets before the Iraqis even knew the Americans were there - they
thought they were under attack by artillery or aircraft. In other stories, the
Iraqis realized the Americans were there, and tried to fire back, only to have
their rounds fall short. The Iraqis tried to close the distance, but took
tremendous casualties doing so.

Anyway, explanation notwithstanding, I need to decide how to handle the above.

In reverse order:

The ballistic computer is going to be figured into the effective range of the
gun. Honestly, I don't really even need to do much - the tank/vehicle/etc. has
stated effective range for the various weapons systems in the technical
literature. All that needs to be done is to look it up in the above table,
calculate points, and it's done.

The stabilized gun is trickier because it figures into movement - typically,
vehicles would have to move, stop, shoot, then resume moving. With the addition
of a stabilized gun, they no longer had to stop. However, given that the basic
rules model assumes either moving slowly (an advance) and shooting or moving
fast (a rush) and not shooting (effectively a double move if you don't shoot),
the solution here is to have units with stabilized guns termed Fast. The
rationale is that the Fast vehicle doesn't need to stop to shoot, so it covers
more ground. However, the vehicle with the unstabilized gun does, so it's not
Fast. If it wants to go quickly, it should double move (and not shoot). This
does mean that if both vehicles Rush, the Fast vehicle will go faster than the
non-Fast vehicle, but vehicles with stabilized guns tend to be modern and faster
anyway, so that's not that big of a deal.

Note that this stabilized / unstabilized distinction only applies to vehicles
with a large caliber main gun, and is ignored in the case of machinguns.
Machineguns generally carry enough ammunition that they can just hose down an
area as they're bouncing around and that will get the job done. Plus, I don't
want to worry about it (there, I said it). Basically, anything around a 30mm
cannon and below are going to be treated like machineguns for the purposes of
this game.

## Quality

The following quality guidelines apply, and are consistent with those from the Point Calculator:

| Quality | Description                                        |
| ------- | -----------                                        |
| 6+      | Irregular forces with minimal training.            |
| 5+      | Regular forces with little combat experience. Experienced irregular forces.|
| 4+      | Regular forces that are combat veterans.           |
| 3+      | Elite special forces.                              |
| 2+      | Legendary operators (medal of honor winners, etc.) |

As is recommended, quality 6+ and 2+ will be sparingly used - for militia mobs
and high military honors winners, respectively.