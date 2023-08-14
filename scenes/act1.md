# act1

```
SceneSetup.act1();
```

(...300)

n: TOTO JE LIDSKÁ ÚZKOST

n: _TY_ JSI TA ÚZKOST

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}



# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: Hele! My jsme zas tady?

`hong({eyes:"0_neutral"})`

n: TVÁ PRÁCE JE OCHRÁNIT SVÉHO ČLOVĚKA PŘED *NEBEZPEČÍM*

`bb({eyes:"look", mouth:"small_lock"})`

n: VE SKUTEČNOSTI, HRANÍ TÉTO HRY ZNOVU HO VYSTAVUJE *NEBEZPEČÍ* PRÁVĚ TEĎ

n: RYCHLE, VARUJ HO!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Člověče! Poslyš, jsme v nebezpečí! Hráč...

[...nás bude zase mučit!](#act1_replay_torture)

[...nenajde alternativní konec!](#act1_replay_alternate)

[...se dostane do ludo-narativní disonance!](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: Donutí nás stočit se do klubíčka a brečet!
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: Donutí nás rozbít ti mobil protože ti zbůsobil záchvat paniky!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: Donutí nás *NE*praštit hostitele té párty!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight"}}
b: Donutí nás praštit toho sympaťáckýho hostitele!
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: Hele, možná tentokrát neskočíme z té střechy--
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b: DONUTÍ NÁS SKOČIT Z TÝ STŘECHY.
{{/if}}

`bb({body:"fear"});`

b: VŠECHNY TYHLE NOVÝ VĚCI SE NÁM STANOU, A PAK--

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Jasně, ten příběh v *celku* je stejnej, ale každá kapitola má dva konce, plus všechny dialogové možno--

`bb({body:"fear"});`

b: Hráč bude zklamán, vypne tabulku v prohlížeči, vymaže náš software a pak--

(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Laudo-co?

`bb({eyes:"normal"});`

b: Příběh byl o tom, že se můžeš *ROZHODNOUT* postavit zdravý vztah se svým strachem,

`bb({eyes:"normal_right"});`

b: Ale hraní této hry znovu dokáže dodat pouze stejný příběh,což implikuje že tvé *ROZHODNUTÍ* jsou bezvýznamné,

`bb({eyes:"narrow_eyebrow"});`

b: Což ukazuje konflikt mezi významem hry a jejími dovednostmi,

`bb({eyes:"fear"});`

b: Což rozhrnuje vrstvy naší narativní dimenze,

`bb({body:"fear"});`

b: A pak--

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: UMŘEEEEEEEEEEEEEEEEEM

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.clearText();
```

(...1001)

```
bb({body:"laugh"});
hong({body:"laugh"});
Game.clearText();
sfx("laugh");
```

(...5001)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({body:"0_sammich"});
```

h: Tak jo, zpátky do rolí.

```
Game.clearText();
```

n4: (NECH _TVOJI_ ÚZKOST BLA BLA BLA NEJPODOBNĚJŠÍ K _TVÉMU_ STRACHU BLA BLA VÍŠ JAK NA TO)

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: Á, můj vlk se vrátil. Faaantastický.

`hong({eyes:"0_neutral"})`

n: TVŮJ ÚKOL JE OCHRÁNIT SVÉHO ČLOVĚKA PŘED *NEBEZPEČÍM*

`bb({eyes:"look", mouth:"small_lock"})`

n: VE SKUTEČNOSTI, TEN SENDVIČ HO VYSTAVUJE *NEBEZPEČÍ* PRÁVĚ TEĎ

n: RYCHLE, VARUJ HO!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Člověče! Poslyš. jsme v nebezpečí! To nebezpečí je...

`bb({body:"squeeze"})`

n4: (NECH _SVOJI_ ÚZKOST SI HRÁT! VYBER SI TO NEJPODOBNĚJŠÍ K TOMU CO ŘÍKÁ _TVŮJ_ STRACH)

(#act1_normal_choice)

# act1_normal_choice

[Obědváme sami! Zase!](#act1a_alone) `bb({body:"squeeze_talk"})`

[Nejsme produktivní při obědvání!](#act1a_productive) `bb({body:"squeeze_talk"})`

[Ten bílý chléb je pro nás nezdravý!](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: Snad nevíš že samota je spojena s předběžnou smrtí stejně jako kouření 15 cigaret denně?-

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad 2010, PLoS Medicine)

`hong({eyes:"0_annoyed"})`

h: Ehm, děkuji že cituješ své zdroje, ale--

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: Což znamená že pokud *ihned* nebudeme s někým trávit čas, tak-

`bb({body:"panic"})`

b: UMŘEMEEEEEEEEEEE

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: POUŽIL JSI *STRACH Z NEMILOSTI*

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: Vytáhni s noťas a začni ihned pracovat na něčem!

`hong({eyes:"0_annoyed"})`

h: Ehm, radši bych si nenadrobil do klávesnice--

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Pokud jakkoli nepřispíváme k tělesu společnosti, tak jsme společnostní parazit!

b: Společnostní těleso půjde k společnostnímu doktorovi pro prášky na společnostní parazity a pak--

```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: UMŘEMEEEEEEEEEEE

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n: POUŽIL JSI *STRACH Z ŠPATNÉHO SVĚDOMÍ*

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: Byly ty studie repliková--

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Zpracovaná pšenice nám zvýší hladinu krevního cukru takže nám amputujou všechny končetiny a pak-

`bb({body:"panic"})`

b: UMŘEMEEEEEEEEEEE

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: POUŽIL JSI *STRACH Z UBLÍŽENÍ*

(#act1b)

# act1b

n: JE TO SUPER EFEKTIVNÍ

`bb({mouth:"smile", eyes:"smile"});`

b: Vidíš, člověče? Já jsem tvůj strážný pes!

`bb({body:"pride_talk"});`

b: Věř svému instinktu! Tvé pocity jsou vždy platné!

`bb({body:"pride"});`

n: DOSTAŇ MĚŘÍTKO ENERGIE ČLOVĚKA NA NULU

n: K OCHRANĚ JEJICH FYZICKÝCH + SOCIÁLNÍCH + MORÁLNÍCH POTŘEB, MŮŽEŠ POUŽÍT:

n: STRACH Z *UBLÍŽENÍ* #harm#

n: STRACH Z *NEMILOSTI* #alone#

n: A STRACH Z *ŠPATNÉHO SVĚDOMÍ* #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: (RADA: HRAJ MOŽNOSTI, KTERÉ OSOBNĚ ODPOVÍDAJÍ *TVÉMU* STRACHU!~)

h: ...

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: víš co je asi načase abych si zkontroloval mobil.

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: OCHRAŇ SVÉHO ČLOVĚKA.

n: PŘED SVĚTEM. PŘED LIDMI. PŘED SEBOU.

n: HODNĚ STĚSTÍ

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: ROUND ONE: *FIGHT!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: Hmm. Facebook mi říká že tenhle víkend bude nějaká párty.

`bb({eyes:"uncertain"});`

b: Nedělá ten podivín *každej* víkend párty?

`bb({eyes:"uncertain_right"});`

b: Jakou vnitřní hlubinu se snaží zaplnit? V jeho hlavě to musí být hrozně zamotaný!

`hong({eyes:"surprise"});`

h: Taky jsem dostal pozvánku?

`bb({eyes:"fear", mouth:"normal"});`

b: Nuže!

[Pojďme, nebo zemřeme na samotu!](#act1c_loner)

[Nechoďme, je to plný jedovatých drog!](#act1c_drugs)

[Nevšímej si toho, párty s náma jsou smutný.](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: Patnáct cigaret denně, člověče! Patnáct!
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: Pak se nikdo nezastaví na náš pohřeb, vysypou náš popel do moře, sežere nás velryba,
{{/if}}

{{if !_.fifteencigs}}
b: a vznikne z nás VELRYBÍ VÝKAL!
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: Takže jo, měli bychom jít na tu párty!
{{/if}}

{{if _.parasite}}
b: Jen si vezmi notebook abychom mohli pracovat, a nebýt společnostní parazit.
{{/if}}

{{if _.whitebread}}
b: Hlavně ale nesmí servírovat BÍLÝ CHLEBA
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: PROBOHA. Pokud už ztichneš, tak fajn.

h: Řeknu že půjdu.

{{if _.whalepoop}}
b: Velrybí výkal, člověče! Velrybí výkal!
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: a nebo by tam mohl být... BÍLÝ CHLEBA
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: Předávkujeme se na tak moc pervitinu a chlebu že se naše tlusté tělo nenarvou do spalovny!
{{/if}}

{{if !_.whitebread}}
b: Předávkujeme se na tolika drogách, že hrobník bude přemýšlet, jak jsme přijeli *už* zabalzamovaný!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: Ostatně, nemůžem jít na párty, musíme pracovat jinak jsme hrozný společnostní parazit!
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: PROBOHA. Pokud už ztichneš, tak fajn.

h: Řeknu že nepůjdu.

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: Jedinou věc kterou děláme je to, že brečíme v rohu že samota je stejně smrtelná jako 15 cigaret denně.
{{/if}}

{{if _.parasite}}
b: Jedinou věc kterou děláme je to, že se stresujeme nad tím, že bychom měli pracovat.
{{/if}}

{{if _.whitebread}}
b: Jedinou věc kterou děláme je to, že se stresujeme nad tím, že nás nezdravá nabídka jídla zabije.
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: to by mě tak zajímalo proč.

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: Takže když půjdem tak budou nešťastní, ale když odmítnem tak taky budou nešťastní!

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: JEDINÝ CO UMÍME JE KAZIT LIDEM NÁLADU, TAKŽE BYCHOM MĚLI BÝT NEŠŤASTNÍ

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: Uf. Pokud už ztichneš, tak fajn.

h: Budu to ignorovat.

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: Nicméně. Facebook je na mě moc. Potřebuju něco klidnějšího, míň úzkostnýho.

`hong({eyes:"neutral"});`

h: Co je nového na Twitteru?

`bb({eyes:"look"});`

[Ale ne! Podívej se na ty hrozné zprávy!](#act1d_news)

[Ó né, je ten tweet tajně o *nás?*](#act1d_subtweet)

[Hele, GIF s kočičkou která pije mlíčko](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: Proboha, je to jako kdyby náš svět hořel, ne?

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: Jako že to všechno končí, všechno umírá a všechno je v háji a nic s tím nemůžeme udělat.

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: Pojďme to retweetnout!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Tak jo, retweetnu to, prostě buď potichu prosím!

`hong({mouth:"neutral", eyes:"annoyed"});`

h: Kašlu na to, podívejme se na Snapchat.

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: Je to subtweet! Šikovný, mazaný subtweet!

`hong({eyes:"annoyed"});`

h: Pravděpodobně ne?

`bb({eyes:"narrow", mouth:"small"});`

b: a co když všichni mluví za našimi zády

h: Nemluv--

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: PŘED NAŠEMI ZÁDY

`hong({eyes:"sad", mouth:"sad"});`

h: Já ne--

`bb({eyes:"narrow", mouth:"small"});`

b: ale *co když*

h: Přest--

`bb({eyes:"narrow_eyebrow"});`

b: *co když*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ...

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: o-KEJ, zkusíme Snapchat.

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: Heh, jo to je roztomilý, zrovna jsem to retweetnul--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: KOČKY NEMOHOU TRÁVIT MLÉKO A JSME HROZNÍ PROTOŽE MÁME RÁDI ZVÍŘECÍ NÁSILÍ

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("18p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: o-KEJ, zkusíme Snapchat.

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: Hm, fotky z včerejšího večera. Takže *takový* jsou ty párty...

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: Uf, docela dost lidí, jen takhle to vypadá nepříjemně.

h: Možná jsem to neměl příjmout?

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[Změnit naší odpověď? Jak zbabělec?!](#act1e_yes_dontchange)

[Změň naší odpověď! Je tam moc narváno!](#act1e_yes_changetono)

{{if _.subtweet}}
[Jo, rozhodně to byl subtweet.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Moment my jsme retweetli bez kontroly zdrojů.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Víš že sedíš jako prase? Co tvoje záda?](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Počítali s náma a teď jsme je zradili? Chceš snad zemřít o samotě?!

{{if _.fifteencigs}}
b: PATNÁCT. CIGARET.
{{/if}}

{{if _.whalepoop}}
b: VELRYBÍ. VÝKAL.
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Ztichni ztichni půjdu tam!

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Ty snad nevíš o smrti ušlapáním?

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: V roce 2003 začal hořet klub na Rhode Island a ta panika z toho ucpala lidmi východy takže 100 lidí uhořelo-

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: CHCEŠ SNAD ABY SE TO STALO NÁM-

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: ŘEKNI NE ŘEKNI NE ŘEKNI NE ŘEKNI NE ŘEKNI NE ŘEKNI NE ŘEKNI NE ŘEK-


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Ztichni ztichni řeknu že nemůžu! Proboha!

(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: Hm... to vypadá docela zábavně.

h: Možná jsem to neměl odmítnout?

`bb({mouth:"normal", eyes:"normal"});`

[Změnit naší odpověď?! Jak nějakej šmejd?!](#act1e_no_dontchange)

[Změň naši odpověď! Neumírejme o samotě!](#act1e_no_changetoyes)

{{if _.subtweet}}
[Jo, rozhodně to byl subtweet.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Moment retweetnuli jsme bez kontroly zdrojů.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Víš, že sedíš jako prase? Co tvoje záda?](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: Všichni s náma počítali!

b: ...abychom tam nešli a aby si mohli užít pořádnou párty bez hrozný odporný {{if _.whitebread}}bílo-chlebo-žeroucí{{/if}} bytosti jako ty--


```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Ztichni ztichni nepůjdu tam!

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Chronická samota by zvýšila naše hladiny kortizolu společně s rizikem kardiovaskulárního onemocnění a mrtvice!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: PATNÁCT. CIGARET.
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Ztichni ztichni, půjdu tam! Proboha!

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Všechny naše problematické tweety se vrací!

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: Někdo je najde a pak nás zruší a přivážou nás ke koni lanem a potáhnou nás po informační superdálnici!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Proč musíš být takovejdle?!

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Rozšiřujeme dezinformace! Ničíme důvěru v nezávislé zpravodajství!

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Budeme důvod proč fašismus vyleze z trosek demokracie!

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
_.factcheck = true;
```

h: Proč musíš být takovejdle?!

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Chceš mít místo páteře preclík? Přestaň se ohýbat tak nad tou obrazovkou!

```
bb({body:"meta"});
```

b: Tím myslím I tebe.

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Proč musíš být takovejdle?!

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: Hm... to vypadá docela zábavně.

h: Možná jsem neměl ignorovat tu pozvánku?

`bb({mouth:"normal", eyes:"normal"});`

[Pořád to ignoruj, jen bychom to zkazili.](#act1e_ignore_continue)

[Moment, řekni ano.](#act1e_ignore_changetoyes)

[Moment, řekni ne.](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: Neni to trochu drzý?

`bb({eyes:"normal_right"});`

b: No ostatní lidi taky ignorujou *nás*, takže

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: řekneme že si jsme kvit.

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: Ty.. mě necháš jít?

b: No, jako, samota nás *může* zabít.

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: Moc lidí. Davy jsou nebezpečné.

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: No nic. Nová tinder notifikace.

`bb({eyes:"uncertain"})`

b: Co, ta seznamka?

`hong({eyes:"annoyed"})`

h: Není to seznamka, je to jen způsob jak poznat nový lidi--

`bb({eyes:"narrow"})`

b: Je to seznamka.

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: Hele, mám match! Vypadají roztomile.

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: Nekaž mi to, prosím--

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: POZOR POZOR POZOR POZOR POZOR POZOR

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[Oni nás *zneužívají*.](#act1f_used_by_others)

[*Zneužíváme* další lidi.](#act1f_using_others)

[TVŮJ MATCH JE SÉRIOVÝ VRAH](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: Náhodný seznamky sice vyplní díru tady,

b: ale nikdy nevyplní díru...

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b:*tady*.

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: To co se snažím říct je to ŽE UMŘEM O SAMOTĚ

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: Ty si myslíš že genetálie ostatních lidí jsou pro nás jak Pokémoni?

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ (znělka pokémonů)-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ Já bych chtěl být, ten nej^kurvi^těj-ší-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ Jako nikdo přede mnou-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ Stehna, ^prdel^, obrovské prsa-

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ s upoceným ^ptákem^ a koulema!-

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ UCHYL-MON! VŠECHNY CHY-

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: To co snažím říct je to, že jsme manipulativní úchyláci.

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: Narvou tě do studny a budou tě krmit jen bílý chleba aby jsi ztloustnul aby mohli nosit tvoji kůži jako oblek!
{{/if}}

{{if _.parasite}}
b: Umlátí tě k smrti s minutkou a řeknou ti že si měl BÝT VÍC PRODUKTIVNÍ TY PARAZITE"
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: Roztrhaj ti kůži na krvavé konfety, z tvých vnitřností vyrobí stuhy a tvou krev zamíchají do punče!
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: TO by byla pořádná párty, co?!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ...

(...500)

h: jsem tak unavenej z týhle hry.

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"samota nás zabije"... {{/if}}
{{if _.parasite}}"jsme společnostní parazit"... {{/if}}
{{if _.whitebread}}"nejez to, zabije nás to"... {{/if}}
{{if _.subtweet}}"mluví nám za zádama"... {{/if}}
{{if _.badnews}}"svět hoří"... {{/if}}
{{if _.hookuphole}}"umřeme o samotě"... {{/if}}
{{if _.serialkiller}}"je to sériový vrah"... {{/if}}
{{if _.catmilk}}"kočky nemůžou trávit mléko"... {{/if}}
{{if _.pokemon}}na ^hovno^ parodie pokémonů... {{/if}}

h: chci prostě žít svůj život.

h: chci být svobodný od téhle... bolesti.

`bb({eyes:"look_sad"});`

b: Hej... člověče...

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: Bude to vpohodě.

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: Jako tvůj věrný strážný pes, vždy budu hledat nebezpečí, a zkusím tě co nejlépe před ním ochránit.

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: Slibuji.

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: Poslední appka. Instagram. Co to bude?

`hong({eyes:"sad"});`

h: Víc... víc fotek z párty.

`hong({mouth:"sad"});`

h: Všichni vypadaj tak vesele. Bez stresu. Bez úzkosti.

`hong({mouth:"anger"});`

h: Sakra, proč nemůžu být jak oni? Proč nemůžu být *normální?*

`bb({eyes:"normal_right"});`

b: Když už mluvíme o párty, ohledně tohodle víkendu, tohle je mé FINÁLNÍ rozhodnutí:

`bb({eyes:"normal"});`

[Měli bychom jít.](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[Neměli bychom jít.](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: Měli by--

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *^NASER^.*

`hong({body:"2_you"});`

h: SI.

(...500)

b: c

(...1500)

`bb({eyes:"wat_2"});`

b: co?

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: Já řeknu že PŮJDU na tu párty,

{{if _.act1g=="go"}}
h: NE protože ty chceš, ale protože *JÁ* chci.
{{/if}}

{{if _.act1g=="dont"}}
h: Právě kvůli tomu že NECHCEŠ abych šel.
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: NEOVLÁDÁŠ mě.

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: A teď mě omluv, zatím co si sním tento lahodný sendvič v ^zasraným^ klidu.

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ...

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ...

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[AAAAA UMŘEMEE](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[AAAAA VŠICHNI NÁS NESNÁŠÍ](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[AAAAA JSME HROZNÍ LIDI](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AAAAA UMŘEMEEEE AAAAAAAAAAA

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AAAAAA VŠICHNI NÁS NESNÁŠÍ AAAAAAA

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AAAAAAAA JSME HROZNÍ LIDI AAAAAAAAA

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: GRATULUJI

(...500)

n: ÚSPĚŠNĚ JSI OCHRÁNIL FYZICKÉ + SOCIÁLNÍ + MORÁLNÍ POTŘEBY TVÉHO ČLOVĚKA

n: JEN SE PODÍVEJ, JAK TI JSOU VDĚČNÝ!

(...500)

n: A TEĎ KDYŽ JEJICH ENERGIE JE NA NULE, MŮŽEŠ PŘÍMO OVLÁDAT JEJICH AKCE

`bb({mouth:"smile", eyes:"normal"});`

n: VYBER SI SVŮJ FINISHER

`bb({mouth:"small_lock", eyes:"fear"});`

n: *FINISH THEM*

[{FIGHT: Potrestej svůj stresující mobil!}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{FLIGHT: Stoč se do klubíčka a breč!}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: Tvůj mobil ti dával úzkostný záchvat!

`bb({eyes:"anger"})`

b: Zuckerberg a Přátelé se ti vbourali do mentálního zdraví aby z tebe vymlátili tvé veškeré prachy!

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Potrestej svůj mobil! Znič ho! Zab ho!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: ZAB HO ZAB HO ZAB HO ZAB HO ZAB HO ZAB HO ZAB HO ZAB HO ZAB HO ZAB HO ZAB HO ZAB HO ZAB H--

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: Celý svět je plný nebezpečí!

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Udělej to jak Pásovec! Stoč se do klubíčka pro sebeochranu! 

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: STOČ SE A BREČ STOČ SE A BREČ STOČ SE A BREČ STOČ SE A BREČ STOČ SE A BREČ STOČ SE A BREČ ST-- 

(#act1j)

# act1j

`SceneSetup.act1_outro()`
