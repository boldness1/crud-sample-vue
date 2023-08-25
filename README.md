# nation-client

# Tüm proje config / env dosyaları ulaşılabilmesi açısından git'e dahil durumdadır
## Proje test staging url'i

## aws Ec2 instance

## http://ec2-35-159-25-42.eu-central-1.compute.amazonaws.com/

 "email":"johndoe@example.com",
 "password":"111111"

## Kullanıcı bilgileri olmak üzere, "johndoe1@example.com", "johndoe2@example.com" .... "johndoe11@example.com" e kadar 11 adet kullanıcı bulunmaktadır ve bunlardan 4 tanesi admin geriye kalanlar default kullanıcılardır
## birinci yani "johndoe@example.com" kullanıcısı admindir.

## Proje minimum vue3 gereksinimleri ile çalışmaktadır kullanılan toollar;

/stores -> Pinia (Store root klasörüdür ve 2 store modülünden oluşmaktadr)
 /stores -> auth
 /stores -> user
 
/router -> Vue router (Proje routelarnı içermektedir)
   {
      path: '/',
      name: 'home',
      component: HomeView
    },
    {
      path: '/login',
      name: 'login',
      component: LoginView
    },
    {
      path: '/users',
      name: 'users',
      meta: {requiresAuth: true},
      // route level code-splitting
      // this generates a separate chunk (About.[hash].js) for this route
      // which is lazy-loaded when the route is visited.
      component: () => import('../views/UsersView.vue')
    }
    
## Route yapısı toplam 3 route'tan oluşur anasayfa,login ve users.

Buradan sonrası default vue projesi kurulumudur, local kurulum anlatıldığı gibi default setup'a sahiptir.

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
