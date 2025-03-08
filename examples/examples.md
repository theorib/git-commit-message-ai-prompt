INPUT:

diff --git a/package.json b/package.json
index 456c4cb..7cbcdf1 100644
--- a/package.json
+++ b/package.json
@@ -128,7 +128,7 @@
"eslint-plugin-tsdoc": "^0.4.0",
"globals": "^16.0.0",
"husky": "^9.1.7",

- "inquirer": "^9.3.7",

* "inquirer": "^12.4.2",
  "jiti": "^2.4.2",
  "jsdom": "^26.0.0",
  "lint-staged": "^15.4.3",
  diff --git a/pnpm-lock.yaml b/pnpm-lock.yaml
  index 2e845db..360651c 100644
  --- a/pnpm-lock.yaml
  +++ b/pnpm-lock.yaml
  @@ -173,7 +173,7 @@ importers:
  version: 19.7.1
  '@commitlint/cz-commitlint':
  specifier: ^19.6.1

-        version: 19.6.1(@types/node@22.13.5)(commitizen@4.3.1(@types/node@22.13.5)(typescript@5.7.3))(inquirer@9.3.7)(typescript@5.7.3)

*        version: 19.6.1(@types/node@22.13.5)(commitizen@4.3.1(@types/node@22.13.5)(typescript@5.7.3))(inquirer@12.4.2(@types/node@22.13.5))(typescript@5.7.3)
         '@eslint/compat':
           specifier: ^1.2.7
           version: 1.2.7(eslint@9.21.0(jiti@2.4.2))
  @@ -295,8 +295,8 @@ importers:
  specifier: ^9.1.7
  version: 9.1.7
  inquirer:

-        specifier: ^9.3.7
-        version: 9.3.7

*        specifier: ^12.4.2
*        version: 12.4.2(@types/node@22.13.5)
         jiti:
           specifier: ^2.4.2
           version: 2.4.2

  @@ -942,6 +942,15 @@ packages:
  cpu: [x64]
  os: [win32]

