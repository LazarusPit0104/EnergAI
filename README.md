# EnergAI: A Large Language Model–Driven Generative Design Method for Early-Stage Building Energy Optimization
Abstract: *The early stage of architectural design plays a decisive role in determining building energy performance, yet conventional evaluation is typically deferred to later phases, restricting timely and data-informed feedback. This paper proposes EnergAI, a generative design framework that incorporates energy optimization objectives directly into the scheme generation process through large language models (e.g., GPT-4o, DeepSeek-V3.1-Think, Qwen-Max, Gemini-2.5 pro). A dedicated dataset, LowEnergy-FormNet, comprising 2,160 cases with site parameters, massing descriptors, and simulation outputs, was constructed to model site, form and energy relationships. The framework encodes building massing into a parametric vector, applies hierarchical prompt strategies and integrates an automatic fenestration optimization module within a closed-loop interface to ClimateStudio. Experimental evaluations demonstrate that Geometry-Oriented and fuzzy-goal prompts achieve average annual reductions of approximately 16-17% in Energy Use Intensity and 3-4% in energy cost compared with human designs, while performance-oriented structured prompts deliver the most reliable improvements, eliminating high-energy outliers and yielding an average EUI saving rate above 50%.  In cross-model comparisons under an identical toolchain, GPT-4o delivered the strongest and most stable optimization, achieving 63.3% mean EUI savings, ~13 percentage points higher than DeepSeek-V3.1-Think, Qwen-Max and Gemini-2.5 baselines. These results demonstrate the feasibility and indicate the potential robustness of embedding performance constraints at the generation stage, providing a feasible approach to support proactive, data-informed early design*


[**Paper**]() | [**Project Page**]() | [**Model Weights**]() | [**Huggingface Demo**]() |


*Figure 1) Examples of design schemes and corresponding annotations in the dataset*
![img](assets/01.png)

*Figure 2) EnergAI closed-loop iterative workflow of parametric input, LLM prompting, performance simulation, and semantic feedback.*
![img](assets/05.png)

*Figure 3) Scatter plot of annual EUI vs. annual energy cost for the human-designed model and the geometry-oriented LLM-designed model.*
![img](assets/06.png)

*Figure 4) Impact of climate information on EUI and energy cost.*
![img](assets/02.png)

*Figure 5) Impact of design strategy on EUI.*
![img](assets/03.png)

*Figure 6)  Impact of design strategy on energy cost.*
![img](assets/03.png)

*Figure 7) Wordclouds.*
![img](assets/03.png)

*Figure 8) Mean energy-saving rate versus the number of prompt dimensions. *
![img](assets/03.png)



## Dataset

*Realistic Image_completed.*
![img](sample/001.jpg)

*Realistic Image_partial.*
![img](sample/002.jpg)

*Perspective Image.*
![img](sample/003.jpg)

*Render Image.*
![img](sample/004.jpg)

*CAD Image.*
![img](sample/005.jpg)

*Pen drawing Image.*
![img](sample/006.jpg)

*Illustration Image.*
![img](sample/007.jpg)

*Watercolor Image.*
![img](sample/008.jpg)

*Book Image.*
![img](sample/009.jpg)

*Digital Model Image.*
![img](sample/010.jpg)

*Historical Document Image.*
![img](sample/011.jpg)

## TODO List

- [x] Release part of LowEnergy-FormNet dataset. 
- [ ] Release EnergAI code and pretrain weights.
- [ ] Upload EnergAI training dataset.




## Inference

```
python Segment_Any_Architecture_Facade_Sample.py --dataset ArchiMetricsNet --batch_size 32  --color_configuration 0 --model_path ckpts/exp/model10000.pt --num_samples 64
```
## Train

```
python Segment_Any_Architecture_Facade_Train.py --dataset ArchiMetricsNet --batch_size 32  --color_configuration 0 
