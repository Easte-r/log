## 引入的库
 - xgplayer
 - vue-awesome-swiper
 

const player = new Player({
	id: 'video',
	url: '//abc.com/test.mp4',
});

import { swiper, swiperSlide } from 'vue-awesome-swiper';



## 编写文件
// type.d.ts
```
declare module 'xgplayer' {
	
	class Player {
		constructor(option: {id: string, url: string});
	}
}

declare module 'vue-awesome-swiper' {
	let swiper: any;
	let swiperSlide: any;
}
```


## 假如要为一个js类编写声明文件

function AA(){
}
AA.prototype.init = function(){}

```
declare class AA {
  construcotr()
  
  init: () => void
}
```
