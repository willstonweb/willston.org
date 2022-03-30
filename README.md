# willston.org

## Development

`hugo server up`

## Converting images

We convert images to `.webp` because they weigh less than `.jpg` images and make
them as small as possible. We use [ImageMagick](https://imagemagick.org/) with
the following command: `convert image.jpg -resize x400 image.webp`r
