import cv2
import time


def main():
    window_name = "Live Video Feed"
    cv2.namedWindow(window_name)
    # for DirectShow (via videoInput) uncomment the below two lines using video source index depending on the camera you are using
    # videoSourceIndex = 1
    # cap = cv2.VideoCapture(cv2.CAP_DSHOW + videoSourceIndex)
    
    try:
        cap = cv2.VideoCapture(0)
    except:
        print("not working")

    finally:
        cap = cv2.VideoCapture(0)


    if cap.isOpened():
        ret, frame = cap.read()
    else:
        ret = False

    while ret:

        ret, frame = cap.read()

        cv2.imshow(window_name, frame)
        if cv2.waitKey(1) == 27:
            break

    cv2.destroyWindow(window_name)

    cap.release()


if __name__ == "__main__":
    main()
