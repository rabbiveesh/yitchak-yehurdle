# ʬṏяƌƚе - The Yitzchak Yehurdle

This is inspired by a copyrighted game that we use no unique elements of. Made using React, Typescript, and Tailwind.

Changed to use a list of baby words, in honor of babies.

## Build and run

### To Run Locally:

Clone the repository and perform the following command line actions:

```bash
# clone the repo and cd into it
npm install
npm run start
```

### To build/run docker container:

#### Development

```bash
docker build -t game:dev .
docker run -d -p 3000:3000 game:dev
```

Open [http://localhost:3000](http://localhost:3000) in browser.

#### Production

```bash
docker build --target=prod -t game:prod .
docker run -d -p 80:80 game:prod
```

Open [http://localhost](http://localhost) in browser.

## FAQ

### How can I change the length of a guess?

- Update the `MAX_WORD_LENGTH` variable in [src/constants/settings.ts](src/constants/settings.ts) to the desired length.
- Update the `WORDS` array in [src/constants/wordlist.ts](src/constants/wordlist.ts) to only include words of the new length.
- Update the `VALID_GUESSES` array in [src/constants/validGuesses.ts](src/constants/validGuesses.ts) arrays to only include words of the new length.
