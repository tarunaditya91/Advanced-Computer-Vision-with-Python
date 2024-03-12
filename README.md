# Advanced-Computer-Vision-with-Python
 
mpDraw=mp.solutions.drawing_utils  will help us to draw all the 21 points 
handlms gives us the number of hands 


![image](https://github.com/tarunaditya91/Advanced-Computer-Vision-with-Python/assets/113850656/bd0dfb06-f004-4a9b-90c9-fe56c14b3a2a)



To add the connections we can add mpDraw.draw_landmarks(frames,handlms,mpHands.HAND_CONNECTIONS)

![image](https://github.com/tarunaditya91/Advanced-Computer-Vision-with-Python/assets/113850656/a4e08f61-b2f6-4a77-9603-e41004f1c363)

for id,ml in enumerate(handlms.landmark):
print(id,ml)
landmark is provided by the mediapipe we are printing the id and ml which is x,y,z
![image](https://github.com/tarunaditya91/Advanced-Computer-Vision-with-Python/assets/113850656/3d91c0b3-78fe-483c-98bc-78d0f758899b)

now we are taking x and y to fid the cx,cy as center of the point useing
for id,ml in enumerate(handlms.landmark):
                # print(id,ml)
                h,w,c=frames.shape
                cx,cy=int(ml.x*w),int(ml.y*h)
                print(id,cx,cy)
then we will get
![image](https://github.com/tarunaditya91/Advanced-Computer-Vision-with-Python/assets/113850656/b79b84ce-bb75-45ed-83aa-32d609d45396)

with the help of this land mark we can detect the point on the hand to show that we HAVE USED the if condition
if id==0:
cv2.circle(frames,(cx,cy),(255,0,255),5,cv2.FILLED)

![image](https://github.com/tarunaditya91/Advanced-Computer-Vision-with-Python/assets/113850656/8157b208-789b-4326-b477-3599c16ab7bb)





