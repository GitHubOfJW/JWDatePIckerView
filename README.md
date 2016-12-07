# JWDatePickerView


====介绍：本控件是为了扩展苹果的日历控件而编写，

swift版本提供 10 个模式
```
public enum JWDatePickerMode:Int{

case dateAndTime// 年月日  时  分  秒
case dateAndHour// 年月日  时
case dateAndTimeRYear// 月日 时 分 秒
case time//  时 分 秒
case timeRSecond//  时 分
case date// 年   月   日
case dateAddHour// 年 月 日  时
case dateAndTimeRSecond// 年月日  时  分
case dateAndTimeRYearAndSecond// 月日  时  分   3
case dateAndTimeForAllComponent// 年 月  日  时  分 秒
}
```

OC版本主要提供8 个模式
```
JWDatePickerMode_DateAndTime,// 年月日 时 分 秒 
JWDatePickerMode_DateAndTimeRYear,//  月日 时 分 秒  
JWDatePickerMode_Time,// 时分秒   
JWDatePickerMode_TimeRSecond,//时分
JWDatePickerMode_Date,// 年月日  
JWDatePickerMode_DateAddHour,// 年 月 日 时  
JWDatePickerMode_DateAndTimeRSecond,// 年月日  时 分  
JWDatePickerMode_DateAndTimeRYearAndSecond//月日 时 分   
```


====介绍：通过代理指定单位
```
-(NSString *)datePickerView:(JWDatePickerView *)datePickerView unitForCalendarUnit:(NSCalendarUnit)calendarUnit
{

switch (calendarUnit) {
case NSCalendarUnitYear:
return @"年";
break;
case NSCalendarUnitMonth:
return @"月";
break;
case NSCalendarUnitDay:
return @"日";
break;
case NSCalendarUnitHour:
return @"时";
break;
case NSCalendarUnitMinute:
return @"分";
break;
case NSCalendarUnitSecond:
return @"秒";
break;
default:
break;
}
return @" ";
}
```
====演示
<br>
![](https://github.com/GitHubOfJW/JWDatePickerView/blob/master/Source/PickerView.gif)  
