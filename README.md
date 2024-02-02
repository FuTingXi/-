# 观察者模式 / Observer mode / โหมดผู้สังเกตการณ์
## 简单介绍：这是一个Python程序思想简单实现的一个观察者模式程序。有一个Python文件，一个检测用的docu.txt文件，还有一个是包含源程序的txt文件（防止.py文件卡bug无法打开）
### 代码思想： 
- 首先，定义了一个抽象观察者类 Observer 和一个抽象发布者类 Publisher。这两个类为观察者模式的基础提供了抽象接口。

- 其次，定义了具体的文件发布者类 FilePublisher，它继承自发布者类。在文件发布者类中，通过使用 os 模块获取文件的
最后修改时间，并且通过 time 模块添加延迟，以避免频繁检查文件是否发生变化。文件发布者还包含一个方法 check_for_changes，
用于检查文件是否发生变化，并在文件发生变化时通知观察者。

- 再次，定义了具体的文件观察者类 FileUser，它继承自观察者类。在文件观察者类中，实现了 update 方法，用于处理文件
变化通知。每当文件发生变化时，观察者会收到通知，并打印出文件变化前后的内容。

- 最后，在主程序入口高层APi中，创建了文件发布者和文件观察者的实例，并将观察者附加到发布者。然后，通过一个循环持续检查文件
变化，如果文件发生变化，发布者会通知观察者。

### 使用方法:
- 通过把该代码放到有Python编译环境的编译软件中，然后让程序运行起来。txt文档就是我在程序测试当中所检测的文档，当txt文档内容发送变化时，就提醒开发者。由于精力有限，我只能做到这一步。再写这个Python程序的时候因为也是刚刚大学二年级上学期接触Python，一些功夫还不到家。存在很多不足，还请大佬们批评指正，多多包涵。



# 观察者模式 / Observer mode / โหมดผู้สังเกตการณ์
## Brief introduction: This is an observer mode program that is simply implemented using Python program ideas. There is a Python file, a docu.txt file for detection, and a txt file containing the source program (to prevent the .py file from being stuck and unable to be opened)
### Code idea:
- First, an abstract observer class Observer and an abstract publisher class Publisher are defined. These two classes provide abstract interfaces that are the basis of the Observer pattern.

- Secondly, a specific file publisher class FilePublisher is defined, which inherits from the publisher class. In the file publisher class, get the file's
Last modified time, and a delay is added via the time module to avoid frequent checks to see if the file has changed. The file publisher also contains a method check_for_changes,
Used to check whether files have changed and notify observers when files change.

- Again, a specific file observer class FileUser is defined, which inherits from the observer class. In the file observer class, the update method is implemented for processing files
Change notifications. Whenever the file changes, the observer will be notified and print out the contents of the file before and after the change.

- Finally, in the main program entry high-level API, instances of the file publisher and file observer are created, and the observer is attached to the publisher. Then, continue checking the file through a loop
Changes, the publisher notifies observers if the file changes.

### Instructions:
- By putting the code into compilation software with a Python compilation environment, and then letting the program run. The txt document is the document I detected during program testing. When the content of the txt document changes, the developer will be reminded. Due to limited energy, I can only do this step. When I wrote this Python program, I had just come into contact with Python in the first semester of my sophomore year in college, so I didn’t know how to master it. There are many shortcomings, and I would like to ask the bosses to criticize and correct me. Please bear with me.



# 观察者模式 / Observer mode / โหมดผู้สังเกตการณ์
## บทนำโดยย่อ: นี่คือโปรแกรมโหมดผู้สังเกตการณ์ที่ใช้งานได้ง่ายโดยใช้แนวคิดโปรแกรม Python มีไฟล์ Python, ไฟล์ docu.txt สำหรับการตรวจจับ และไฟล์ txt ที่มีโปรแกรมต้นฉบับ (เพื่อป้องกันไม่ให้ไฟล์ .py ติดค้างและไม่สามารถเปิดได้)
### แนวคิดโค้ด:
- ขั้นแรก มีการกำหนดคลาสผู้สังเกตการณ์เชิงนามธรรมและผู้เผยแพร่คลาสผู้เผยแพร่เชิงนามธรรม คลาสทั้งสองนี้จัดเตรียมอินเทอร์เฟซเชิงนามธรรมที่เป็นพื้นฐานของรูปแบบผู้สังเกตการณ์

- ประการที่สอง มีการกำหนดคลาสผู้เผยแพร่ไฟล์เฉพาะ FilePublisher ซึ่งสืบทอดมาจากคลาสผู้เผยแพร่ ในคลาสผู้เผยแพร่ไฟล์ ให้รับไฟล์
เวลาที่แก้ไขครั้งล่าสุด และเพิ่มการหน่วงเวลาผ่านโมดูลเวลาเพื่อหลีกเลี่ยงการตรวจสอบบ่อยครั้งเพื่อดูว่าไฟล์มีการเปลี่ยนแปลงหรือไม่ ผู้เผยแพร่ไฟล์ยังมีวิธีการ check_for_changes
ใช้เพื่อตรวจสอบว่าไฟล์มีการเปลี่ยนแปลงหรือไม่ และแจ้งให้ผู้สังเกตการณ์ทราบเมื่อไฟล์มีการเปลี่ยนแปลง

- อีกครั้ง มีการกำหนดคลาสผู้สังเกตการณ์ไฟล์เฉพาะ FileUser ซึ่งสืบทอดมาจากคลาสผู้สังเกตการณ์ ในคลาสผู้สังเกตการณ์ไฟล์ วิธีการอัพเดตจะถูกนำไปใช้ในการประมวลผลไฟล์
เปลี่ยนการแจ้งเตือน เมื่อใดก็ตามที่ไฟล์มีการเปลี่ยนแปลง ผู้สังเกตการณ์จะได้รับแจ้งและพิมพ์เนื้อหาของไฟล์ก่อนและหลังการเปลี่ยนแปลง

- ในที่สุด ใน API ระดับสูงของรายการโปรแกรมหลัก อินสแตนซ์ของผู้เผยแพร่ไฟล์และผู้สังเกตการณ์ไฟล์จะถูกสร้างขึ้น และผู้สังเกตการณ์จะถูกแนบไปกับผู้เผยแพร่ จากนั้นทำการตรวจสอบไฟล์ต่อไปแบบวนซ้ำ
การเปลี่ยนแปลง ผู้เผยแพร่จะแจ้งให้ผู้สังเกตการณ์ทราบหากไฟล์มีการเปลี่ยนแปลง

### คำแนะนำ:
- โดยการใส่โค้ดลงในซอฟต์แวร์การคอมไพล์ด้วยสภาพแวดล้อมการคอมไพล์ Python แล้วปล่อยให้โปรแกรมทำงาน เอกสาร txt คือเอกสารที่ฉันตรวจพบระหว่างการทดสอบโปรแกรม เมื่อเนื้อหาของเอกสาร txt เปลี่ยนแปลง นักพัฒนาจะได้รับการเตือน เนื่องจากพลังงานมีจำกัด ฉันจึงทำได้เพียงขั้นตอนนี้เท่านั้น ตอนที่ฉันเขียนโปรแกรม Python นี้ ฉันเพิ่งได้รู้จักกับ Python ในภาคเรียนแรกของปีที่สองในวิทยาลัย ดังนั้นฉันจึงไม่รู้ว่าจะเชี่ยวชาญมันได้อย่างไร มีข้อบกพร่องมากมายและฉันอยากจะขอให้หัวหน้าวิพากษ์วิจารณ์และแก้ไขฉัน โปรดอดทนกับฉัน



