#### 生成 dist 目录用于博客发布

hugo --gc --minify --baseURL "https://blog.hzau.top/" -d dist --cleanDestinationDir

#### 生成 public 目录用于本地预览

hugo serve -D
