---
title: 'Language Science at the Crossroads of AI, Cognition, and Society'
date: 2024-10-31
permalink: /posts/2024/10/nlp-mila-workshop/
tags:
  - NLP
  - cognitive science
  - AI safety
  - workshop
excerpt: "Notes from Mila's three-day transatlantic workshop on NLP in the Era of Generative AI, Cognitive Sciences, and Societal Transformation."
---

From October 1 to 3, 2024, [Mila](https://mila.quebec/en) hosted a three-day workshop bringing together researchers from Canada and France working on natural language processing. The workshop, organized as part of the [International Laboratory on Learning Systems](https://ottawa.office.cnrs.fr/en/research/international-laboratory-on-learning-systems-2/), was structured around three themes: the technical foundations of language models, their connections to the cognitive and brain sciences, and their broader applications and social impacts. The program addressed how current large language models operate, how they compare to human language use, and what is required to deploy them in sensitive domains.

<details style="margin: 1rem 0; border: 1px solid #e1e4e8; border-radius: 8px; padding: 0.75rem 1rem; background: #f6f8fa; font-size: 0.85rem;">
  <summary style="cursor: pointer; font-weight: 600; padding: 0.15rem 0;">Day 1 · Technical foundations</summary>
  <ol style="padding-left: 1.25rem; margin: 0.75rem 0 0.25rem 0; line-height: 1.5;">
    <li>Yoshua Bengio, Université de Montréal &amp; Mila, Risks of capable AI</li>
    <li>Danilo Bzdok, McGill University &amp; Mila, IVADO and the Canadian AI ecosystem</li>
    <li>Claire Gardent, CNRS &amp; LORIA, Data-to-text across languages</li>
    <li>Philippe Langlais, Université de Montréal &amp; RALI, Rethinking evaluation</li>
    <li>Golnoosh Farnadi, McGill University &amp; Mila, Fairness in foundation models</li>
    <li>François Yvon, CNRS &amp; ISIR, Translation memories</li>
    <li>David Adelani, McGill University &amp; Mila, LLMs for African languages</li>
    <li>Siva Reddy, McGill University &amp; Mila, Inductive biases for LLMs</li>
    <li>Benoît Sagot, INRIA Almanach Paris, Why small LMs struggle</li>
    <li>Lili Mou, University of Alberta &amp; Amii, LLMs as reward signals</li>
  </ol>
</details>

<details style="margin: 1rem 0; border: 1px solid #e1e4e8; border-radius: 8px; padding: 0.75rem 1rem; background: #f6f8fa; font-size: 0.85rem;">
  <summary style="cursor: pointer; font-weight: 600; padding: 0.15rem 0;">Day 2 · Cognition &amp; brains</summary>
  <ol style="padding-left: 1.25rem; margin: 0.75rem 0 0.25rem 0; line-height: 1.5;">
    <li>Yang Xu, University of Toronto, Why languages look the way they do</li>
    <li>Abdellah Fourtassi, Aix-Marseille Université, How children learn language</li>
    <li>Guillaume Dumas, Université de Montréal &amp; Mila, Brains vs. language models</li>
    <li>Benjamin Morillon, Aix-Marseille Université &amp; INSERM, What LMs reveal about the brain</li>
    <li>Maxime Peyrard, CNRS Grenoble, and Dhanya Sridhar, Université de Montréal &amp; Mila, Causal models for NLP</li>
    <li>Panel discussion</li>
  </ol>
</details>

<details style="margin: 1rem 0; border: 1px solid #e1e4e8; border-radius: 8px; padding: 0.75rem 1rem; background: #f6f8fa; font-size: 0.85rem;">
  <summary style="cursor: pointer; font-weight: 600; padding: 0.15rem 0;">Day 3 · Society &amp; applications</summary>
  <ol style="padding-left: 1.25rem; margin: 0.75rem 0 0.25rem 0; line-height: 1.5;">
    <li>Dilek Hakkani-Tür, University of Illinois Urbana-Champaign, Friction in dialogue systems</li>
    <li>Mirco Ravanelli, Concordia University &amp; Mila, Audio for multimodal LLMs</li>
    <li>Roland Memisevic, Qualcomm AI Research Toronto, Situated interaction</li>
    <li>Serena Villata, CNRS i3s, and Jimmy Lin, University of Waterloo, Argumentation and retrieval</li>
    <li>Saif Mohammad, National Research Council Canada, NLP for affective science</li>
    <li>Frank Rudzicz, Dalhousie University, Language tech in healthcare</li>
    <li>Géraldine Damnati, Orange Innovation, Real-world evaluation</li>
  </ol>
</details>

## Day 1

Day 1 focused on the technical foundations of language models and on how current systems handle the diversity of the world's languages and users.

<div id="day1-video" style="position: relative; max-width: 720px; cursor: pointer; margin-bottom: 2rem;" onclick="loadDay1Video()">
  <img src="/images/mila_workshop_day1.png" alt="Watch Day 1 session" style="width: 100%; display: block; border-radius: 8px;">
  <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: rgba(255,0,0,0.9); width: 68px; height: 48px; border-radius: 12px; display: flex; align-items: center; justify-content: center; z-index: 2;">
    <div style="width: 0; height: 0; border-left: 18px solid white; border-top: 12px solid transparent; border-bottom: 12px solid transparent; margin-left: 4px;"></div>
  </div>
</div>
<script type="text/javascript">
function loadDay1Video() {
  var container = document.getElementById('day1-video');
  container.style.paddingBottom = '56.25%';
  container.style.height = '0';
  container.innerHTML = '<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-radius: 8px;" src="https://www.youtube.com/embed/J2wHTW6YMjI?start=7&autoplay=1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>';
  container.style.cursor = 'default';
}
</script>

### Yoshua Bengio (Université de Montréal, Mila): On the Risks of Increasingly Capable AI

[Yoshua Bengio](https://yoshuabengio.org/en), the founder of Mila, opened the workshop with a talk on the risks associated with increasingly capable AI systems. He noted that progress toward general-purpose AI is [advancing faster than many had anticipated](https://metr.org/time-horizons/), and that the field has not yet developed reliable methods to ensure such systems behave in line with human values. He reviewed possible failure modes, including systems that pursue goals in unintended ways and systems that could be deliberately misused, and argued that AI safety should be treated as a core research priority.

### Danilo Bzdok (McGill University, Mila): IVADO and the Canadian AI Ecosystem

[Danilo Bzdok](https://bzdok.lab.mcgill.ca/), IVADO's Scientific Co-Director of Research Programs and Academic Relations, provided an overview of [IVADO](https://ivado.ca/) and its [R³AI vision](https://ivado.ca/en/the-r3ai-vision-toward-a-robust-reasoning-and-responsible-ai/) of advancing robust, reasoning, and responsible AI. The Quebec-based institute supports AI research and training through a transdisciplinary approach that brings together researchers across disciplines and institutions to work on questions where AI intersects with science and different sectors of society.

### Claire Gardent (CNRS, LORIA): Turning Data into Text Across Many Languages

The first session, chaired by Pablo Piantanida, focused on core NLP. [Claire Gardent](https://members.loria.fr/CGardent/) presented work on verbalizing knowledge graphs and abstract meaning representations into twenty-one European languages. She described how encoder-decoder architectures enriched with structural embeddings for sibling and branch information, trained on the Europarl corpus, outperformed both monolingual baselines and hybrid machine-translation pipelines, particularly for low-resource European languages.

### Philippe Langlais (Université de Montréal, RALI): Rethinking How We Measure Progress

[Philippe Langlais](http://rali.iro.umontreal.ca/rali/?q=en/felipe) followed with a talk on evaluation, arguing that benchmarks themselves often contain significant problems. He presented work on the open information extraction task, showing that different popular benchmarks lead to opposite conclusions about which systems perform best. He then demonstrated that a re-annotated benchmark, combined with downstream task evaluation, produces a different picture, and concluded with a recommendation to examine benchmarks closely rather than rely on them at face value.

### Golnoosh Farnadi (McGill University, Mila): Fairness in Foundation Models

[Golnoosh Farnadi](https://gfarnadi.github.io/) closed the session with an overview of algorithmic fairness. She traced the field from its emergence around 2014 through the era of foundation models, arguing that marginalized communities can be characterized, from a machine-learning perspective, as those at the tails of training distributions, with low-resource languages as one example. She noted that the scale of foundation models amplifies existing fairness challenges, since notions of fairness are inherently contextual while these general-purpose models are deployed across many contexts simultaneously.

### François Yvon (CNRS, ISIR): Translation That Remembers

The afternoon opened with a session on multilinguality. [François Yvon](https://fyvo.github.io/) revisited example-based machine translation, showing how translation memories and retrieval augmentation can be combined with neural encoder-decoder and non-autoregressive architectures to handle repetitive, domain-specific translation tasks common in professional translation work.

### David Adelani (McGill University, Mila): Making Language Models Work for African Languages

[David Adelani](https://dadelani.github.io/) continued with an assessment of how large language models perform on under-resourced languages. He noted that of the world's roughly seven thousand languages, approximately fifty are well-supported by LLMs, and that among African languages only Afrikaans and Swahili approach the data scale typically considered sufficient. He argued that the pretrain-then-finetune paradigm remains effective for these settings and should not be abandoned in favor of prompting-based approaches.

### Siva Reddy (McGill University, Mila): Do Language Models Still Need Our Help?

The third session turned to architectural and methodological questions. [Siva Reddy](https://sivareddy.in/) examined whether LLMs still require human-designed inductive biases, reviewing cases such as negation and scope ambiguity where next-word-prediction objectives fall short, and showing how targeted unlikelihood training combined with distillation can address these limitations in models such as BERT.

### Benoît Sagot (INRIA Almanach, Paris): Why Small Language Models Struggle

[Benoît Sagot](http://alpage.inria.fr/~sagot/) presented joint work with his PhD student Nathan Godey on why small language models underperform. He described a "saturation" effect visible in Pythia checkpoints, in which smaller models' training loss plateaus and eventually worsens, and linked this behavior to representational anisotropy and the softmax bottleneck. He noted the relevance of these findings for training inference-efficient models under current scaling laws.

### Lili Mou (University of Alberta, Amii): Language Models as Hidden Reward Signals

[Lili Mou](https://lili-mou.github.io/) closed the day with work on using LLMs as implicit reward functions. She outlined theoretical connections between inverse reinforcement learning and pretrained language models, and described how the resulting reward signals can be applied to semi-supervised learning and knowledge distillation.

## Day 2

Day 2 shifted focus from language technology itself to its connections with the cognitive sciences and neuroscience.

<div id="day2-video" style="position: relative; max-width: 720px; cursor: pointer; margin-bottom: 2rem;" onclick="loadDay2Video()">
  <img src="/images/mila_workshop_day2.png" alt="Watch Day 2 session" style="width: 100%; display: block; border-radius: 8px;">
  <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: rgba(255,0,0,0.9); width: 68px; height: 48px; border-radius: 12px; display: flex; align-items: center; justify-content: center; z-index: 2;">
    <div style="width: 0; height: 0; border-left: 18px solid white; border-top: 12px solid transparent; border-bottom: 12px solid transparent; margin-left: 4px;"></div>
  </div>
</div>
<script type="text/javascript">
function loadDay2Video() {
  var container = document.getElementById('day2-video');
  container.style.paddingBottom = '56.25%';
  container.style.height = '0';
  container.innerHTML = '<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-radius: 8px;" src="https://www.youtube.com/embed/MHyL6eXjn0c?autoplay=1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>';
  container.style.cursor = 'default';
}
</script>

### Yang Xu (University of Toronto): Why Languages Look the Way They Do

[Yang Xu](https://www.cs.toronto.edu/~yangxu/) opened by noting that the objective function of language models, from Shannon's n-grams to GPT, has remained largely unchanged for seventy years, while natural language has evolved under different pressures. He proposed three factors shaping lexical evolution: communication, with the lexicon functioning as an information-theoretic compressor that maps a large space of ideas through a finite symbolic bottleneck; cognition, in which the mind extends its vocabulary in response to a changing world; and culture, which shapes which new words persist. He discussed points of contact between each factor and current computational models.

### Abdellah Fourtassi (Aix-Marseille Université): Using AI to Study How Children Learn Language

[Abdellah Fourtassi](https://afourtassi.github.io/) continued with a discussion of the relationship between developmental science and NLP. He noted that early NLP drew on child-learning intuitions, with Jeff Elman's simple recurrent networks as one example, and argued that the two fields have since diverged. He suggested that NLP tools now offer scalability relevant to developmental psychology, and presented results from "BabyBERTa," a model trained on five million words of child-directed speech that achieves syntactic performance comparable to larger models such as RoBERTa. He noted that this finding suggests children's linguistic input may be richer than classic poverty-of-the-stimulus arguments indicated.

### Guillaume Dumas (Université de Montréal, Mila): The Gap Between Brains and Language Models

[Guillaume Dumas](https://www.extrospection.eu/) cautioned against what he termed the "map–territory fallacy" of conflating LLMs with human cognition. He presented his lab's research on interbrain synchronization, the coupled neural dynamics of two people in conversation measured through hyperscanning, and argued that much of human language is fundamentally interactive. He noted that similarities in representations across model layers and brain regions do not necessarily imply similar underlying processes.

### Benjamin Morillon (Aix-Marseille Université, INSERM): What Language Models Reveal About the Brain

[Benjamin Morillon](https://ins-amu.fr/benjaminmorillon) presented intracranial recordings of patients listening to speech and music. He discussed how the predictive-coding framework unifies auditory processing across domains, and how large language models can serve as regressors for localizing where and when the brain generates expectations about upcoming words. He emphasized that correlations between layer activations and brain signals are a starting point for investigation rather than a conclusion about shared mechanisms.

### Maxime Peyrard (CNRS, Grenoble): Can We Really Explain What a Neural Network Is Doing? and Dhanya Sridhar (Université de Montréal, Mila): What Language Models Are Actually Learning From Examples

The afternoon session on causal models for NLP paired [Maxime Peyrard](https://peyrardm.github.io/) with [Dhanya Sridhar](https://www.dsridhar.com/). Peyrard surveyed interpretability, outlining where current mechanistic interpretability converges with and diverges from earlier traditions of neural-network analysis. Sridhar examined whether in-context learning could be made more robust and sample-efficient by introducing causal inductive biases into how examples are selected and how models infer regularities, a question with practical implications for prompting reliability.

### Panel Discussion

The day closed with a panel moderated by Jackie Chi Kit Cheung and Frédéric Béchet, with Frank Rudzicz, Yang Xu, Claire Gardent, Serena Villata, Benjamin Morillon, Guillaume Dumas, and Aaron Courville. The discussion addressed whether AI and neuroscience can inform each other, concerns about benchmark culture and reproducibility in NLP research, the risks of deploying language technology in healthcare, the challenges of systems in which multiple AI agents interact, and the effectiveness of current safety measures.

## Day 3

Day 3 addressed the societal and applied dimensions of NLP, opening with a welcome address from [Adeline Nazarenko](https://www.cnrs.fr/en/person/adeline-nazarenko), director of the CNRS Institute for Information Sciences and Technology.

<div id="day3-video" style="position: relative; max-width: 720px; cursor: pointer; margin-bottom: 2rem;" onclick="loadDay3Video()">
  <img src="/images/mila_workshop_day3.png" alt="Watch Day 3 session" style="width: 100%; display: block; border-radius: 8px;">
  <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); background: rgba(255,0,0,0.9); width: 68px; height: 48px; border-radius: 12px; display: flex; align-items: center; justify-content: center; z-index: 2;">
    <div style="width: 0; height: 0; border-left: 18px solid white; border-top: 12px solid transparent; border-bottom: 12px solid transparent; margin-left: 4px;"></div>
  </div>
</div>
<script type="text/javascript">
function loadDay3Video() {
  var container = document.getElementById('day3-video');
  container.style.paddingBottom = '56.25%';
  container.style.height = '0';
  container.innerHTML = '<iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border-radius: 8px;" src="https://www.youtube.com/embed/vOfSst9pzDQ?autoplay=1&start=27" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>';
  container.style.cursor = 'default';
}
</script>

### Dilek Hakkani-Tür (University of Illinois Urbana-Champaign): Why a Little Friction Is a Good Thing

The conversational AI session opened with [Dilek Hakkani-Tür](https://dilek.web.illinois.edu/) on over-reliance. She described how users tend to accept the outputs of fluent systems uncritically, contributing to an accountability gap, and argued that dialogue systems should include built-in uncertainty expression and explicit deferral mechanisms.

### Mirco Ravanelli (Concordia University, Mila): Teaching Language Models to Handle Audio

[Mirco Ravanelli](https://sites.google.com/site/mircoravanelli/) presented work on discrete audio tokens for multimodal LLMs, which allow models to process speech and audio in a manner comparable to text.

### Roland Memisevic (Qualcomm AI Research, Toronto): Building AI That Watches and Talks Back in Real Time

[Roland Memisevic](https://www-labs.iro.umontreal.ca/~memisevr/) closed the session with work on end-to-end learning for camera-based situated interaction, and discussed the role of embodied understanding in the next generation of AI assistants.

### Serena Villata (CNRS i3s): Teaching Computers to Recognize Arguments and Jimmy Lin (University of Waterloo): Search as an Aid to Thinking

The information retrieval and argumentation session followed, with [Serena Villata](https://webusers.i3s.unice.fr/~villata/Home.html) on trustworthy natural-language argumentation, a field she noted is becoming increasingly important as LLMs generate growing volumes of persuasive text online. [Jimmy Lin](https://cs.uwaterloo.ca/~jimmylin/) then addressed the future of information retrieval in an LLM-mediated environment, focusing on the evolving question of how retrieval systems should be evaluated.

### Saif Mohammad (National Research Council Canada): What Language Can Tell Us About Emotions

[Saif Mohammad](https://www.saifmohammad.com/) spoke on NLP for affective science, examining which questions about emotion, sentiment, and subjective experience can be productively investigated with current tools.

### Frank Rudzicz (Dalhousie University): Language Technology in Healthcare

[Frank Rudzicz](https://www.dal.ca/faculty/computerscience/faculty-staff/Frank-Rudzicz.html) presented a talk entitled "NLPrimum Non Nocere," a reference to the principle of "first, do no harm," which addressed the risks of deploying language technology in medical and clinical contexts where errors carry significant consequences.

### Géraldine Damnati (Orange Innovation): Evaluation in the Real World

[Géraldine Damnati](https://sites.google.com/site/geraldinedamnati/) closed the workshop with a discussion of the need to move from benchmark assessments to in-use evaluation. She argued that the gap between model performance on curated test sets and model behavior in real deployments has grown in the generative-AI era.

### Closing reflections

Across three days, the workshop addressed generative NLP, its relationship with human cognition and neuroscience, and its deployment in society. Several themes recurred across sessions. Speakers raised concerns about the reliability of current benchmarks and evaluation practices. Several talks addressed how scale amplifies disparities along linguistic and cultural lines. Presenters working at the intersection of cognitive science and AI cautioned that similar outputs between models and humans do not necessarily indicate similar underlying mechanisms. And speakers on applied topics emphasized the need for improved evaluation, accountability, and deployment practices.

A recurring point across the program was that progress in NLP depends on sustained contact with neighboring disciplines, including linguistics, psychology, neuroscience, philosophy, and public policy, alongside continued work on model capabilities.
