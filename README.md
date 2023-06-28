# AILaw
# EasyOCR -- extracting text from img
import easyocr

def extract_text_from_image(image_path):
    reader = easyocr.Reader(['en'])

    result = reader.readtext(image_path)

    for detection in result:
        text = detection[1]
        print(text)

extract_text_from_image('/Users/lqn/PycharmProjects/demo/image/page.jpeg')
