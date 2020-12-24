# Instructions

## 1. Upload images
1. Go to www.myonlinestartup.com/wp-admin
2. Click on `Media` in the left side menu
3. Click on the blue button `Add new`
4. Drag your images in to upload them

## 2. Write down image links
For each image you uploaded:
1. Click on each image so that you can see the full image with some extra info on the right hand side.
2. Go to the `File URL` and click on `Copy URL`. The URL should look something like:
```
https://myonlinestartup.com/media/name-of-image.png
```
3. Note this down somewhere

## 3. Get side banner code
1. Go to www.myonlinestartup.com/wp-admin
2. Go to `Appearance > Widgets` in the left side menu

On the right hand side, there should be a few boxes with a light blue top border

3. Click on the box `Free Course Banners1` to expand it
4. Click on "Custom HTML" to see the code
5. Copy the code into your code editor (e.g. VS Code).

If you save the file as something.html, you will get syntax highlighting and it will look something like this:

```html
<!-- START: Only Free Members will see these banners -->
[mos_if_level level=subscriber]
<!-- First banner -->
<a href="https://myonlinestartup.com/partner?utm_source=membership&utm_medium=Testimonial&utm_campaign=partner/" target="_blank" rel="noopener noreferrer"><img src="/media/partner-widget-small-cut-min.png" alt="Upgrade To Partner" class="conditional-banner-small"></a>
<!-- Second banner -->
<a href="https://www.facebook.com/groups/chucksmastermindgroup/" target="_blank" rel="noopener noreferrer"><img src="/media/mastermind-widget-small-cut-min.png" alt="Join Our Facebook Mastermind Group" class="conditional-banner-small"></a>
<!-- Third banner -->
<a href="https://www.facebook.com/OfficialMyOnlineStartup/" target="_blank" rel="noopener noreferrer"><img src="/media/stayupdated-widget-small-cut-min.png" alt="Stay Updated" class="conditional-banner-small"></a>
[/mos_if_level]
<!-- END: Only Free Members will see these banners -->

<!-- START: Only partners will see these banners -->
[mos_if_level level=partner]
<!-- First Banner -->
<a href="/legendary" target="_blank" rel="noopener noreferrer"><img src="/media/legendary-widget-small-cut-min.png" alt="Upgrade To Legendary Partner" class="conditional-banner-small"></a>
<!-- Second Banner -->
<a href="https://www.facebook.com/groups/chucksmastermindgroup/" target="_blank" rel="noopener noreferrer"><img src="/media/mastermind-widget-small-cut-min.png" alt="Join Our Facebook Mastermind Group" class="conditional-banner-small"></a>
<!-- Third Banner -->
<a href="https://www.facebook.com/OfficialMyOnlineStartup/" target="_blank" rel="noopener noreferrer"><img src="/media/stayupdated-widget-small-cut-min.png" alt="Stay Updated" class="conditional-banner-small"></a>
[/mos_if_level]
<!-- END: Only partners will see these banners -->


<!-- Start: Only Legendary and admins will see these banners -->
[mos_if_level level=_atleast_legendary_partner]
<!-- First Banner -->
<a href="https://www.facebook.com/groups/ChucksInnerCircle/" target="_blank" rel="noopener noreferrer"><img src="/media/innercircle-widget-small-cut-min.png" alt="Join the Legendary Inner Circle" class="conditional-banner-small"></a>
<!-- Second Banner -->
<a href="https://www.facebook.com/groups/chucksmastermindgroup/" target="_blank" rel="noopener noreferrer"><img src="/media/mastermind-widget-small-cut-min.png" alt="Join Our Facebook Mastermind Group" class="conditional-banner-small"></a>
<!-- Third Banner -->
<a href="https://www.facebook.com/OfficialMyOnlineStartup/" target="_blank" rel="noopener noreferrer"><img src="/media/stayupdated-widget-small-cut-min.png" alt="Stay Updated" class="conditional-banner-small"></a>
[/mos_if_level]
<!-- END: Only Legendary and admins will see these banners -->
```

## 4. Edit the code
The code contains 3 blocks, with 3 images in each block. It looks something like this:
```html
<!-- Only free members will see this -->
<a><img>First Image</a>
<a><img>Second Image</a>
<a><img>Third Image</a>

<!-- Only Partners will see this -->
<a><img>First Image</a>
<a><img>Second Image</a>
<a><img>Third Image</a>

<!-- Only Legendary and admin will see this -->
<a><img>First Image</a>
<a><img>Second Image</a>
<a><img>Third Image</a>
```
To change a banner, you need to:
1. Change the link (if you want the link to change)
2. Change the image

### Changing a link:
1. Go to the block you want to edit (Free Member, Partner or Legendary)
2. Find the banner you want to edit. Each banner starts with `<a href=...`
3. Find the part where it says `href="/some-link"` and replace the part inside the quotes
> Note: the links won't have `www.myonlinestartup.com` in it, because that part is omitted. You should ommit it too. So instead of `www.mos.com/partner` you should just insert `/partner` (include the opening slash)

### Changing an image:
1. Go to the block you want to edit (Free Member, Partner or Legendary)
2. Find the banner you want to edit. Each banner starts with `<a href=...`
3. Find the part where it says `<img src="/media/...`
4. Replace the link in the quotes with the link you copied down when you Uploaded the images
> Note: the links won't have `www.myonlinestartup.com` in it, because that part is omitted. You should ommit it too. So instead of `www.mos.com/partner` you should just insert `/partner` (include the opening slash)
