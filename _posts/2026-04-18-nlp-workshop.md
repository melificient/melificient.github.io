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

From October 1 to 3, 2024, [Mila](https://mila.quebec/en) hosted a three-day workshop bringing together researchers from across Canada and France working on natural language processing. The workshop, organized as part of the [International Laboratory on Learning Systems](https://ottawa.office.cnrs.fr/en/research/international-laboratory-on-learning-systems-2/), was structured around three themes: the technical foundations of language models, their connections to the cognitive and brain sciences, and their broader applications and social impacts. Recurring questions throughout the three days included how today's large language models actually work, how they compare to human language use, and what it takes to deploy them responsibly in sensitive domains.

## Day 1

Day 1 focused on the technical foundations of language models and on how well current systems handle the full diversity of the world's languages and users.

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

[Yoshua Bengio](https://yoshuabengio.org/en), the founder of Mila, opened the workshop with a talk on the risks that come with AI systems as they grow more capable. He argued that progress toward general-purpose AI is [happening faster than many expected](https://metr.org/time-horizons/), and that the field has not yet developed reliable ways to ensure such systems behave in line with human values. He discussed possible failure modes, from systems that pursue goals in unintended ways to systems that could be deliberately misused, and made the case for treating AI safety as a core research priority rather than an afterthought.

### Danilo Bzdok (McGill University, Mila): IVADO and the Canadian AI Ecosystem

[Danilo Bzdok](https://bzdok.lab.mcgill.ca/), IVADO's Scientific Co-Director of Research Programs and Academic Relations, gave a short overview of [IVADO](https://ivado.ca/) and its commitment to addressing these challenges through its [R³AI vision](https://ivado.ca/en/the-r3ai-vision-toward-a-robust-reasoning-and-responsible-ai/) of advancing robust, reasoning, and responsible AI. The Quebec-based institute supports AI research and training through a transdisciplinary approach that brings together researchers across disciplines and institutions to work on questions where AI intersects with science and different sectors of society.

### Claire Gardent (CNRS, LORIA): Turning Data into Text Across Many Languages

The first session, chaired by Pablo Piantanida, focused on core NLP. **[Claire Gardent](https://members.loria.fr/CGardent/)** presented work on verbalizing knowledge graphs and abstract meaning representations into twenty-one European languages. She showed how encoder-decoder architectures enriched with structural embeddings for sibling and branch information, trained on the Europarl corpus, could outperform both monolingual baselines and hybrid machine-translation pipelines, particularly for low-resource European languages. 

### Philippe Langlais (Université de Montréal, RALI): Rethinking How We Measure Progress

[Philippe Langlais](http://rali.iro.umontreal.ca/rali/?q=en/felipe) followed with a characteristically skeptical talk on evaluation, arguing that benchmarks themselves often contain deep problems. He presented work on the open information extraction task, showing that different popular benchmarks lead to opposite conclusions about which systems are best, and demonstrated that a carefully re-annotated benchmark, combined with downstream task evaluation, gives a very different picture. His mantra: don't trust your benchmarks; look inside them.

### Golnoosh Farnadi (McGill University, Mila): Fairness in Foundation Models

[Golnoosh Farnadi](https://gfarnadi.github.io/) rounded out the session with an overview of algorithmic fairness. She traced the field from its emergence around 2014 through the era of foundation models, arguing that marginalized communities can be redefined, from a machine-learning perspective, as those at the tails of training distributions (low-resource languages being the canonical example). The scale of foundation models amplifies old fairness challenges: notions of fairness are inherently contextual, yet these general-purpose models are deployed everywhere at once.

### François Yvon (CNRS, ISIR): Translation That Remembers

The afternoon opened with multilinguality. [François Yvon](https://fyvo.github.io/) revisited example-based machine translation through a modern lens, showing how translation memories and retrieval augmentation can be combined with neural encoder-decoder and non-autoregressive architectures to handle the repetitive, domain-specific translation tasks that fill professional translators' days. 

### David Adelani (McGill University, Mila): Making Language Models Work for African Languages

[David Adelani](https://dadelani.github.io/) continued with a clear-eyed assessment of how poorly large language models serve under-resourced languages. Of the world's seven thousand languages, perhaps fifty are well-supported by LLMs; for African languages, only Afrikaans and Swahili approach the data scale typically considered sufficient. He argued that the old pretrain-then-finetune paradigm remains remarkably effective for these settings and should not be abandoned in the rush toward prompting.

### Siva Reddy (McGill University, Mila): Do Language Models Still Need Our Help?

The third session turned to architectural and methodological questions. [Siva Reddy](https://sivareddy.in/) asked whether LLMs still need our inductive biases, walking through cases, such as negation and scope ambiguity, where next-word-prediction objectives clearly fall short, and showing how targeted unlikelihood training with distillation can correct models like BERT

### Benoît Sagot (INRIA Almanach, Paris): Why Small Language Models Struggle

[Benoît Sagot](http://alpage.inria.fr/~sagot/) presented joint work with his PhD student Nathan Godey on why small language models underperform, tracing the phenomenon to a "saturation" effect visible in Pythia checkpoints: smaller models' training loss plateaus and eventually worsens, a behavior he linked to representational anisotropy and the softmax bottleneck. The finding is important for anyone hoping to train inference-efficient models under modern scaling laws.

### Lili Mou (University of Alberta, Amii): Language Models as Hidden Reward Signals

[Lili Mou](https://lili-mou.github.io/) closed the day with work on using LLMs as implicit reward functions, drawing theoretical connections between inverse reinforcement learning and pretrained language models, and showing how the resulting reward signals can be applied to semi-supervised learning and knowledge distillation.

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

[Yang Xu](https://www.cs.toronto.edu/~yangxu/) opened with a provocation: the objective function of language models, from Shannon's n-grams to GPT, has remained essentially unchanged for seventy years, yet natural language has evolved under very different pressures. He proposed three C's shaping lexical evolution: communication (the lexicon as an information-theoretic compressor, squeezing infinite ideas through a finite symbolic bottleneck), cognition (the mind extending its vocabulary to keep up with a changing world), and culture (the social forces that shape which new words stick). Each opens points of contact, and of friction, with computational models.

### Abdellah Fourtassi (Aix-Marseille Université): Using AI to Study How Children Learn Language

[Abdellah Fourtassi](https://afourtassi.github.io/) continued the dialogue between developmental science and NLP. He reminded the room that although early NLP drew on child-learning intuitions (Jeff Elman's simple recurrent networks being a canonical example), the two fields have drifted apart. He argued NLP tools now offer scalability that developmental psychology desperately needs. He presented results from "BabyBERTa," which, trained on only five million words of child-directed speech, achieves syntactic performance comparable to far larger models like RoBERTa, suggesting that children's linguistic input may be richer than classic poverty-of-the-stimulus arguments allowed.

### Guillaume Dumas (Université de Montréal, Mila): The Gap Between Brains and Language Models

[Guillaume Dumas](https://www.extrospection.eu/) warned against the "map–territory fallacy" of conflating LLMs with human cognition. His lab's research on interbrain synchronization, the coupled neural dynamics of two people in conversation, revealed by hyperscanning, shows how much of human language is fundamentally interactive. Similar representations across model layers and brain regions, he cautioned, do not imply similar underlying processes.

### Benjamin Morillon (Aix-Marseille Université, INSERM): What Language Models Reveal About the Brain

[Benjamin Morillon](https://ins-amu.fr/benjaminmorillon) brought the biological perspective forward with intracranial recordings of patients listening to both speech and music. He showed how the predictive-coding framework unifies auditory processing across domains, and how large language models provide a valuable regressor for localizing where and when the brain generates expectations about upcoming words, while emphasizing that correlation between layer activations and brain signals is a starting point, not a conclusion, about shared mechanisms.

### Maxime Peyrard (CNRS, Grenoble): Can We Really Explain What a Neural Network Is Doing? and Dhanya Sridhar (Université de Montréal, Mila): What Language Models Are Actually Learning From Examples

The afternoon session on causal models for NLP paired [Maxime Peyrard](https://peyrardm.github.io/) with [Dhanya Sridhar](https://www.dsridhar.com/). Peyrard surveyed interpretability, outlining where current mechanistic interpretability converges with or diverges from the older traditions of neural-network analysis. Sridhar asked whether in-context learning could be made more robust and sample-efficient by introducing causal inductive biases into how examples are selected and how the model infers regularities, a question of deep practical importance given how brittle prompting can be.

### Panel Discussion

The day closed with a panel moderated by Jackie Chi Kit Cheung and Frédéric Béchet, with Frank Rudzicz, Yang Xu, Claire Gardent, Serena Villata, Benjamin Morillon, Guillaume Dumas, and Aaron Courville. The discussion ranged over whether AI and neuroscience can genuinely inform each other, concerns about benchmark culture and reproducibility in NLP research, the risks of deploying language technology in healthcare, the emerging challenges of systems where multiple AI agents interact, and whether current safety measures are meaningfully improving model behavior or papering over deeper problems.

## Day 3

Day 3 turned to the broader societal and applied dimensions of NLP, opening with a welcome address from [Adeline Nazarenko](https://www.cnrs.fr/en/person/adeline-nazarenko), director of the CNRS Institute for Information Sciences and Technology. 

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

The conversational AI session opened with [Dilek Hakkani-Tür](https://dilek.web.illinois.edu/) on over-reliance: when a system speaks fluently, users accept its outputs uncritically, and the accountability gap widens. She argued dialogue systems need built-in uncertainty expression and explicit deferral mechanisms.

### Mirco Ravanelli (Concordia University, Mila): Teaching Language Models to Handle Audio

[Mirco Ravanelli](https://sites.google.com/site/mircoravanelli/) presented work on discrete audio tokens for multimodal LLMs, a pragmatic shift that lets models treat speech and audio on the same footing as text.

### Roland Memisevic (Qualcomm AI Research, Toronto): Building AI That Watches and Talks Back in Real Time

[Roland Memisevic](https://www-labs.iro.umontreal.ca/~memisevr/) closed the session with end-to-end learning for camera-based situated interaction, a reminder that embodied understanding will be central to the next generation of assistants.

### Serena Villata (CNRS i3s): Teaching Computers to Recognize Arguments and Jimmy Lin (University of Waterloo): Search as an Aid to Thinking

The information retrieval and argumentation session followed, with [Serena Villata](https://webusers.i3s.unice.fr/~villata/Home.html) on trustworthy natural-language argumentation, a field positioned to become critical as LLMs generate increasing volumes of persuasive text online, and [Jimmy Lin](https://cs.uwaterloo.ca/~jimmylin/) on the future of information retrieval in an LLM-mediated world, where the question of how to evaluate retrieval systems becomes more urgent, not less.

### Saif Mohammad (National Research Council Canada): What Language Can Tell Us About Emotions

The application-domain session was perhaps the most grounded. [Saif Mohammad](https://www.saifmohammad.com/) spoke on NLP for affective science, asking which big questions about emotion, sentiment, and subjective experience can be meaningfully probed with current tools. 

### Frank Rudzicz (Dalhousie University): Language Technology in Healthcare

[Frank Rudzicz](https://www.dal.ca/faculty/computerscience/faculty-staff/Frank-Rudzicz.html) delivered a talk entitled "NLPrimum Non Nocere," first, do no harm, addressing the risks of deploying language technology in medical and clinical contexts where errors have real human costs. 

### Géraldine Damnati (Orange Innovation): Evaluation in the Real World

[Géraldine Damnati](https://sites.google.com/site/geraldinedamnati/) closed with a call to move from benchmark assessments to in-use evaluation: the gap between how models perform on curated test sets and how they behave in real deployments, she argued, has widened in the generative-AI era rather than narrowed.

### Closing reflections

Across three days, the workshop traced a clear arc: from the mechanics of generative NLP, through its relationship with human minds and brains, to its deployment in society. Several threads recurred. Benchmarks and evaluations are under strain, trusted less by those who build them most carefully. Scale unlocks capability but also amplifies disparity, especially along linguistic and cultural lines. Cognitive and neural comparisons with LLMs must avoid premature conclusions: similar outputs do not imply similar mechanisms. And societal deployment demands not just better models but better evaluation, accountability, and humility.

If there was a single takeaway, it was that progress in NLP now depends as much on rigorous contact with neighboring disciplines, such as linguistics, psychology, neuroscience, philosophy, and public policy, as on the next increase in parameter count. That contact was very much on display in Montréal.
