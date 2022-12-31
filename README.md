# LoadMore Pagination

Simple VueJS project to create pagination. You Click LoadMore button, then fetch() function will request more posts and append already fetched posts. In this project, when component is mounted, fetch() function will fetch only 3 posts of first page and show in grid. LoadMore function is protected, clicking it will increment page number if no more posts are available than LoadMore button will disappear and No more data message will showup. Components templates are build will Tailwindcss.

## Initial Project setup
```
npm install
```

### Run Development Server
```
npm run serve
```

### Compiles Project for production
```
npm run build
```  
### Run JSON Backend Server
```
npm run back
```