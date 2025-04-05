.. Typescript Learning Note documentation master file, created by
   sphinx-quickstart on Fri Apr  4 22:41:39 2025.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Typescript Learning Note
======================================

.. 
   toctree::
   :maxdepth: 2
   :caption: Contents:


node のインストール
--------------------------------------

.. code-block:: bash
   :linenos:

   brew install nvm

   nvm install [node version]


Typescript を使う準備
--------------------------------------

.. code-block:: bash 
   :linenos:

   # TypeScript のインストール
   npm install -g typescript @types/node

   # TypeScript のバージョン確認
   tsc -v

   # TypeScript の初期化
   tsc --init


lint の設定
--------------------------------------

.. code-block:: bash 
   :linenos:

   npm init @eslint/config@latest

   Need to install the following packages:
   @eslint/create-config@1.6.0
   Ok to proceed? (y) 


   > npx
   > create-config

   @eslint/create-config: v1.6.0

   ✔ How would you like to use ESLint? · problems
   ✔ What type of modules does your project use? · esm
   ✔ Which framework does your project use? · none
   ✔ Does your project use TypeScript? · typescript
   ✔ Where does your code run? · browser
   The config that you've selected requires the following dependencies:

   eslint, globals, @eslint/js, typescript-eslint
   ✔ Would you like to install them now? · No / Yes
   ✔ Which package manager do you want to use? · npm
   ☕️Installing...

   added 2 packages, changed 1 package, and audited 126 packages in 3s

   36 packages are looking for funding
   run `npm fund` for details

   found 0 vulnerabilities

   ll
   total 192
   drwxr-xr-x@ 10 masarufukazawa  staff    320  4  5 00:38 ./
   drwxr-xr-x@ 82 masarufukazawa  staff   2624  4  4 22:51 ../
   -rw-r--r--@  1 masarufukazawa  staff    425  4  5 00:38 eslint.config.mjs
   drwxr-xr-x@ 97 masarufukazawa  staff   3104  4  5 00:38 node_modules/
   -rw-r--r--@  1 masarufukazawa  staff  59609  4  5 00:38 package-lock.json
   -rw-r--r--@  1 masarufukazawa  staff    241  4  5 00:38 package.json
   -rw-r--r--@  1 masarufukazawa  staff  12813  4  4 23:09 tsconfig.json


**src ディレクトリを作る**

- tsコードの保存先を作る

.. code-block:: bash 

   $ mkdir src

**package.json の編集**

.. code-block:: bash 
   :linenos:

   {
      "scripts": {
         "lint": "eslint --ext ts,tsx src/**/*",
         "lint:fix": "eslint --ext ts,tsx --fix src/**/"
      },
      "devDependencies": {
         "@eslint/js": "^9.23.0",
         "@typescript-eslint/eslint-plugin": "^8.29.0",
         "@typescript-eslint/parser": "^8.29.0",
         "eslint": "^9.23.0",
         "globals": "^16.0.0",
         "typescript-eslint": "^8.29.0"
      }
   }


lint の実行
--------------------------------------

.. code-block:: bash
   :linenos:

   npm run lint