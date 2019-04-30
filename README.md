# 黄历和日历
黄历和日历
## Requirement

 - PHP >=5.4
 
  ## 用法
```php
  
     $huangli=Hunagli::date('2019-04-30');
         $res = $huangli->getLunarByBetween();
         $res['gongli'] = $huangli->dateTime->format('Y-m-d');
         $res['week'] = Hunagli::getWeekChs($huangli->dateTime->getTimestamp());
         //24节气
         $res['jieqi'] = $huangli->getJieQi();
         $jieQiList = $huangli->getAllJieQi($huangli->dateTime->format('Y'));
         //方位
         $res['position'] = $huangli->getPosition();
         //八门方位
         $res['bamen'] = $huangli->getBaMenPosition();
         $res['peng_zu'] = $huangli->getPengZuBaiJi();
         //建除十二神
         $res['jianchu'] = $huangli->getJianChu();
         //今日合害
         $res['hehai'] = $huangli->getTodayHeHai();
         //纳音
         $res['na_yin'] = $huangli->getNayin();
         //星宿
         $res['xing_su'] = $huangli->getXingSu();
         //空亡
         $res['kong_wang'] = $huangli->getKongWang();
         //值日
         $res['zhi_ri'] = $huangli->getZhiRi();
         //三煞
         $res['san_sha'] = [
             'y' => $huangli->getSanSha($res['jinian']['y'][1]),
             'm' => $huangli->getSanSha($res['jinian']['m'][1]),
             'd' => $huangli->getSanSha($res['jinian']['d'][1]),
         ];
         //星座
         $res['xing_zuo'] = $huangli->getXingZuo();
         //吉凶宜忌
         $res['yi_ji'] = $huangli->getJiXiong();
         //胎神
         $res['tai_shen'] = $huangli->getTaiShen();
         //时辰详情
         $res['h_detail'] = $huangli->getHourDetail();
``` 