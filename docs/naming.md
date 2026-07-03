# Sonatelle Naming

Sonatelle project names should feel like entries in a quiet catalogue of works. Prefer classical forms, musical genres, and performance terms over product-like labels.

Names should be restrained, pronounceable, and able to carry real engineering work without overstating it. A name may suggest a project's shape, scale, or temperament, but public claims should still come from implemented behavior.

## Usage Markers

Use Markdown task markers to track the catalogue:

- `[ ]` means the name is available.
- `[x]` means the name has been assigned to a concrete project.

Reserved names stay unchecked until they are actually assigned.

## Principles

- Prefer single-word names from musical forms, genres, or performance language.
- Use Title Case for display names and lowercase for repository names.
- Keep the highest-symbolic names for projects that can carry them.
- Avoid names that sound like generic tool suites, growth products, or inflated platforms.
- Prefer names with room for `core`, `cli`, `gui`, or other crates when a project naturally has multiple parts.
- Document assigned and reserved names so the catalogue stays coherent over time.

## Repository Form

Use lowercase repository names:

```text
partita
fugue
aria
nocturne
```

For multi-crate projects, prefer names that read naturally with crate suffixes:

```text
partita-core
partita-cli
partita-gui
```

## Current Assignments

- [x] **Partita** (`partita`) - Archive compression and extraction tool.
  A multi-part work fits a safety-first tool with core, CLI, GUI, and format-specific concerns.

## Reserved Names

- [ ] **Sonata**（奏鸣曲） - A formal multi-movement instrumental work with strong classical structure.
  Reserve for a flagship work with lasting symbolic weight.
- [ ] **Sonatina**（小奏鸣曲） - A smaller sonata, lighter but still formally shaped.
  Suitable for a compact counterpart to a larger formal project.
- [ ] **Symphony**（交响曲） - A large orchestral work with broad scale and multiple movements.
  Suitable for a major multi-system platform.
- [ ] **Concerto**（协奏曲） - A work built around dialogue between a soloist and ensemble.
  Suitable for host/plugin systems or projects centered on collaboration between parts.
- [ ] **Oratorio**（清唱剧） - A large narrative vocal work, usually unstaged.
  Suitable for documentation-heavy, narrative, or knowledge-system projects.

## Large Forms

- [ ] **Sonata**（奏鸣曲） - A formal, structured instrumental work, often in several movements.
  Suitable for a central flagship project with a clear architecture.
- [ ] **Symphony**（交响曲） - A large orchestral form with multiple movements and themes.
  Suitable for large systems with many cooperating subsystems.
- [ ] **Concerto**（协奏曲） - A dialogue between solo instrument and ensemble.
  Suitable for host/plugin frameworks, core/UI pairings, or human-in-the-loop tools.
- [ ] **Oratorio**（清唱剧） - A large narrative vocal work without staged drama.
  Suitable for knowledge systems, documentation systems, or long-form workflows.
- [ ] **Opera**（歌剧） - A staged musical drama with roles, scenes, and rich presentation.
  Suitable for GUI-heavy applications with many views and states.
- [ ] **Ballet**（芭蕾舞剧） - Music joined to movement and visual staging.
  Suitable for visual, animated, or interaction-heavy applications.
- [ ] **Mass**（弥撒曲） - A solemn musical setting of liturgical text.
  Suitable for serious security, audit, policy, or compliance tools.
- [ ] **Requiem**（安魂曲） - A memorial mass with grave and reflective character.
  Suitable for recovery, legacy cleanup, or archival projects.
- [ ] **Passion**（受难曲） - A large sacred narrative work.
  Suitable for serious history, traceability, or audit projects.
- [ ] **Sinfonia**（交响序曲） - A short symphonic work or overture-like opening.
  Suitable for system entry points, launchers, or foundational layers.

## Multi-Part Works

- [x] **Partita**（组曲；变奏组曲） - A multi-part instrumental work, often made from related dances or movements.
  Suitable for archive tools, multi-crate systems, or projects with core/CLI/GUI.
- [ ] **Suite**（组曲） - A set of related movements or pieces.
  Suitable for tool collections or cohesive utility sets.
- [ ] **Cantata**（康塔塔） - A medium-scale vocal and instrumental work in several sections.
  Suitable for medium applications with several modes or views.
- [ ] **Divertimento**（嬉游曲） - A light multi-movement work for entertainment.
  Suitable for experiment collections or lighter applications.
- [ ] **Serenade**（小夜曲） - A gentle work associated with evening performance.
  Suitable for friendly UI, notifications, companion tools.
- [ ] **Cassation**（晚间嬉游曲） - A light multi-movement work related to serenades and divertimenti.
  Suitable for small desktop suites or experimental collections.
- [ ] **Concertino**（小协奏曲） - A smaller concerto.
  Suitable for small host/plugin tools.
