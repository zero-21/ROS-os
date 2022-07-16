robot os (ros)
السلام عليم ورحمة الله وبركاته
سنتحدث اليوم عن طريقة تثبيت نظام التشغيل روز بطريقة (البيئة الأفتراضية)
لكن قبل ذلك سنتكلم قليلا عن نظام التشغيل روز وناخذ لمحة بسيطة عن تاريخه
نظام تشغيل الروبوت (روز) هو اشهر واضخم إطار مفتوح المصدر لعمل  وبناء تطبيقات الروبوت بحيث يتيح  العديد من الادوات والحزم التي يمكن التعديل والتطوير عليها من قبل مطورين اخرين

 الخطوة الاولى بعد تثبيت نظام التشغيل اوبينتو نقوم بطباعة الامر التالي في سطر الأوامر لتهئية الكومبيوتر لقبول البرامج  
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
الخطوة الثانية  نقوم بطباعة الامر التالي  
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
الخطوة الثالثة نتأكد انه النظام على اخرإصدار من التحديث عن طريق الامر التالي 
sudo apt update
الأن نقوم بإختيار حزمة روز التي نريدها
اذا تريد النسخة الكاملة قم بطباعة الأمر التالي 
sudo apt install ros-noetic-desktop-full
وإذا كنت تريد تثبيت نسخه من غير أدوات واجهة المستخدم الرسومية(يناسب الاجهزة ذات كرت الشاشه الضعيف ) قم بطباعة الامر التالي 
sudo apt install ros-noetic-ros-base
ثم نقوم بتأكد من وجود نواة الروزعن طريق كتابة في سطر الأوامر
roscore
ثم لم يكن موجود سنقوم بكتابة الامر التالي 
sudo apt install python3-roslaunch
ثم نقوم بطباعة الأمر التالي 
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
ثم
source ~/.bashrc
ثم نقوم بطباعة الأمر التالي في سطر الأوامر 
sudo apt install ros-noetic-tuertlesim



