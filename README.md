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
