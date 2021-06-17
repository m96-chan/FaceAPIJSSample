# FaceAPIJSSample
example for face-api.js

# what is this?

this system detect your face and register your arrival at work.

# how to work!
 
## 1. put your face photo into photos/me.

```
const meLabeled = await loadLabeledFaceDescriptors("me", ['photos/me/1.png']);
```

This is a code loading your face.  
If you have a lot of your face photos, you should put photos into the folder.
and change the code.

like this.

photos/me/hoge.png  
photos/me/fuga.jpg  
photos/me/piyo.jpg  

```
const meLabeled = await loadLabeledFaceDescriptors("me", [
    'photos/me/hoge.png',
    'photos/me/fuga.jpg',
    'photos/me/piyo.jpg',
]);
```

## 2. create plugins/stamp.js and implements stampAttendance

### why do not have this file?
> This is because a diligence and indolence system varies according to companies.

### why do not have sample.
> This is because my company OSS activity is bad when it comes out.  
> I am very sorry.

### poor sample...
```
async function stampAttendance() {
    const url = `your company api url?`;
    const popup = window.open(url, "popup", "width=800,height=640");
    setTimeout(() => popup.close(), 3000);
}
```

# develop execute

1. run `npm install`
1. install [live-server](https://www.npmjs.com/package/live-server)
1. run live-server

# release

tobe soon...

## attention  
you must allow　access the video

