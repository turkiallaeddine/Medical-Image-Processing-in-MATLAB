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
## Part 2: Types of Medical Images / الجزء 2: أنواع الصور الطبية

### Introduction / مقدمة
English:  
There are several types of medical images, depending on the type of scan and the information they provide. Understanding these types is important for proper analysis and processing in MATLAB.

العربية:  
هناك عدة أنواع من الصور الطبية، تختلف حسب نوع الفحص والمعلومات التي تحتويها. فهم هذه الأنواع مهم لتحليلها ومعالجتها بشكل صحيح في MATLAB.

---

### 1️⃣ Grayscale Images / الصور الرمادية
English:  
- Each pixel has a single value between 0 and 255 (usually 8-bit).  
- Commonly used in X-rays and MRI slices.  
- Shows details clearly without color interference.

العربية:  
- كل بكسل يحتوي على قيمة واحدة بين 0 و255 (عادة 8-bit).  
- تُستخدم بكثرة في الأشعة السينية وشرائح الرنين المغناطيسي (MRI slices).  
- تعرض التفاصيل بوضوح بدون تأثيرات اللون.

---

### 2️⃣ RGB Images / الصور الملونة
English:  
- Each pixel has three values: Red (R), Green (G), Blue (B).  
- Used in some colored scans or microscopic images.  
- Less common in diagnostic imaging.

العربية:  
- كل بكسل يحتوي على ثلاث قيم: الأحمر (R)، الأخضر (G)، والأزرق (B).  
- تُستخدم في بعض الأشعة الملونة أو صور المجهر.  
- أقل شيوعًا في الفحوصات التشخيصية.

---

### 3️⃣ Binary Images / الصور الثنائية
English:  
- Each pixel is either 0 or 1 (black or white).  
- Usually used after segmentation to mark specific regions like tumors or bones.

العربية:  
- كل بكسل هو 0 أو 1 (أسود أو أبيض).  
- تُستخدم عادة بعد التقطيع (segmentation) لتحديد مناطق محددة مثل الأورام أو العظام.

---

### 4️⃣ DICOM Format / صيغة DICOM
English:  
- The most common standard in medical imaging.  
- Contains image data + additional information like:  
  - Patient name and scan date  
  - Pixel spacing  
  - Modality type (CT, MRI, Ultrasound)  
- Used widely in hospitals and research.

العربية:  
- المعيار الأكثر شيوعًا في الصور الطبية.  
- تحتوي الصورة على بيانات الصورة بالإضافة إلى معلومات إضافية مثل:  
  - اسم المريض وتاريخ الفحص  
  - المسافة بين البكسلات (Pixel Spacing)  
  - نوع الموداليتي (CT, MRI, Ultrasound)  
- تُستخدم على نطاق واسع في المستشفيات والأبحاث.

---

### Important Note / ملاحظة مهمة
English:  
Most medical images you will work with in MATLAB are grayscale or DICOM, because they contain the most accurate information and pixel measurements needed for analysis.

العربية:  
معظم الصور الطبية التي ستتعامل معها في MATLAB ستكون رمادية أو DICOM، لأنها تحتوي على المعلومات الدقيقة وقياسات البكسل اللازمة للتحليل.

---

### Optional: Example Table / جدول توضيحي
| Type / النوع | Example / المثال | Notes / ملاحظات |
|--------------|-----------------|----------------|
| Grayscale / رمادية | X-ray, MRI slices | Most common in diagnostic imaging |
| RGB / ملونة | Colored microscopic images | Rare in medical scans |
| Binary / ثنائية | Segmentation mask | After image processing |
| DICOM | CT, MRI, Ultrasound | Contains metadata for analysis |
### What is an Image? / ما هي الصورة؟
English:  
An image is a 2D or 3D matrix, where each element represents the brightness or color of a pixel. In medical imaging, this value may indicate bone density, tissue intensity, or blood flow at that location.

العربية:  
الصورة عبارة عن مصفوفة ثنائية أو ثلاثية الأبعاد، حيث يحتوي كل عنصر في المصفوفة على قيمة تمثل سطوع أو لون البكسل. في الصور الطبية، هذه القيمة قد تمثل كثافة العظم، أو الأنسجة، أو تدفق الدم في ذلك الموقع.
