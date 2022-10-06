# obfile
`Obfile` or `Obfuscate File` is a command line utility to encrypt or decrypt the file with AES256.

# Installation
```bash
git clone https://github.com/FlareXes/obfile.git && cd obfile

pip install -r requirements.txt
```

# Usage
### Files
- To encrypt the file
    ```
    python main.py -e <filename>
    ```
    Above command will generate a `.enc` file with is encrypted with password


- To decrypt the file
    ```
    python main.py -d <filename>.enc
    ```

- To remove original file after any operation
    ```
    python main.py -d <filename>.enc -r
    ```
### Directory
- To encrypt the directory
    ```
    python main.py -er <dirname>
    ```
    Recursively encrypt all files inside directory but not inside subdirectories


- To encrypt the directory with depth
    ```
    python main.py -er <dirname> --depth 2
    ```
    Recursively encrypt all files inside specified directory till defined depth


- To encrypt whole directory till possible
    ```
    python main.py -er <dirname> --depth -1
    ```
    Any negative value of `--depth` will recursively encrypt all files inside specified directory


- To decrypt the specified directory
    ```
    python main.py -dr <dirname> --depth 2
    ```
  Decrypt the file inside specified directory till depth 2


- To remove original file after any operation use `-r`
    ```
    python main.py -dr <dirname> --depth -1 -r
    ```

---

> Note: `obfile` doesn't follow symbolic links.
# Licence 

MIT License

Copyright (c) 2022 FlareXes

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
