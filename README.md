
THE RAPID DEVELOPMENT OF A COMPUTER VISION 
MODEL FOR DETECTING CROP PESTS FOR INTEGRATED 
PEST MANAGEMENT: A CASE STUDY IN THE BLACK VINE 
WEEVIL.
 
Abstract
Black vine weevil poses a significant threat to global agriculture, causing substantial damage 
and economic losses. Traditional manual methods of pest monitoring are labor-intensive, 
time-consuming, and prone to human errors, limiting their scalability for large-scale 
applications. To address these challenges, this study proposes a rapid pest detection 
method utilizing YOLOv8-based computer vision models. The primary objective is to develop 
an efficient and accurate system capable of automatically identifying and localizing crop 
pests, facilitating integrated pest management practices. The YOLOv8 algorithm, is 
employed for real-time object detection and precise localization. A labeled dataset 
comprising images of the black vine weevil (BVW) and earwig pests is utilized for model 
training and evaluation. Through an extensive exploration of hyperparameters, including 
image size, batch size, and epochs, the study aims to optimize the model training process 
for superior performance. Results indicate that YOLOv8n and YOLOv8s models outperform 
other model sizes, achieving high precision, recall, and mean average precision (mAP) at 
varying intersection-over-union (IoU) thresholds. And finally, validated the best performing 
model in a real-time pest detection of weevil and earwig. The proposed methodology 
showcases the potential of computer vision technologies in revolutionizing pest 
management, offering promising implications for precision pest control and sustainable 
agriculture.

Introduction
Insect pests are a major cause of crop damage globally, resulting in significant losses in 
agriculture (Nanni, Maguolo and Pancino, 2020). Crop pests can interfere with metabolic 
processes and reduce yield output and quality(Muralidharan and Pasalu, 2006). Regular 
pesticide use is often habitual, which while sometimes effectively contributes to the 
accumulation of pest resistance and potentially negatively impacting non-pest species, while 
contributing to business costs(Hazarika, Bhuyan and Hazarika, 2009). Indeed, there is 
evidence routine pesticide use negatively impacts the ecological environment and leaves 
pesticide residues in agricultural products(Miller and Spoolman, 2014). Pest population 
information cannot be easily and accurately obtained, further contributing to the practice of 
pesticide overuse. On the other hand, if accurate pest population information were easily 
and efficiently accessible, Adequate pest control approaches, such as the careful use of 
insecticides, and proper prevention measures may be achievable(Zhang and Swinton, 
2009). As a result, information on insect types and quantities is critical and essential. 
Because of the fast with the advancement of electronic picture technology, there's is a rising 
inclination towards adopting in the realm of agricultural research, technology for machine 
vision is being used to solve these difficulties with promising results.(Cho et al., 2007).
Traditional manual methods of insect pest monitoring, relying on human experts, are labourintensive, subjective, and unsuitable for large-scale applications (Ding and Taylor, 2016). 
Workers). Workers do this by comparing morphological features such as colour, texture, and 
other attributes. However, this often requires labour and expertise which are limiting and 
prone to mistakes (Cho et al., 2007)(Ding and Taylor, 2016). A potential solution is to 
automate pest identification. This need has given rise to solutions using computer vision 
(Cho et al., 2007). 
Even though certain pertinent studies have achieved significant advancements, their study 
still mostly focuses on theoretical issues and pays little attention to real-world application 
scenarios for two key reasons: First, methods other than deep learning are frequently used 
to measure and identify insects, yet the precision varies (Wang et al., 2012). Furthermore, 
most recent studies employ insect photos obtained in an ideal lab setting rather than in the 
field (Gassoumi, Prasad and Ellington, 2000) (Maharlooei et al., 2017a); (Larios et al.,
2010)(Kang, Cho and Lee, 2014)Although only a few studies employ photos of insects taken 
in the wild, these high-resolution photographs must be transferred to a server where the 
counting and identification tasks are accomplished. To overcome the obstacles Real-time 
object identification is an important task in computer vision and is commonly used in 
computer vision systems. An object detector employs an object detection approach to 
estimate bounding boxes and class probabilities for each item in the input picture when 
conducting image recognition tasks.
In the context of comprehensive pest management (IPM), pest control that combines and 
integrates biological and chemical control is defined (Stern et al., 1959). IPM tries to 
eliminate insect populations below the economic injury level which results in less effects on 
environment and human begins. The promise of computer vision models for automated, 
instantaneous detection of crop pests has gained significant attention. Such a model would 
facilitate the implementation of precision pest control measures, thereby reducing crop 
losses and remove the limitations of cost, time, and expertise. Among the pests 
Otiorhynchus sulcatus, sometimes known as the black vine weevil (BVW), is a significant 
pest of Horticultural crops, ornamentals used in landscaping. The black vine weevil harms 
host plants by marginally notching the leaves of broadleaved evergreens and other host 
plants. Adults prefer to consume plant leaves over culminating in subterranean tissues or 
fruits noticeable scratching with the leaf margin(Moorhouse, Charnley and Gillespie, 1992). 
Although it is well acknowledged that such notching has minimal influence Its presence has 
a negative impact on total crop health and can drastically impair the commercial value of 
attractive crops. that are less forgiving of aesthetic defects. (California Agriculture published 
descriptions of this univoltine species (having a single generation per year) in March–April 
1984, January–February 1985, and May–June 1989.The overall aim of this project is to 
rapidly develop a computer vision model that accurately detects the black vine weevil.
Objectives
My specific objectives are: 1) Create a reproducible methodology to rapidly create a baseline 
dataset for training, testing and validation for pest insect classification; 2) create a 
reproducible baseline classification and detection model using a comparative framework 
(different model sizes in a recent YOLO model framework); 3) create and test a reproducible 
experiment methodology to rapidly train and tune pest detection models for accuracy and 
speed; and 4) validate an example model using real pest images in a biologically relevant 
scenario. I will discuss my results in the context of opportunities of computer vision 
applications for solving integrated pest management problems.

