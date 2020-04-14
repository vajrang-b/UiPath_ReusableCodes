import speech_recognition as sr

def SpeechToText():
    r= sr.Recognizer()
    with sr.Microphone() as source:
        Text= 'Nothing'
        print('say something');
        audio = r.listen(source)
        print('Time over, Thanks')
        try:
            Text = r.recognize_google(audio, language="en-US")
            print('Text: '+r.recognize_google(audio, language="en-US"));
        except:
                pass
            
    return Text

