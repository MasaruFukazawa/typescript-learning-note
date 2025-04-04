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

.. code-block:: shell
   :linenos:

   brew install nvm

   nvm install [node version]


Typescript を使う準備
--------------------------------------

.. code-block:: shell
   :linenos:

   # TypeScript のインストール
   npm install -g typescript @types/node

   # TypeScript のバージョン確認
   tsc -v

   # TypeScript の初期化
   tsc --init

   npm install --save-dev @typescript-eslint/parser @typescript-eslint/eslint-plugin

   ll 
   drwxr-xr-x@  9 masarufukazawa  staff    288  4  4 23:16 ./
   drwxr-xr-x@ 82 masarufukazawa  staff   2624  4  4 22:51 ../
   drwxr-xr-x@ 96 masarufukazawa  staff   3072  4  4 23:16 node_modules/
   -rw-r--r--@  1 masarufukazawa  staff  59822  4  4 23:16 package-lock.json
   -rw-r--r--@  1 masarufukazawa  staff    125  4  4 23:16 package.json
   -rw-r--r--@  1 masarufukazawa  staff  12813  4  4 23:09 tsconfig.json