* '@inquirer/checkbox@4.1.2':
* resolution: {integrity: sha512-PL9ixC5YsPXzXhAZFUPmkXGxfgjkdfZdPEPPmt4kFwQ4LBMDG9n/nHXYRGGZSKZJs+d1sGKWgS2GiPzVRKUdtQ==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
* '@inquirer/confirm@5.1.6':
  resolution: {integrity: sha512-6ZXYK3M1XmaVBZX6FCfChgtponnL0R6I7k8Nu+kaoNkT828FVZTcca1MqmWQipaW2oNREQl5AaPCUOOCVNdRMw==}
  engines: {node: '>=18'}
  @@ -960,10 +969,91 @@ packages:
  '@types/node':
  optional: true
* '@inquirer/editor@4.2.7':
* resolution: {integrity: sha512-gktCSQtnSZHaBytkJKMKEuswSk2cDBuXX5rxGFv306mwHfBPjg5UAldw9zWGoEyvA9KpRDkeM4jfrx0rXn0GyA==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
*
* '@inquirer/expand@4.0.9':
* resolution: {integrity: sha512-Xxt6nhomWTAmuSX61kVgglLjMEFGa+7+F6UUtdEUeg7fg4r9vaFttUUKrtkViYYrQBA5Ia1tkOJj2koP9BuLig==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
* '@inquirer/figures@1.0.10':
  resolution: {integrity: sha512-Ey6176gZmeqZuY/W/nZiUyvmb1/qInjcpiZjXWi6nON+nxJpD1bxtSoBxNliGISae32n6OwbY+TSXPZ1CfS4bw==}
  engines: {node: '>=18'}
* '@inquirer/input@4.1.6':
* resolution: {integrity: sha512-1f5AIsZuVjPT4ecA8AwaxDFNHny/tSershP/cTvTDxLdiIGTeILNcKozB0LaYt6mojJLUbOYhpIxicaYf7UKIQ==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
*
* '@inquirer/number@3.0.9':
* resolution: {integrity: sha512-iN2xZvH3tyIYXLXBvlVh0npk1q/aVuKXZo5hj+K3W3D4ngAEq/DkLpofRzx6oebTUhBvOgryZ+rMV0yImKnG3w==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
*
* '@inquirer/password@4.0.9':
* resolution: {integrity: sha512-xBEoOw1XKb0rIN208YU7wM7oJEHhIYkfG7LpTJAEW913GZeaoQerzf5U/LSHI45EVvjAdgNXmXgH51cUXKZcJQ==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
*
* '@inquirer/prompts@7.3.2':
* resolution: {integrity: sha512-G1ytyOoHh5BphmEBxSwALin3n1KGNYB6yImbICcRQdzXfOGbuJ9Jske/Of5Sebk339NSGGNfUshnzK8YWkTPsQ==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
*
* '@inquirer/rawlist@4.0.9':
* resolution: {integrity: sha512-+5t6ebehKqgoxV8fXwE49HkSF2Rc9ijNiVGEQZwvbMI61/Q5RcD+jWD6Gs1tKdz5lkI8GRBL31iO0HjGK1bv+A==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
*
* '@inquirer/search@3.0.9':
* resolution: {integrity: sha512-DWmKztkYo9CvldGBaRMr0ETUHgR86zE6sPDVOHsqz4ISe9o1LuiWfgJk+2r75acFclA93J/lqzhT0dTjCzHuoA==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
*
* '@inquirer/select@4.0.9':
* resolution: {integrity: sha512-BpJyJe7Dkhv2kz7yG7bPSbJLQuu/rqyNlF1CfiiFeFwouegfH+zh13KDyt6+d9DwucKo7hqM3wKLLyJxZMO+Xg==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
* '@inquirer/type@3.0.4':
  resolution: {integrity: sha512-2MNFrDY8jkFYc9Il9DgLsHhMzuHnOYM1+CUYVWbzu9oT0hC7V7EcYvdCKeoll/Fcci04A+ERZ9wcc7cQ8lTkIA==}
  engines: {node: '>=18'}
  @@ -3376,14 +3466,19 @@ packages:
  react: ^16.8 || ^17.0 || ^18.0 || ^19.0.0 || ^19.0.0-rc
  react-dom: ^16.8 || ^17.0 || ^18.0 || ^19.0.0 || ^19.0.0-rc
* inquirer@12.4.2:
* resolution: {integrity: sha512-reyjHcwyK2LObXgTJH4T1Dpfhwu88LNPTZmg/KenmTsy3T8lN/kZT8Oo7UwwkB9q8+ss2qjjN7GV8oFAfyz9Xg==}
* engines: {node: '>=18'}
* peerDependencies:
*      '@types/node': '>=18'
* peerDependenciesMeta:
*      '@types/node':
*        optional: true
* inquirer@8.2.5:
  resolution: {integrity: sha512-QAgPDQMEgrDssk1XiwwHoOGYF9BAbUcc1+j+FhEvaOt8/cKRqyLn0U5qA6F74fGhTMGxf92pOvPBeh29jQJDTQ==}
  engines: {node: '>=12.0.0'}

- inquirer@9.3.7:
- resolution: {integrity: sha512-LJKFHCSeIRq9hanN14IlOtPSTe3lNES7TYDTE2xxdAy1LS5rYphajK1qtwvj3YmQXvvk0U2Vbmcni8P9EIQW9w==}
- engines: {node: '>=18'}
- internal-slot@1.1.0:
  resolution: {integrity: sha512-4gd7VpWNQNB4UKKCFFVcp1AVv+FMOgs9NKzjHKusc8jTMhd5eL1NqQqOpE0KzMds804/yHlglp3uxgluOqAPLw==}
  engines: {node: '>= 0.4'}
  @@ -3916,10 +4011,6 @@ packages:
  mute-stream@0.0.8:
  resolution: {integrity: sha512-nnbWWOkoWyUsTjKrhgD0dcz22mdkSnpYqbEjIm2nhwhuxlSkpywJmBo8h0ZqJdkp73mb90SssHkN4rsRaBAfAA==}
- mute-stream@1.0.0:
- resolution: {integrity: sha512-avsJQhyd+680gKXyG/sQc0nXaC6rBkPOfyHYcFb9+hdkqQkR9bdnkJ0AMZhke0oesPqIO+mFFJ+IdBc7mst4IA==}
- engines: {node: ^14.17.0 || ^16.13.0 || >=18.0.0}
- mute-stream@2.0.0:
  resolution: {integrity: sha512-WWdIxpyjEn+FhQJQQv9aQAYlHoNVdzIzUySNV1gHUPDSdZJ3yZn7pAAbQcV7B56Mvu881q9FZV+0Vx2xC44VWA==}
  engines: {node: ^18.17.0 || >=20.5.0}
  @@ -4419,6 +4510,9 @@ packages:
  rxjs@7.8.1:
  resolution: {integrity: sha512-AA3TVj+0A2iuIoQkWEK/tqFjBq2j+6PO6Y0zJcvzLAFhEFIO3HL0vls9hWLncZbAAbK0mar7oZ4V079I/qPMxg==}

* rxjs@7.8.2:
* resolution: {integrity: sha512-dhKf903U/PQZY6boNNtAGdWbG85WAbjT/1xYoZIC7FAY0yWapOBQVsVrDl58W86//e1VpMNBtRV4MaXfdMySFA==}
* safe-array-concat@1.1.3:
  resolution: {integrity: sha512-AURm5f0jYEOydBj7VQlVvDrjeFgthDdEF5H1dP+6mNpoXOMo1quQqJ4wvJDyRZ9+pO3kGWoOdmV08cSv2aJV6Q==}
  engines: {node: '>=0.4'}
  @@ -5354,14 +5448,14 @@ snapshots:
  '@commitlint/types': 19.5.0
  ajv: 8.17.1

- '@commitlint/cz-commitlint@19.6.1(@types/node@22.13.5)(commitizen@4.3.1(@types/node@22.13.5)(typescript@5.7.3))(inquirer@9.3.7)(typescript@5.7.3)':

* '@commitlint/cz-commitlint@19.6.1(@types/node@22.13.5)(commitizen@4.3.1(@types/node@22.13.5)(typescript@5.7.3))(inquirer@12.4.2(@types/node@22.13.5))(typescript@5.7.3)':
  dependencies:
  '@commitlint/ensure': 19.5.0
  '@commitlint/load': 19.6.1(@types/node@22.13.5)(typescript@5.7.3)
  '@commitlint/types': 19.5.0
  chalk: 5.4.1
  commitizen: 4.3.1(@types/node@22.13.5)(typescript@5.7.3)

-      inquirer: 9.3.7

*      inquirer: 12.4.2(@types/node@22.13.5)
         lodash.isplainobject: 4.0.6
         word-wrap: 1.2.5
       transitivePeerDependencies:

  @@ -5711,6 +5805,16 @@ snapshots:
  '@img/sharp-win32-x64@0.33.5':
  optional: true

* '@inquirer/checkbox@4.1.2(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/figures': 1.0.10
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
*      ansi-escapes: 4.3.2
*      yoctocolors-cjs: 2.1.2
* optionalDependencies:
*      '@types/node': 22.13.5
* '@inquirer/confirm@5.1.6(@types/node@22.13.5)':
  dependencies:
  '@inquirer/core': 10.1.7(@types/node@22.13.5)
  @@ -5731,8 +5835,88 @@ snapshots:
  optionalDependencies:
  '@types/node': 22.13.5
* '@inquirer/editor@4.2.7(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
*      external-editor: 3.1.0
* optionalDependencies:
*      '@types/node': 22.13.5
*
* '@inquirer/expand@4.0.9(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
*      yoctocolors-cjs: 2.1.2
* optionalDependencies:
*      '@types/node': 22.13.5
* '@inquirer/figures@1.0.10': {}
* '@inquirer/input@4.1.6(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
* optionalDependencies:
*      '@types/node': 22.13.5
*
* '@inquirer/number@3.0.9(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
* optionalDependencies:
*      '@types/node': 22.13.5
*
* '@inquirer/password@4.0.9(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
*      ansi-escapes: 4.3.2
* optionalDependencies:
*      '@types/node': 22.13.5
*
* '@inquirer/prompts@7.3.2(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/checkbox': 4.1.2(@types/node@22.13.5)
*      '@inquirer/confirm': 5.1.6(@types/node@22.13.5)
*      '@inquirer/editor': 4.2.7(@types/node@22.13.5)
*      '@inquirer/expand': 4.0.9(@types/node@22.13.5)
*      '@inquirer/input': 4.1.6(@types/node@22.13.5)
*      '@inquirer/number': 3.0.9(@types/node@22.13.5)
*      '@inquirer/password': 4.0.9(@types/node@22.13.5)
*      '@inquirer/rawlist': 4.0.9(@types/node@22.13.5)
*      '@inquirer/search': 3.0.9(@types/node@22.13.5)
*      '@inquirer/select': 4.0.9(@types/node@22.13.5)
* optionalDependencies:
*      '@types/node': 22.13.5
*
* '@inquirer/rawlist@4.0.9(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
*      yoctocolors-cjs: 2.1.2
* optionalDependencies:
*      '@types/node': 22.13.5
*
* '@inquirer/search@3.0.9(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/figures': 1.0.10
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
*      yoctocolors-cjs: 2.1.2
* optionalDependencies:
*      '@types/node': 22.13.5
*
* '@inquirer/select@4.0.9(@types/node@22.13.5)':
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/figures': 1.0.10
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
*      ansi-escapes: 4.3.2
*      yoctocolors-cjs: 2.1.2
* optionalDependencies:
*      '@types/node': 22.13.5
* '@inquirer/type@3.0.4(@types/node@22.13.5)':
  optionalDependencies:
  '@types/node': 22.13.5
  @@ -8361,6 +8545,18 @@ snapshots:
  react: 19.0.0
  react-dom: 19.0.0(react@19.0.0)
* inquirer@12.4.2(@types/node@22.13.5):
* dependencies:
*      '@inquirer/core': 10.1.7(@types/node@22.13.5)
*      '@inquirer/prompts': 7.3.2(@types/node@22.13.5)
*      '@inquirer/type': 3.0.4(@types/node@22.13.5)
*      ansi-escapes: 4.3.2
*      mute-stream: 2.0.0
*      run-async: 3.0.0
*      rxjs: 7.8.2
* optionalDependencies:
*      '@types/node': 22.13.5
* inquirer@8.2.5:
  dependencies:
  ansi-escapes: 4.3.2
  @@ -8379,21 +8575,6 @@ snapshots:
  through: 2.3.8
  wrap-ansi: 7.0.0

- inquirer@9.3.7:
- dependencies:
-      '@inquirer/figures': 1.0.10
-      ansi-escapes: 4.3.2
-      cli-width: 4.1.0
-      external-editor: 3.1.0
-      mute-stream: 1.0.0
-      ora: 5.4.1
-      run-async: 3.0.0
-      rxjs: 7.8.1
-      string-width: 4.2.3
-      strip-ansi: 6.0.1
-      wrap-ansi: 6.2.0
-      yoctocolors-cjs: 2.1.2
- internal-slot@1.1.0:
  dependencies:
  es-errors: 1.3.0
  @@ -8931,8 +9112,6 @@ snapshots:
  mute-stream@0.0.8: {}
- mute-stream@1.0.0: {}
- mute-stream@2.0.0: {}
  nanoid@3.3.8: {}
  @@ -9398,6 +9577,10 @@ snapshots:
  dependencies:
  tslib: 2.8.1

* rxjs@7.8.2:
* dependencies:
*      tslib: 2.8.1
* safe-array-concat@1.1.3:
  dependencies:
  call-bind: 1.0.8

OUTPUT:
🔧 chore(deps): bump inquirer to version 12.4.2

- update inquirer dependency from version 9.3.7 to 12.4.2
- update pnpm-lock.yaml to reflect changes in the dependency tree

INPUT:
diff --git a/package.json b/package.json
index 7cbcdf1..afc918f 100644
--- a/package.json
+++ b/package.json
@@ -151,5 +151,12 @@
"react-is": "^19.0.0",
"eslint": "^9.19.0",
"date-fns": "^4.1.0"

- },
- "pnpm": {
- "onlyBuiltDependencies": [
-      "esbuild",
-      "msw",
-      "sharp"
- ]
  }
  }

OUTPUT:

🔧 chore(deps): add pnpm configuration to approve build scripts for specific dependencies

- add pnpm.onlyBuiltDependencies field to package.json
- specify esbuild, msw, and sharp as dependencies that require build scripts

INPUT:
diff --git a/eslint.config.ts b/eslint.config.ts
index bef3dd6..f3a29b0 100644
--- a/eslint.config.ts
+++ b/eslint.config.ts
@@ -336,6 +336,18 @@ const configNext = {
files: [...NEXT_JS_JSX_TS_TSX_FILE_PATTERNS],
} satisfies Config

+/\*\*

- - Some Next.js files have default async exports with function such as GET, POST, generateMetadata, generateStaticParams, etc.
- - When these functions are used, depending on the implementation they don't necessarily need to await for values thus we ewnt to turn some rules into warnings only in some specific files.
- \*/
  +const configNextCustomRoutes = {
- name: 'next/custom-routes',
- files: ['src/**/?(route|page|layout).?(c|m)?(t|j)s?(x)'],
- rules: {
- '@typescript-eslint/require-await': ['warn'],
- },
  +} satisfies Config
- /\*\*
  - next/core-web-vitals updates eslint-plugin-next to error on a number of rules that are warnings by default if they affect Core Web Vitals
  - @see {@link https://nextjs.org/docs/app/api-reference/config/eslint#with-core-web-vitals}
    @@ -503,6 +515,7 @@ const eslintConfig = [
  nextNextRecommended,
  configNext,
- configNextCustomRoutes,

  coreWebVitals,
  vitestRecommended,

OUTPUT:
✨ feat(eslint): add custom rule for async functions in Next.js routes

- add `configNextCustomRoutes` to handle specific Next.js files with default async exports
- set `@typescript-eslint/require-await` rule to `warn` for next.js `route`, `page` and `layout` files
  to accommodate cases where awaiting values is not necessary but functions have to be async
