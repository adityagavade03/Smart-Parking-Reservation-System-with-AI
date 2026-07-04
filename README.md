# Smart-Parking-Reservation-System-with-AI

Smart Parking System – Project Summary

The Smart Parking System is an AI-based parking management solution that automates vehicle detection, license plate recognition, and parking record management using computer vision and deep learning. The system processes live camera feeds or recorded videos to identify vehicle number plates in real time and stores the detected information in a MongoDB database for monitoring and future verification.

The workflow begins by capturing video frames through OpenCV, followed by image preprocessing to improve detection quality. A YOLO-based object detection model is used to accurately locate vehicle number plates, and the detected plate regions are extracted for text recognition. EasyOCR is then applied to recognize the license plate characters, while preprocessing techniques such as grayscale conversion, thresholding, and noise removal improve OCR accuracy. The recognized text is validated using the standard Indian license plate format to eliminate incorrect detections.

To improve reliability, the system implements a plate stabilization mechanism that compares OCR results across multiple frames and stores only the most consistently detected license plate. This reduces duplicate entries and minimizes errors caused by motion blur or varying camera angles.

Detected vehicle information, including the license plate number, timestamp, and detection source, is stored in MongoDB for efficient querying and future comparison with registered users or authorized vehicles. The application also provides real-time visualization by displaying bounding boxes and recognized plate numbers on the video stream, making it suitable for monitoring and demonstrations.

The project follows a modular architecture consisting of detection, OCR, database, and visualization modules, allowing easy maintenance and future enhancements such as parking slot reservation, mobile application integration, user authentication, and automated entry/exit gate control. Performance is optimized using frame skipping, confidence threshold tuning, and lightweight OCR processing, enabling real-time operation on mid-range hardware.
