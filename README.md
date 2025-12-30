# Flintstones Dataset

This repository provides the **Flintstones dataset**, a multimedia benchmark
for long-form story illustration and vision–language generation.

The dataset is self-curated to support the evaluation of **consistency-aware,
multi-frame image generation systems**, with a particular focus on character
identity preservation, visual coherence, and prompt-based controllability.

---

## Dataset Overview

The **Flintstones dataset** is inspired by the classic animated series
*The Flintstones*, which features recurring characters and visually distinctive
settings suitable for studying long-horizon visual consistency.

The dataset contains **166 stories**, each provided as a single, self-contained
`JSON` file. Each story represents a complete narrative episode segmented into
multiple frames for story illustration.

---

## Directory Structure



```
.
├── stories/
│   ├── season 1_episode_1.json
│   └── ... (166 story files in total)
├── LICENSE
└── README.md
```

## Data Format

Each `JSON` file in the `stories/` directory represents a single story and
contains the following fields:

- **`full_story`** *(String)*  
  A complete natural-language narrative describing the episode.

- **`global_characters_dict`** *(Object)*  
  A structured character registry containing canonical descriptions of the
  main characters appearing in the story. This registry provides reference
  information for maintaining character identity consistency across frames.

- **`global_objects_dict`** *(Object)*  
  A placeholder for global object descriptions (currently empty).

- **`captions_info`** *(Array)*  
  A sequence of frame-level annotations, where each entry corresponds to one
  illustrated frame. Each entry includes:
  
  - **`page_id`** *(Integer)*: Sequential frame index, starting from 1.  
  - **`caption`** *(String)*: A short description summarizing the events in
    the frame.  
  - **`char_all_list`** *(Array of Strings)*: Characters appearing in the frame.  
  - **`description`** *(String)*: A detailed **Executable Description** that
    integrates the frame caption with character attributes and inferred visual
    cues. This description is designed to serve as input to text-to-image
    generation models.

The dataset contains only text-based narratives and structured annotations.
No images are included.

---

## Data Sources and Provenance

The **Flintstones dataset** was constructed by deriving structured story
descriptions from publicly available episode summaries of *The Flintstones*.

Original episode summaries were obtained from **Wikipedia**, which is licensed
under **CC BY-SA 4.0**. No text was copied verbatim. All narratives were
rewritten and expanded to form new derived descriptions and annotations
suitable for story illustration research.

- **Reference source:**  
  *List of The Flintstones episodes* – Wikipedia  
  https://en.m.wikipedia.org/wiki/List_of_The_Flintstones_episodes

All derived content is released under **CC BY 4.0** for research and educational
purposes. *The Flintstones* and its characters remain the property of their
respective rights holders.

---

## Citation

Citation information will be provided upon paper acceptance.

---

## License

The **Flintstones dataset** is licensed under the
**Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

