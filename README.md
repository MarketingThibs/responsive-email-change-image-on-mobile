# Change Image on mobile

How to display a different image according to the device used by the recipient

## The HTML block
- Add the `title-img-responsive` class on the desktop image (already added in our template)

- Add the `title-img-responsive` AND the `mobile` class on the mobile image (already added in our template)

> example: `class="title-img-responsive mobile"`
> 

```html
<table width="100%" cellspacing="0" cellpadding="0">
    <tr>
        <td align="center">
            <!-- desktop Image  -->
            <img src="http://desktop.jpg" height="300" width="600" style="padding: 0px; text-align: center; height: 362px; width: 620px; border: 0px;" class="title-img-responsive ">
            <!-- /desktop Image   -->
            <!-- mobile image -->
            <img src="http://mobile.jpg" height="300" width="600" style="padding: 0px; text-align: center; height: 362px; width: 620px; border: 0px;" class="title-img-responsive mobile">
            <!-- /mobile image -->
        </td>
    </tr>
</table>
```



## The CSS 
In the `<head>` of the email use the media queries before creating the CSS rules.

1 - this code **hides the mobile image** on the desktop version

```css 
.title-img-responsive.mobile {
  display: none;
}
```

2 - this code is **hidding the desktop image** on mobile version
```css
.title-img-responsive {
  display: none;
}
```

3 - this code is **displaying the mobile image** on the mobile version
```css
.title-img-responsive.mobile {
  display: block !important;
}
```

## Going further
- [Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)
