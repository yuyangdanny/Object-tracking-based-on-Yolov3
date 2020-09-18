# Object-tracking-based-on-Yolov3
基於Yolov3的物件追蹤
</br>
</br>
</br>這是使用real-time偵測的結果
</br>![A](https://github.com/yuyangdanny/Object-tracking-based-on-Yolov3/blob/master/real-time-result/1.PNG)  ![A](https://github.com/yuyangdanny/Object-tracking-based-on-Yolov3/blob/master/real-time-result/2.PNG)
</br>由上面兩張圖可得知 畫面中偵測到3個瓶子，但是編號各不同。
</br>而當藍色蓋子的瓶子移到中間時，編號不變，代表雖然都偵測為瓶子的標籤，但是對程式來說每個瓶子都是獨立的。但表物體可追蹤。
</br>
# Theorem:
</br>這是利用卡爾曼演算法基於yolo的應用:
</br>卡爾曼濾波器的主要步驟有兩個：1.預估  2.測量更新
</br><li> 預估：假如一數值在理論上時間內是不變得，但是實際上一段時間後就會有誤差，這些誤差就是"高斯白雜訊"
</br><li> 測量：假如一數值在理論上時間內是不變得，但是實際上測量就會存在誤差，這些誤差也是"高斯白雜訊"
</br>![A](https://github.com/yuyangdanny/Object-tracking-based-on-Yolov3/blob/master/real-time-result/423182.jpg)
</br>這使得下一次預測的bounding box可以根據當前的bounding box來更新參數，以實現物體追蹤的目的。