- [ ] **Sinfonietta**（小交响曲） - A smaller symphonic work.
  Suitable for medium platforms or compact system frameworks.

## Structural Forms

- [ ] **Fugue**（赋格曲） - A contrapuntal form where voices enter and interweave around a subject.
  Suitable for proxy tools, concurrency systems, routing engines, orchestration.
- [ ] **Canon**（卡农） - A rule-based imitation between voices.
  Suitable for synchronization, mirroring, validation, strict safety rules.
- [ ] **Rondo**（回旋曲） - A recurring main theme alternates with contrasting episodes.
  Suitable for cyclic workflows, schedulers, repeated task runners.
- [ ] **Theme and Variations**（主题与变奏） - One theme developed through repeated variations.
  Suitable for template systems, configuration variants, format transformations.
- [ ] **Passacaglia**（帕萨卡利亚） - Variations over a repeated bass or harmonic pattern.
  Suitable for stable engines, long-running services, foundational systems.
- [ ] **Chaconne**（夏空） - A variation form built on repeated harmonic ground.
  Suitable for strategy systems, format abstraction, policy variation.
- [ ] **Ricercar**（利切卡尔） - An exploratory contrapuntal form, historically related to the fugue.
  Suitable for search, parsing, exploration of complex structures.
- [ ] **Invention**（创意曲） - A compact contrapuntal work built around a clear idea.
  Suitable for small algorithm libraries or technical experiments.
- [ ] **Counterpoint**（对位法） - Independent melodic lines combined coherently.
  Suitable for multi-agent, multi-process, or coordination tools.
- [ ] **Polyphony**（复调） - Multiple independent voices sounding together.
  Suitable for multi-session, multi-stream, or multi-window applications.

## Short Works

- [ ] **Prelude**（前奏曲） - An opening piece or independent short work.
  Suitable for scaffolds, initializers, launch helpers.
- [ ] **Intermezzo**（间奏曲） - A short piece placed between larger sections or acts.
  Suitable for bridges, adapters, format conversion, or middle-layer tools.
- [ ] **Cadenza**（华彩段） - A free solo passage that shows technique within a larger work.
  Suitable for plugins, extension systems, or format backends.
- [ ] **Etude**（练习曲） - A study written to develop a technique.
  Suitable for learning projects, benchmarks, algorithm experiments.
- [ ] **Bagatelle**（小品） - A short, light, polished piece.
  Suitable for small single-purpose tools or crates.
- [ ] **Impromptu**（即兴曲） - A short work with an improvised character.
  Suitable for quick prototypes, scratch tools, temporary helpers.
- [ ] **Caprice**（随想曲） - A free and often playful work.
  Suitable for creative experiments or flexible tools.
- [ ] **Capriccio**（随想曲） - A free-form, spirited piece.
  Suitable for configurable tools, demos, or expressive experiments.
- [ ] **Moment Musical**（音乐瞬间） - A short piece that captures a mood or moment.
  Suitable for clips, excerpts, note fragments, quick capture tools.
- [ ] **Albumblatt**（纪念册页） - A short piece often written as a personal dedication or keepsake.
  Suitable for personal archives, saved fragments, small memory tools.
- [ ] **Miniature**（小品；微型作品） - A small but complete work.
  Suitable for micro-components, demos, previews.
- [ ] **Sketch**（草稿曲；素描） - A musical idea or draft rather than a full formal work.
  Suitable for prototypes and concept repositories.
- [ ] **Arietta**（小咏叹调） - A small aria.
  Suitable for compact UI components or single-expression tools.
- [ ] **Aria**（咏叹调） - A lyrical solo vocal piece, often clear and expressive.
  Suitable for UI frameworks, expression layers, and focused interface libraries.

## Night, Time, And Lyric Forms

- [ ] **Nocturne**（夜曲） - A lyric piece with night-like, inward character.
  Suitable for native terminals, dark tools, quiet long-running applications.
- [ ] **Notturno**（夜曲） - An Italian form of nocturne.
  Suitable as a more classical alternative to Nocturne.
- [ ] **Aubade**（晨歌） - A dawn song, often tied to morning or parting.
  Suitable for morning planning, startup tools, recovery workflows.
- [ ] **Vesper**（晚祷；黄昏音乐） - Evening prayer or dusk-associated music.
  Suitable for end-of-day review, log closure, backup wrap-up.
- [ ] **Berceuse**（摇篮曲） - A lullaby-like piece.
  Suitable for sleep, calm reminders, low-frequency tools.
- [ ] **Barcarolle**（船歌） - A lyric piece suggesting the motion of a boat.
  Suitable for sync, migration, stream movement, transfer tools.
- [ ] **Pastorale**（田园曲） - Music evoking rural calm or natural simplicity.
  Suitable for simple local tools and low-complexity applications.
- [ ] **Romance**（浪漫曲） - A lyric and melodic short work.
  Suitable for writing, personal content, collections.
