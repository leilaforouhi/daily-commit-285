def alternate_case(text):
    result = []
    upper = True

    for char in text:
        if char.isalpha():
            result.append(char.upper() if upper else char.lower())
            upper = not upper
        else:
            result.append(char)

    return "".join(result)


if __name__ == "__main__":
    text = "daily github coding"

    print("Original:", text)
    print("Alternate case:", alternate_case(text))
