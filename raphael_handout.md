## Raphael Handout

### Learning Objectives

1. Be able to identify *what* Bootstrap is.

2. Understand *how to implement Bootstrap* in any project.

3. Recognize the *pros and cons of Bootstrap*, and explain why, or why not, Bootstrap is right for a project.

4. Be comfortable with *at least 1 Bootstrap element*

    4.1. Explain *how Bootstrap elevates the element*
  
    4.2. Recognize *what the Bootstrap classes do* and how they affect the element
  
5. Know *where to look to find extra help* when implementing Bootstrap.

6. Be able to name *at least 1 alternative* to Bootstrap.

### How to Get Bootstrap Into Your Code

1. Add this to the head:
```
<meta name="viewport" content="width=device-width, initial-scale=1">
```
2. Add this code also to the head:
```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi" crossorigin="anonymous">
```

3. Finally, insert this code into the body.
```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-OERcA2EqjJCMA+/3y+gxIOqMEjwtxJY7qPCqsdltbNJuaOe923+mo//f6V8Qbsw3" crossorigin="anonymous"></script>
```

### Quiz Questions

1. What is Bootstrap?

2. List two of the main benefits of Bootstrap.

3. Is Bootstrap a client or a server side framework?

4. How many tags do you need to include in your project to add Bootstrap and where do they go?

5. What are the 2 aspects of a Bootstrap component?

6. What is one limitation of Bootstrap?

7. Name one alternative to Bootstrap.

8. Choose your favorite Bootstrap element. Name some of the essential classes needed to make it Bootstrap.

9. Choose your favorite Bootstrap element. Explain how Bootstrap enhances the element.

10. Name one source for finding extra help on Bootstrap.

### Bootstrap Cheat Sheet

| Element | Some Common Classes |
| ------- | ------- |
| Toasts | toast, toast-container, toast-body, in js -> new bootstrap.Toast(toastLiveExample) toast.show() |
| Forms | form-control, form-inline, form-group, row, col, needs-validation, is-valid, is-invalid |
| Grids | container, container-fluid, row, col-\*, no-gutters |
| Navbars | navbar, navbar-toggler, navbar sticky-top, navbar-light, collapse navbar-collapse |
| Buttons | btn, btn-primary, btn-outline-danger, btn-link, btn-dark |
| Popovers | Popovers don't use classes, rather, include these attributes in an HTML button element: data-toggle="popover", data-placement (where popover appears), data-content (what popover says) |

[*This is not an all inclusive list of Bootstrap elements and classes, if you're still interested, check out this site for a really helpful list of Bootstrap classes organized by element*](https://hackerthemes.com/bootstrap-cheatsheet/)

[Another option is **Bootstrap's doc page**, accessible here!](https://getbootstrap.com/docs/5.2/getting-started/introduction/)

### Codepens for Practice

- [Toasts](https://codepen.io/ediey/pen/ZEROMqY)
- [Forms](https://codepen.io/ediey/pen/ZERpjGJ?editors=1010)
- [Grids](https://codepen.io/margoth/pen/wvXzxoM)
- [Navbars](https://codepen.io/zhao-sherry/pen/KKegLpj)
- [Buttons](https://codepen.io/zhao-sherry/pen/WNyxbxY)
- [Popovers](https://codepen.io/kubiteddie/pen/QWxKZyR)
