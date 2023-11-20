# -5
Саліга Артем 1Варіант

    def read_file(file_path):
        with open(file_path, 'r', encoding='utf-8') as file:
            text = file.read()
        return text

    def get_word_frequency(text):
        words = re.findall(r'\b\w+\b', text.lower())
        word_count = Counter(words)
        return word_count

    def main():
        file_path = 'Lw5.txt'
        text = read_file(file_path)
        word_frequency = get_word_frequency(text)

    print("Слово\t\tПоширення")
    print("------------------------")
    for word, count in word_frequency.items():
        print(f"{word.ljust(15)}{count}")

    if __name__ == "__main__":
        main()
