# HW_5.3


import string
def generate_hashtag(sentence):
    sentence = ''.join([char for char in sentence if char not in string.punctuation])
    words = sentence.split()
    hashtag = '#' + ''.join([word.capitalize() for word in words])
    if len(hashtag) > 140:
        hashtag = hashtag[:140]
    return hashtag
#Пример
print(generate_hashtag("Python Community"))  # -> #PythonCommunity
print(generate_hashtag("I Like python community!"))  # -> #ILikePythonCommunity
print(generate_hashtag("Should, I. subscribe? Yes!"))  # -> #ShouldISubscribeYes
