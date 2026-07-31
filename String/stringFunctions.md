# C++
s.size() / s.length() → length of string

s.empty() → check if string is empty

s[i] → access character at index

s.substr(pos, len) → substring

s.find("abc") → first occurrence index (or npos)

s.rfind("abc") → last occurrence index

s.compare(str) → lexicographic comparison

s.append(str) / s += str → concatenate 
 - currString.append("hello");          // append a C-string
 - currString.append(otherString);      // append another std::string
 - currString.append('x');  // error: 'x' is a char, not a string

 - What to use for a single character?
 - currString.append(1, 'x');           // append 1 copy of char 'x'
 - currString.append(5, '!');           // append 5 copies of '!'
 - or simply:  currString.push_back(ch);


s.insert(pos, str) → insert substring

s.erase(pos, len) → erase substring

s.replace(pos, len, str) → replace substring

s.c_str() → convert to C‑style char array

stoi(s) / stoll(s) / stod(s) → string → number

to_string(num) → number → string

toupper(ch) → convert a single character to uppercase

tolower(ch) → convert a single character to lowercase

transform(s.begin(), s.end(), s.begin(), ::toupper) → whole string to uppercase

transform(s.begin(), s.end(), s.begin(), ::tolower) → whole string to lowercase

- Case checks:

isupper(ch) / islower(ch) → check character case

isdigit(ch) / isalpha(ch) / isalnum(ch) → digit/letter checks

Reversal & sorting:

reverse(s.begin(), s.end()) → reverse string

sort(s.begin(), s.end()) → sort characters (useful for anagrams)

Unique & frequency:

unique(s.begin(), s.end()) → remove consecutive duplicates

count(s.begin(), s.end(), 'a') → count occurrences of a char

Stringstream parsing:
stringstream ss(s);
string word;
while (ss >> word) { ... }  // split by spaces

string s = "10,20,30";
stringstream ss(s);
string token;

while (getline(ss, token, ',')) {   // ',' is the delimiter
    int num = stoi(token);          // convert string → int
    cout << num << " ";
}

string s = "apple banana cherry";
stringstream ss(s);
string word;

while (ss >> word) {
    cout << word << endl;   // prints each word
}




# Python
len(s) → length of string

s[i] → access character at index

s.find("abc") → first occurrence index (−1 if not found)

s.rfind("abc") → last occurrence index

s.count("abc") → count occurrences

s.startswith("abc") / s.endswith("xyz") → prefix/suffix check

s.lower() / s.upper() → case conversion

s.strip() / s.lstrip() / s.rstrip() → trim whitespace

s.split(delim) → split into list

delim.join(list) → join list into string

s.replace("old", "new") → replace substring

int(s) / float(s) → string → number

str(num) → number → string

s.upper() → whole string to uppercase

s.lower() → whole string to lowercase

s.capitalize() → first character uppercase, rest lowercase

s.title() → capitalize each word

s.swapcase() → swap uppercase ↔ lowercase

- Checks:

s.isupper() / s.islower()

s.isdigit() / s.isalpha() / s.isalnum()

Reversal & sorting:

s[::-1] → reverse string

''.join(sorted(s)) → sort characters

Frequency & collections:

s.count('a') → count occurrences

collections.Counter(s) → frequency dictionary

Splitting & joining:

s.split() → split by whitespace

' '.join(list_of_words) → join with spaces
