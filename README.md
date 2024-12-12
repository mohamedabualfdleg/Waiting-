import random

def guess_the_number():
    print("مرحباً بك في لعبة تخمين الرقم!")
    print("سيختار الكمبيوتر رقمًا بين 1 و 100، وعليك تخمينه.")
    
    # اختيار رقم عشوائي بين 1 و 100
    number_to_guess = random.randint(1, 100)
    attempts = 0

    while True:
        try:
            # طلب إدخال اللاعب
            user_guess = int(input("أدخل تخمينك: "))
            attempts += 1

            if user_guess < number_to_guess:
                print("رقمك أقل من المطلوب! حاول مرة أخرى.")
            elif user_guess > number_to_guess:
                print("رقمك أكبر من المطلوب! حاول مرة أخرى.")
            else:
                print(f"مبروك! لقد خمنت الرقم الصحيح ({number_to_guess}) في {attempts} محاولة.")
                break
        except ValueError:
            print("الرجاء إدخال رقم صحيح!")

if __name__ == "__main__":
    guess_the_number(