- [ ] **Elegy**（挽歌） - A reflective work of mourning or remembrance.
  Suitable for legacy cleanup, historical records, memorial archives.
- [ ] **Lullaby**（摇篮曲） - A song for sleep and comfort.
  Suitable for gentle companion tools.

## Dance Forms

- [ ] **Minuet**（小步舞曲） - An elegant triple-meter court dance.
  Suitable for polished small tools and refined UI.
- [ ] **Gavotte**（加沃特舞曲） - A clear and lightly stepping French dance.
  Suitable for lightweight desktop tools.
- [ ] **Sarabande**（萨拉班德舞曲） - A slow, grave dance with weight.
  Suitable for archiving, reading, organizing, and preservation tools.
- [ ] **Gigue**（吉格舞曲） - A fast dance often closing a suite.
  Suitable for fast CLI tools and batch processing.
- [ ] **Allemande**（阿勒曼德舞曲） - A steady dance often opening a Baroque suite.
  Suitable for foundational libraries and orderly tools.
- [ ] **Courante**（库朗特舞曲） - A flowing dance form.
  Suitable for sync, transfer, stream, and movement-oriented tools.
- [ ] **Bourree**（布列舞曲） - A lively dance with clear rhythm.
  Suitable for small practical utilities.
- [ ] **Pavane**（帕凡舞曲） - A slow, stately court dance.
  Suitable for readers, galleries, static presentation tools.
- [ ] **Tarantella**（塔兰泰拉舞曲） - A fast, energetic dance.
  Suitable for high-speed processing or dense interaction tools.
- [ ] **Waltz**（圆舞曲） - A flowing triple-meter dance with rotational feeling.
  Suitable for smooth UI, browsing, animation, visual navigation.

## Tempo And Character Terms

These are not usually standalone composition forms, but they still make good names when a project's temperament matters.

- [ ] **Adagio**（柔板） - Slow and spacious.
  Suitable for stable backups, checks, and long-running work.
- [ ] **Andante**（行板） - Walking pace.
  Suitable for everyday productivity tools.
- [ ] **Allegro**（快板） - Fast and bright.
  Suitable for search, conversion, quick CLI tools.
- [ ] **Vivace**（活泼地） - Lively.
  Suitable for responsive interfaces.
- [ ] **Presto**（急板） - Very fast.
  Suitable for performance tools and batch processors.
- [ ] **Largo**（广板） - Broad and slow.
  Suitable for large-file or long-duration workflows.
- [ ] **Lento**（慢板） - Slow.
  Suitable for low-frequency monitoring and patient background work.
- [ ] **Grave**（庄板） - Serious and weighty.
  Suitable for recovery, audit, and security tools.
- [ ] **Sostenuto**（保持音） - Sustained.
  Suitable for sessions, persistence, state management.
- [ ] **Rubato**（弹性速度） - Flexible timing.
  Suitable for dynamic scheduling and adaptive layouts.

## Touch And Expression Terms

- [ ] **Toccata**（触技曲） - A keyboard work emphasizing touch and agility.
  Suitable for terminals, command palettes, keyboard-first tools.
- [ ] **Legato**（连奏） - Smoothly connected.
  Suitable for animation, migration, streaming, transitions.
- [ ] **Staccato**（断奏） - Short and separated.
  Suitable for small task runners and event slicing.
- [ ] **Marcato**（强调地） - Clearly accented.
  Suitable for CLI feedback and command emphasis.
- [ ] **Cantabile**（如歌地） - In a singing style.
  Suitable for UI frameworks, writing tools, text experiences.
- [ ] **Dolce**（柔和地） - Soft and sweet.
  Suitable for gentle interfaces and low-intrusion tools.
- [ ] **Espressivo**（富有表情地） - Expressive.
  Suitable for creative tools and rich text editors.
- [ ] **Semplice**（简洁地） - Simple and plain.
  Suitable for minimal libraries and configuration tools.
- [ ] **Maestoso**（庄严地） - Majestic.
  Suitable for main consoles and large control surfaces.
- [ ] **Serioso**（严肃地） - Serious.
  Suitable for validators, safety tools, and audit utilities.

## High-Value Name Pool

Keep these names visible when planning new projects:

- [ ] **Sonata**
- [x] **Partita**
- [ ] **Nocturne**
- [ ] **Fugue**
- [ ] **Aria**
- [ ] **Prelude**
- [ ] **Canon**
- [ ] **Rondo**
- [ ] **Toccata**
- [ ] **Cantata**
- [ ] **Oratorio**
- [ ] **Intermezzo**
- [ ] **Cadenza**
- [ ] **Vesper**
- [ ] **Aubade**
- [ ] **Passacaglia**
- [ ] **Chaconne**
- [ ] **Sinfonia**
- [ ] **Concerto**
- [ ] **Etude**
