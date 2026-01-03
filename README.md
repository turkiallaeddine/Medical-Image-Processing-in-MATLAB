# Medical Image Processing in MATLAB / معالجة الصور الطبية في MATLAB

## Part 1: Introduction / الجزء 1: مقدمة

### Introduction / المقدمة
English:  
Medical imaging is one of the most important fields in healthcare and biomedical engineering. It allows doctors and researchers to visualize the internal structures of the body without invasive procedures. Common medical images include X-rays, CT scans, MRI scans, and Ultrasound images.

Processing these images is crucial because raw images often contain noise, low contrast, or artifacts, making it difficult to analyze or measure anatomical structures accurately. That is why Medical Image Processing is used: to enhance image quality, extract meaningful information, and support diagnosis.

العربية:  
تُعتبر معالجة الصور الطبية من أهم المجالات في الرعاية الصحية والهندسة الطبية الحيوية. فهي تتيح للأطباء والباحثين رؤية الهياكل الداخلية للجسم دون الحاجة إلى تدخل جراحي. الصور الطبية الأكثر شيوعًا تشمل الأشعة السينية (X-ray)، الأشعة المقطعية (CT)، الرنين المغناطيسي (MRI)، والموجات فوق الصوتية (Ultrasound).

تُعتبر معالجة هذه الصور أمرًا مهمًا لأن الصور الخام غالبًا ما تحتوي على ضوضاء أو تباين منخفض أو تشويش، مما يصعب تحليلها أو قياس الهياكل بدقة. لذلك، تُستخدم معالجة الصور الطبية لتحسين جودة الصورة، واستخراج المعلومات المهمة، ودعم التشخيص الطبي.

---

### Importance of MATLAB / أهمية MATLAB
English:  
MATLAB is a powerful tool for medical image processing because it provides:  
- Functions to read and display medical images, including DICOM format.  
- Tools for image enhancement (contrast adjustment, histogram equalization).  
- Filters for noise reduction.  
- Functions for segmentation and measurements.

العربية:  
يُعد برنامج MATLAB أداة قوية لمعالجة الصور الطبية لأنه يوفر:  
- وظائف لــ قراءة وعرض الصور الطبية، بما في ذلك صيغة DICOM.  
- أدوات لــ تحسين الصور (تعديل التباين، معادلة المدرج التكراري).  
- فلاتر لــ إزالة الضوضاء.  
- وظائف لــ التقطيع واستخراج القياسات.

---

### Key Points of This Part / أهم النقاط
English:  
1. Understand what an image is and how it represents real-world data.  
2. Learn the different types of medical images and their properties.  
3. Introduce DICOM format as the standard for medical imaging.

العربية:  
1. فهم ما هي الصورة وكيف تمثل البيانات الواقعية.  
2. التعرف على أنواع الصور الطبية وخصائصها.  
3. مقدمة عن صيغة DICOM كالمعيار الأساسي للصور الطبية.

---

### What is an Image? / ما هي الصورة؟
English:  
An image is a 2D or 3D matrix, where each element represents the brightness or color of a pixel. In medical imaging, this value may indicate bone density, tissue intensity, or blood flow at that location.

العربية:  
الصورة عبارة عن مصفوفة ثنائية أو ثلاثية الأبعاد، حيث يحتوي كل عنصر في المصفوفة على قيمة تمثل سطوع أو لون البكسل. في الصور الطبية، هذه القيمة قد تمثل كثافة العظم، أو الأنسجة، أو تدفق الدم في ذلك الموقع.
