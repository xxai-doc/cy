<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Mae rhan o god y wefan yn ffynhonnell agored, croeso i chi helpu i wneud y gorau o'r cyfieithiad.

## cod pen blaen

* [cod pen blaen](https://github.com/xxai-art/web)
* [Pecynnau iaith ar gyfer y wefan gyfan](https://github.com/xxai-art/web/tree/main/i18n)
* [Pecynnau iaith ar gyfer modiwlau mewngofnodi](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Dogfennaeth Amlieithog y Wefan](https://github.com/xxai-doc)

Yr iaith raglennu pen blaen yw [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , sy'n ychwanegu rhai nodweddion yn seiliedig ar gystrawen y coffeescript, gweler [./coffee_plus.md](./coffee_plus.md) .

## Rhyngwladoli gwefannau a dogfennau

Adeiladu ar y 3 phrosiect canlynol

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Yr ôl-ddodiad yw `.mdt` , gallwch ddefnyddio'r gystrawen debyg i `<+ ./coffee_plus/import.js>` i gyfeirio at ffeiliau allanol, a chynhyrchu marcio i lawr gyda'r ôl-ddodiad `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Ni fydd cyfieithiad Markdown yn cyfieithu codau a dolenni, a bydd yn storio brawddegau wedi'u cyfieithu. Os caiff y cyfieithiad ei addasu ond nad yw'r testun gwreiddiol wedi'i addasu, ni fydd ei gyflawni eto yn trosysgrifo addasiad y cyfieithiad.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Ffeiliau iaith ar gyfer cyfieithu gwefannau a gynhyrchir gan `yaml` .

### Cyfarwyddiadau Awtomeiddio Cyfieithu Dogfennau

Gweler ystorfa [xxai-art/doc](https://github.com/xxai-art/doc)

Argymhellir gosod nodejs, [direnv](https://direnv.net) a [bun](https://github.com/oven-sh/bun) yn gyntaf, ac yna rhedeg `direnv allow` ar ôl mynd i mewn i'r cyfeiriadur.

Er mwyn osgoi warysau rhy fawr wedi'u cyfieithu i gannoedd o ieithoedd, creais warws cod ar wahân ar gyfer pob iaith a chreu sefydliad i storio'r warws hwn

Bydd gosod y newidyn amgylchedd `GITHUB_ACCESS_TOKEN` ac yna rhedeg [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) yn creu'r warws yn awtomatig.

Wrth gwrs, gallwch chi hefyd ei roi mewn warws.

Cyfeirnod sgript cyfieithu [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Dehonglir y cod sgript fel a ganlyn:

[Bunx](https://bun.sh/docs/cli/bunx) yn lle npx, sy'n gyflymach. Wrth gwrs, os nad oes gennych byn wedi'i osod, gallwch ddefnyddio `npx` yn lle hynny.

`bunx mdt zh` yn rendr `.mdt` yn y cyfeiriadur zh fel `.md` , gweler y 2 ffeil cysylltiedig isod

* [coffi_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffi_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` yw'r cod craidd ar gyfer cyfieithu (os mai dim ond `nodejs` sydd gennych wedi'u gosod, ond nid yw `bun` a `direnv` wedi'u gosod, gallwch hefyd redeg `npx i18n` i gyfieithu).

Bydd yn dosrannu [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , mae ffurfwedd `i18n.yml` yn y ddogfen hon fel a ganlyn:

```
en:
zh: ja ko en
```

Yr ystyr yw: cyfieithiad Tsieineaidd i Japaneeg, Corëeg, Saesneg, cyfieithiad Saesneg i bob iaith arall. Os mai dim ond Tsieinëeg a Saesneg rydych chi eisiau, gallwch chi ysgrifennu `zh: en` .

Yr olaf yw [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , sy'n tynnu'r cynnwys rhwng y prif deitl ac is-deitl cyntaf `README.md` pob iaith i greu cofnod `README.md` . Mae'r cod yn syml iawn, gallwch chi edrych arno'ch hun.

Defnyddir Google API ar gyfer cyfieithu am ddim. Os na allwch gael mynediad i Google, ffurfweddwch a gosodwch ddirprwy, fel:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Bydd y sgript cyfieithu yn cynhyrchu celc cyfieithu yn y cyfeiriadur `.i18n` , gwiriwch ef gyda `git status` a'i ychwanegu at y storfa god i osgoi cyfieithiadau ailadroddus.
