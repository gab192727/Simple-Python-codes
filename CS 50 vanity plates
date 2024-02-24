def main():
    plate = input("Plate: ")
    if is_valid(plate):
        print("Valid")
    else:
        print("Invalid")


def is_valid(plates):
    if not 2 <= len(plates) <= 6 or not all(check.isalpha() or check.isdigit() for check in plates):
        return False
    if not (plates.isupper() and plates[0:2].isalpha()):
        return False
    checker = ''
    for checks in range(1, len(plates)):
        if plates[checks].isdigit():
            checker += plates[checks]
        elif plates[checks].isalpha() and plates[checks - 1].isdigit():
            return False
    if checker != '' and checker[0] == "0":
        return False

    return True


if __name__ == '__main__':
    main()
