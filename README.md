# JWAVPlayer
自定义简单的支持横屏竖屏切换的Avplayer
```javascript     
    JWPlayer*player=[[JWPlayer alloc]initWithFrame:CGRectMake(0, 0, 414,9*414/16)];
    [player updatePlayerWith:[NSURL URLWithString:@"http://120.25.226.186:32812/resources/videos/minion_01.mp4"]];
    [self.view addSubview:player];
```
## 第二种用法
```javascript
    JWPlayer*player=[[JWPlayer alloc]initWithFrame:CGRectMake(0, 0, 414,9*414/16)];
    [player updatePlayerWith:[NSURL URLWithString:@"http://120.25.226.186:32812/resources/videos/minion_01.mp4"]];
    [player showInSuperView:self.view andSuperVC:self];
```

## 在tableview上的使用
```python
 UITableViewCell*cell=[tableView dequeueReusableCellWithIdentifier:@"cell"];
 if (!cell) {
 cell=[[UITableViewCell alloc]initWithStyle:UITableViewCellStyleDefault reuseIdentifier:@"cell"];
 cell.contentView.userInteractionEnabled=YES;
 }
 UIView*view=[[UIView alloc]initWithFrame:CGRectMake(0, 0, 414, 9*414/16)];
 [cell.contentView addSubview:view];
 JWPlayer*player=[[JWPlayer alloc]initWithFrame:CGRectMake(0, 0, 414,9*414/16)];
 [player updatePlayerWith:[NSURL URLWithString:@"http://120.25.226.186:32812/resources/videos/minion_01.mp4"]];
 [player showInSuperView:view andSuperVC:self];

```
![img](https://github.com/JarvisHot/JWAVPlayer/blob/master/JWPlayer/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202016-11-15%20%E4%B8%8B%E5%8D%882.05.33.png)
