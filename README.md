# BR Brasil - Clima Real

![BR Brasil - Clima Real](images/cover.png)

**Feel the Brazilian summer on every journey.** Regional dashboard temperatures for **Euro Truck Simulator 2 + BR Brasil**, with changing weather states and gradual geographical transitions.

[Download the latest version](https://github.com/Rhaiderr/ets2-brbrasil-climate/releases/latest) · [Support the project](https://buymeacoffee.com/leonardoarouck) · [Português](#português-brasil)

The coast, inland roads and highlands deserve different temperatures. Clima Real brings regional summer references into your truck's dashboard: cooler nights, warmer afternoons, milder spells and occasional strong heat. The maximum is not a fixed daily ceiling, and the same journey can feel different as the game's weather changes.

## What you get

- **Regional coverage across the supported BR Brasil map:** 1,019 sectors receive climate profiles built from 42 reference locations.
- **Variation beyond the daily cycle:** native weather states include milder and hotter conditions, with an uncommon heat tail.
- **Smoother transitions:** nearby regions share geographical interpolation and coordinated thermal states, rather than receiving an independent temperature draw for each city.
- **A single mod:** no external plugin or background application is required.

## Download and installation

Tested target: **BR Brasil 6.1 / ETS2 1.62**. BR Brasil is required and is not included.

1. Back up your existing profile and saves.
2. Download `brbrasil-clima-real-verao.scs` from [Releases](https://github.com/Rhaiderr/ets2-brbrasil-climate/releases/latest). The ZIP download contains the same mod plus its guide.
3. Copy the `.scs` file into your ETS2 `mod` folder.
4. Activate **BR Brasil - Clima Real** **above all BR Brasil map packages** in the Mod Manager, giving it higher priority.
5. Disable older Clima Real versions. Use only one copy, whether installed manually or through Workshop.

An existing profile can be used. Other weather mods can overwrite the same climate definitions; **Weather_3.9 compatibility has not been validated**. Keep it disabled for your first test. Review compatibility again when the game or map updates.

## How the temperatures are built

The summer baseline uses **ten December–February seasons, 2015/16 through 2024/25**, with **903 daily minimum/maximum pairs per reference location**, from Open-Meteo's ERA5-Land historical reanalysis. These are regional reference data, not live readings or individually validated records for every city.

Daily pairs are ranked by their maxima to produce linked mild, typical and hot regimes, retaining corresponding nighttime minima. An observed IAC/CIIAGRO Santos heat event (40.3°C in February 2010) informs a rare warm tail; it is not presented as an all-time city record.

At each supported position, nearby references contribute distance-based weights with a smoothly fading boundary. The target daily curve has the form `T = Tmin + solar_factor × (Tmax − Tmin)`. It is fitted to the game's approximate solar cycle and native weather states. Offline height compensation accounts for the engine's altitude effect within the limits of a shared sector profile.

This design gives neighbouring locations consistent weather regimes while preserving their regional differences. Native weather can change the active regime; it does **not** guarantee a unique temperature or a single persistent weather state per calendar day. Repeated rounded dashboard readings are possible.

## Scope and known limits

- **Fixed summer:** no live weather, PC-date seasons or automatic online updates.
- **Steep terrain:** coast and plateau can share a sector, so a single height compensation cannot perfectly match both. Residual cold or warm readings can occur in mountainous stretches.
- **Fallback:** 11 unresolved/legacy sectors retain the map's original climate. Future map changes require review and regeneration; runtime discovery of new cities is not included.
- **Weather appearance:** using native states can also affect the frequency of sky conditions.
- The mod supplies climate definitions and sector climate assignments, with **no replacement road geometry or custom environmental areas**.

Version **1.0.2** corrects description formatting and prepares the public release. Temperature and map data are unchanged from the tested 1.0.1 package. Road tests reported smooth transitions on the Santos–São Bernardo route; this is not a validation of every road or all weather combinations.

## Support and more realism

If this mod makes your journeys more immersive, [buy me a coffee](https://buymeacoffee.com/leonardoarouck). Your support helps keep the project moving.

Explore my other projects:

- [ETS2 Truck Dirt](https://github.com/Rhaiderr/ets2-truck-dirt) — dynamic truck dirt.
- [ETS2 Tire Wear](https://github.com/Rhaiderr/ets2-tire-wear) — tire wear for your journeys.

## Credits

Created by **Rhaiderr**. Climate data: [Open-Meteo Historical Weather API](https://open-meteo.com/en/docs/historical-weather-api), ERA5-Land / Copernicus Climate Change Service. Observed heat reference: [IAC/CIIAGRO February 2010 bulletin](https://www.ciiagro.sp.gov.br/Boletim_Agrome/Semanal_Fevereiro3_2010.pdf). Data attribution does not imply endorsement. Euro Truck Simulator 2 belongs to SCS Software; BR Brasil belongs to its respective author. This is an independent add-on, not an official SCS or BR Brasil release. Cover artwork is illustrative.

This repository hosts the public guide, images and downloadable releases. Development sources are maintained separately.

---

# Português (Brasil)

**Sinta o verão brasileiro em cada viagem.** Temperaturas regionais no painel para **Euro Truck Simulator 2 + BR Brasil**, com estados do tempo variáveis e transições graduais entre regiões.

[Baixar a versão mais recente](https://github.com/Rhaiderr/ets2-brbrasil-climate/releases/latest) · [Apoie o projeto](https://buymeacoffee.com/leonardoarouck)

Litoral, interior e serra merecem temperaturas diferentes. O Clima Real traz referências regionais de verão para o painel do caminhão: noites mais frescas, tardes quentes, períodos amenos e episódios de calor forte. A máxima não é um teto fixo diário, e a mesma viagem pode ter outra sensação conforme o tempo muda no jogo.

## O que o mod oferece

- **Cobertura regional do mapa BR Brasil suportado:** 1.019 setores recebem perfis calculados a partir de 42 localidades de referência.
- **Variação além do horário:** estados nativos incluem condições mais amenas e mais quentes, com calor extremo pouco frequente.
- **Transições mais suaves:** regiões próximas compartilham interpolação geográfica e estados térmicos coordenados, evitando sorteios independentes por cidade.
- **Um único mod:** sem plugin externo nem aplicativo rodando em segundo plano.

## Download e instalação

Versões de referência: **BR Brasil 6.1 / ETS2 1.62**. O mapa BR Brasil é necessário e não está incluído.

1. Faça backup do perfil e dos saves.
2. Baixe `brbrasil-clima-real-verao.scs` em [Releases](https://github.com/Rhaiderr/ets2-brbrasil-climate/releases/latest). O ZIP contém o mesmo mod e seu guia.
3. Copie o `.scs` para a pasta `mod` do ETS2.
4. Ative **BR Brasil - Clima Real** **acima de todos os pacotes do mapa BR Brasil** no Gerenciador de Mods, com prioridade maior.
5. Desative versões antigas. Use apenas uma cópia, manual ou da Oficina Steam.

Pode usar um perfil existente. Outros mods de clima podem sobrescrever as mesmas definições; **a compatibilidade com Weather_3.9 não foi validada**. Deixe-o desligado no primeiro teste. Atualizações do jogo e do mapa exigem nova revisão de compatibilidade.

## Como as temperaturas são calculadas

A base usa **dez verões de dezembro a fevereiro, de 2015/16 a 2024/25**, com **903 pares de mínima e máxima diárias por localidade**, provenientes da reanálise histórica ERA5-Land pelo Open-Meteo. São referências regionais, não leituras ao vivo nem recordes validados individualmente para todas as cidades.

Os dias são classificados pela máxima para criar regimes amenos, típicos e quentes, preservando mínimas noturnas associadas. Um evento observado de 40,3°C em Santos, registrado pelo IAC/CIIAGRO em fevereiro de 2010, serve de referência para uma cauda de calor rara; não é apresentado como recorde absoluto da cidade.

Cada posição suportada combina referências próximas por pesos de distância que diminuem suavemente até a borda. A curva diária segue `T = Tmin + fator_solar × (Tmax − Tmin)`, ajustada ao ciclo solar aproximado e aos estados nativos do jogo. Uma compensação de altura calculada na geração considera o efeito de altitude do motor, dentro dos limites de um perfil compartilhado por setor.

Regiões vizinhas mantêm um regime coerente e suas diferenças locais. O tempo nativo pode mudar o regime ativo; isso **não** garante temperatura exclusiva em cada visita nem um estado fixo por dia. O painel também pode repetir valores arredondados.

## Escopo e limitações

- **Verão fixo:** sem clima em tempo real, estação pela data do PC ou atualização online automática.
- **Serra:** litoral e planalto podem compartilhar um setor; uma compensação única não representa perfeitamente as duas alturas. Podem ocorrer leituras frias ou quentes residuais.
- **Fallback:** 11 setores antigos ou não resolvidos preservam o clima original. Mudanças futuras do mapa exigem revisão e nova geração; não há descoberta automática de cidades durante o jogo.
- **Céu:** o uso de estados nativos também pode influenciar a frequência das condições visuais.
- O pacote contém definições climáticas e atribuições por setor, **sem substituir geometria de estradas ou adicionar áreas ambientais especiais**.

A versão **1.0.2** corrige a formatação da descrição e prepara a publicação. Temperaturas e dados do mapa permanecem iguais aos da 1.0.1 testada. Os testes relatados no trecho Santos–São Bernardo tiveram transições suaves; isso não representa validação de todas as estradas ou combinações de tempo.

## Apoie e conheça os outros projetos

Gostou de trazer mais realismo às viagens? [Apoie pelo Buy Me a Coffee](https://buymeacoffee.com/leonardoarouck) e ajude o projeto a continuar.

- [ETS2 Truck Dirt](https://github.com/Rhaiderr/ets2-truck-dirt) — sujeira dinâmica no caminhão.
- [ETS2 Tire Wear](https://github.com/Rhaiderr/ets2-tire-wear) — desgaste de pneus nas viagens.

## Créditos

Criado por **Rhaiderr**. Dados: [Open-Meteo](https://open-meteo.com/en/docs/historical-weather-api), ERA5-Land / Copernicus Climate Change Service; referência observada de calor: [IAC/CIIAGRO](https://www.ciiagro.sp.gov.br/Boletim_Agrome/Semanal_Fevereiro3_2010.pdf). A atribuição dos dados não implica endosso. ETS2 pertence à SCS Software e BR Brasil ao respectivo autor. Complemento independente, sem vínculo oficial. A capa é ilustrativa.

Este repositório reúne guia público, imagens e versões para download. O desenvolvimento é mantido separadamente.
