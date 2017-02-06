# txscript

Eventually: decodes txscript data to strings

Right now: decodes the DATA/PUSHDATA op-codes (and their associated data blobs) to strings (emphasis on input scripts because existing libraries/websites don't do these very transparently).

## Usage

```sh
$ txscript 473044022001220a67bf74be2f1d1c6b9ed8d3fc55347cf30aaf4ea3a1118363ee450093850220634a3738091f6b72d9acdad0e02e1b11b3e0515cdfa40edb391349ca4a20545d024dc10100202020202020202020202020202020202020202000763237735372612e6a7067202020202020202020002020202020202020202020202020202020202020002f396a2f34414151536b5a4a5267414241514541534142494141442f327742444143676348694d654753676a49534d744b79677750475242504463335048745958556c6b6b59435a6c6f2b41006a497167744f62446f4b72617259714d79502f4c327537312f2f2f2f6d38482f2f2f2f362f2b62392f2f6a2f32774244415373744c54773150485a42515862347059796c2b506a342b506a34002b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a2f776741524341474141674144415245410041684542417845422f385141474141414177454241414141414141414141414141414141414145434177542f7841415741514542415141414141414141414141414141414141414141514c2f003267414d41774541416841444541414141586e544746454a4653455349777341415968415562797359786742496841494267535a49315978456d7859774a4945414341426741774141676f4e004dcf010035617167674554556f695248505967474d514142305373734147424968414951786b475355714b4553626c67424a41674142414d4267414242514275746c6c49434d316845514977736b414b004a41426d3874466c444743776b69454951786b47513043315242755741456b434141454d41474177454d514778533644545378526b314353535359325141464567417a6557696969687274630034793545694151774a4d6b59796c314d44557341494a4541414959414d5941414341324b57796a4a4e5356684a4a4a4d6b696b425249414d326c736f6f6f6c64456b7a4549516867535a5742005543376d427355414545694141454d42674d41414241616c464b7a4a4e5643556b6b6b7a53616b41414141316c304b4b47496b6f6b51684347424a6b6854417157446f4b414343514541434700417747414141686c773659456c6742496953444b78414d4241427446725251434a4b454951434742426d68514263734a304c51415a6945414149594447414141434756425445496f5941496b006778734147416741316a526147494352674167454d43444a43676355736e534141514951414168674d5941414149597747494267417845694d4c41414749414e4931566a4541414941454144004dcf0100494d7241414c6c6c4f6c514149454941415177474d414141454d4267454155414d51674f657741426941433431566a4a415941424977415a426c59414f4749365641417a454141414141786700414141674741414144414145426859674159674173755756744a57696b4241516f6c674241694c4143705a73365a5741693651444d6f6b5177474d414142414177414141426c6a46515a6f6a00455178414252704b6c614a61536841424b694d59456b4c4e79446c7051614e4b6152646a41444f4a4159444741414167454d594141414d306f4542434977454d514161533355536c7a73577200415a6d6b714a4d6f424e6b47684d54524c53736153436955614b4c69797747417867414149435570514147414141434d6b564f554a735952713143557457516d686f555571475949784458590041706e4a49524367693173675355426253544a4b41594441414741674953314141414a4555555a4a466154515369734279364b784475646936414b584f476741696c59776f4d5a416c637a5100555130347257576d63726143554542674d514b79556f414953314141444f7943356156704a4a5330516c704a46584e55576c325774444742494441414151686a4a455a6c444d70556d31694d004c6da9143627dc4a186fbfeef21e8bc6613f90ee78192ad288a914f6232995824ce822d325ff6e42a27d774f79147988a914d773e70106a74ea27b4c574c1627d6de2741c600882103af5d78c03ea0c982e0f58f7a8d7a22baf35e022497b01eaeb773b20234e263ffad0075740087

OP_DATA_71
3044022001220a67bf74be2f1d1c6b9ed8d3fc55347cf30aaf4ea3a1118363ee450093850220634a3738091f6b72d9acdad0e02e1b11b3e0515cdfa40edb391349ca4a20545d02
OP_PUSHDATA2(449)
00202020202020202020202020202020202020202000763237735372612e6a7067202020202020202020002020202020202020202020202020202020202020002f396a2f34414151536b5a4a5267414241514541534142494141442f327742444143676348694d654753676a49534d744b79677750475242504463335048745958556c6b6b59435a6c6f2b41006a497167744f62446f4b72617259714d79502f4c327537312f2f2f2f6d38482f2f2f2f362f2b62392f2f6a2f32774244415373744c54773150485a42515862347059796c2b506a342b506a34002b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a342b506a2f776741524341474141674144415245410041684542417845422f385141474141414177454241414141414141414141414141414141414145434177542f7841415741514542415141414141414141414141414141414141414141514c2f003267414d41774541416841444541414141586e544746454a4653455349777341415968415562797359786742496841494267535a49315978456d7859774a4945414341426741774141676f4e00
OP_PUSHDATA2(463)
0035617167674554556f695248505967474d514142305373734147424968414951786b475355714b4553626c67424a41674142414d4267414242514275746c6c49434d316845514977736b414b004a41426d3874466c444743776b69454951786b47513043315242755741456b434141454d41474177454d514778533644545378526b314353535359325141464567417a6557696969687274630034793545694151774a4d6b59796c314d44557341494a4541414959414d5941414341324b57796a4a4e5356684a4a4a4d6b696b425249414d326c736f6f6f6c64456b7a4549516867535a5742005543376d427355414545694141454d42674d41414241616c464b7a4a4e5643556b6b6b7a53616b41414141316c304b4b47496b6f6b51684347424a6b6854417157446f4b414343514541434700417747414141686c773659456c6742496953444b78414d4241427446725251434a4b454951434742426d68514263734a304c51415a6945414149594447414141434756425445496f5941496b006778734147416741316a526147494352674167454d43444a43676355736e534141514951414168674d5941414149597747494267417845694d4c41414749414e4931566a454141494145414400
OP_PUSHDATA2(463)
00494d7241414c6c6c4f6c514149454941415177474d414141454d4267454155414d51674f657741426941433431566a4a415941424977415a426c59414f4749365641417a454141414141786700414141674741414144414145426859674159674173755756744a57696b4241516f6c674241694c4143705a73365a5741693651444d6f6b5177474d414142414177414141426c6a46515a6f6a00455178414252704b6c614a61536841424b694d59456b4c4e79446c7051614e4b6152646a41444f4a4159444741414167454d594141414d306f4542434977454d514161533355536c7a73577200415a6d6b714a4d6f424e6b47684d54524c53736153436955614b4c69797747417867414149435570514147414141434d6b564f554a735952713143557457516d686f555571475949784458590041706e4a49524367693173675355426253544a4b41594441414741674953314141414a4555555a4a466154515369734279364b784475646936414b584f476741696c59776f4d5a416c637a5100555130347257576d63726143554542674d514b79556f414953314141444f7943356156704a4a5330516c704a46584e55576c325774444742494441414151686a4a455a6c444d70556d31694d00
OP_PUSHDATA1(109)
a9143627dc4a186fbfeef21e8bc6613f90ee78192ad288a914f6232995824ce822d325ff6e42a27d774f79147988a914d773e70106a74ea27b4c574c1627d6de2741c600882103af5d78c03ea0c982e0f58f7a8d7a22baf35e022497b01eaeb773b20234e263ffad0075740087
```