Discussion
Objective 1: Create a reproducible methodology to rapidly create a baseline dataset for 
training, testing, and validation for pest insect classification.
To achieve this objective, we developed a reproducible methodology for creating a baseline 
dataset to train, test, and validate the pest insect classification model. Leveraging a 
previously curated database, we assembled the dataset consisting of two classes: black vine 
weevil and earwig pests. This dataset is crucial for training and evaluating the computer 
vision model accurately.
The approach of creating a dataset using image analysis aligns with previous studies.(Cho
et al., 2007) demonstrated the application of image analysis for the automatic identification 
of whiteflies, aphids, and thrips in greenhouses. Similarly, (Maharlooei et al., 2017b) utilized 
image processing techniques for detecting soybean aphids in a greenhouse environment. 
These studies highlight the efficacy of image-based approaches for pest identification and 
management.
Objective 2: Create a reproducible baseline classification and detection model using a 
comparative framework (different model sizes in a recent YOLO model framework).
To fulfil this objective, we built a reproducible baseline classification and detection model 
using a comparative framework that involved different model sizes in the YOLOv8 model. By 
experimenting with YOLOv8n, YOLOv8s, YOLOv8m, YOLOv8l, and YOLOv8x, we aimed to 
identify the most efficient and accurate model for pest detection.
The adoption of the YOLO framework in this study is supported by (Jiang et al., 2022), who 
provided an extensive review of YOLO algorithm developments. They highlighted the 
versatility and real-time object detection capabilities of the YOLO framework, making it a 
suitable choice for pest detection applications.
Objective 3: Create and test a reproducible experiment methodology to rapidly train and tune 
pest detection models for accuracy and speed.
To address this objective, we developed and tested a reproducible experiment methodology 
to rapidly train and tune the pest detection models. By systematically adjusting 
hyperparameters, such as image size, batch size, and epochs, optimized the models for 
improved accuracy and computational efficiency.
Hyperparameter tuning is a critical aspect of deep learning model development, and it has 
been explored in various studies. (Ferri, Hernández-Orallo and Modroiu, 2009) performed 
an experimental comparison of performance measures for classification tasks and 
emphasized the importance of selecting appropriate hyperparameters to enhance model 
performance. In this context, the methodology used in the current study aligns with 
established best practices in deep learning.
Objective 4: Validate an example model using real pest images in a biologically relevant 
scenario.
To achieve objective 4, The developed model was validated using real pest images in a 
biologically relevant scenario. We ensured that the model could accurately distinguish 
between black vine weevils and earwigs in practical agricultural settings, thus establishing its 
real-world applicability.
The importance of validation with real-world images is well-documented in the literature. (Li
et al., 2021) conducted a systematic review of classification and detection of insects using 
deep learning for smart pest management. We emphasized the need for validation with real 
field images to ensure the robustness of the models in actual pest control scenarios. The 
successful validation in this study confirms the potential of the developed model for practical 
pest management applications.
Conclusion
To summarise, we created an efficient and robust object detection system YOLOv8 based on 
computer vision for accurate detection of Weevils and Earwigs in this study. When 
comparing the performance of several YOLOv8 models, fascinating discoveries emerge. 
Yolov8n and Yolov8s routinely exhibit excellent accuracy, recall, mAP50, and mAP50-90 
scores, making them appropriate candidates for accurate object detection tasks in the 
Earwig and Weevil. The results for Yolov8m, Yolov8l, and Yolov8x are slightly lower, 
demonstrating an imbalance both the level of complexity and efficiency. Among the models 
evaluated, Yolov8n and Yolov8s appear to be the most sturdy and accurate options.
However, the performance drop is minor, demonstrating that the models may still retain good 
accuracy with bigger batch sizes and better picture resolutions. The top-performing models 
across all configurations are the YOLOv8n and YOLOv8s. They regularly earn the greatest 
accuracy, recall, mAP50, and mAP50-90 scores, making them the best models for detecting 
Weevils and Earwigs. The excellent accuracy and recall scores of the YOLOv8n and 
YOLOv8s algorithms show their potential usefulness for accuracy Horticultural and 
agricultural applications such as pest management. Their capacity to identify and localise 
Weevil and Earwig occurrences can help to develop more efficient and focused pest 
management techniques, which will improve farming practises in the long run. Therefore, 
based on the evidence we presented in this study, YOLOv8n and YOLOv8s are the best 
models for rapid and accurate pest detection in the context of integrated pest management 
for the black vine weevil case study.
