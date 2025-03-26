# **Computer Graphics Olympiad**
Данный репозиторий содержит Unity URP Sample (для версии 2022.2.58f).

Для выполнения заданий, необходимо сделать форк этого репозитория. Все решения должны быть публиковать на своем гите. <br>
В данной олимпиаде не допускается использовать сторонние ассеты, плагины, ShaderGraph и другие API, решающие поставленные задачи.

## **Task 1**

В первом задании необходимо написать собственный шейдер, реализующий одну (на выбор участника) PBR шейдинг модель от одного направленного (directional) источника света. Цвет и направление источника света должны быть учтены. <br>
За основу можно взять **Sample.shader**, расположенный по пути "Assets/Shaders/PBR-sample". <br>
Данный шейдер должен корректно учитывать следующие компоненты:
  * Коэффициент шероховатости поверхности [0; 1]
  * Коэффициент металличности поверхности [0; 1]
  * Текстурная карта материала (Diffuse Map)
  * Текстурная карта шероховатости поверхности материала (Roughness map)
  * Текстурная карта металличности поверхности материала (Metallic map)
  * Текстурная карта нормалей поверхности материала (Normal map)

Текстурные карты шероховатости и металличности не должны конфликтовать с аналогичными коэффициентами. <br>
Решение должно быть комплексным и учитывать совокупность данных параметров.

Вспомогательные ресурсы: <br>
https://google.github.io/filament/Filament.html <br>
https://learnopengl.com/PBR/Theory <br>
https://catlikecoding.com/unity/tutorials/custom-srp/ <br>
https://catlikecoding.com/unity/tutorials/rendering/ <br>


## **Task 2**

Во втором задании необходимо реализовать процедурную анимацию плейна, расположенного на сцене "SampleScene". <br>
Вид анимации остается на выбор участника (как пример: волны, имитация повреждений при коллизии с другим мешем, преобразование в другой меш, “эффект желе” и тд). <br>
Задача должна быть выполнена с помощью одного из предложенных способов:
  * Single threaded C#
  * Single threaded Burst
  * Multi threaded Burst
  * GPU compute shader

Вспомогательные ресурсы: <br>
https://github.com/Unity-Technologies/MeshApiExamples?tab=readme-ov-file

## **Task 3**

В третьем задании необходимо реализовать собственный (кастомный) этап отрисовки для пост-процессинга. <br>
Алгоритм пост-процессинга остается на выбор участника. <br>
Как пример, можно реализовать: Bloom pass, Outline pass, Lens Flare pass, Color Grading pass, SSAO pass и тд. <br>
Кастомный проход необходимо внедрить в уже имеющийся рендер пайплан Unity c использованием ScriptableRendererFeature.

Вспомогательные ресурсы: <br>
https://docs.unity3d.com/6000.0/Documentation/Manual/urp/renderer-features/custom-rendering-pass-workflow-in-urp.html#inject-pass
