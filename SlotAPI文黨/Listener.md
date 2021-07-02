## Class  EventSelector

* 各類事件監聽添加,呼叫監聽

> 繼承 :
>
> >  <font color="MediumSpringGreen">Class EventOutput ( )</font> 
> >
> > > <font color="HotPink">interface  IEventSelector ( )</font>
> > >
> > > > 以綁定事件名稱 
> > > >
> > > > >* server 事件 <font color="MediumSpringGreen">static</font>  [Class ServerListenerParameter](#ServerListenerParameter )
> > > > >
> > > > >* game 事件 <font color="MediumSpringGreen">static</font>  [Class GameListenerParameter](# GameListenerParameter)



* [gameEventSelector](#gameEventSelector) : 遊戲監聽橋接器

* [serverEventSelector](#serverEventSelector) : responese 回傳橋接器

* [gameEventListener(  )](#gameEventListener) : 遊戲內事件監聽

* [serverEventListener(  )](#serverEventListener) : servlet事件監聽

* [event (  )](#event) : 監聽事件輸出,呼叫已綁定的監聽者

  

#### 以綁定事件 : 

##### Sever :  Class ServerListenerParameter ( )

* <font color="MediumSpringGreen">BET_RESULT </font>: 一般獲獎回傳
* <font color="MediumSpringGreen">FREE_SPIN_RESULT </font>: 免費模式獲獎
* <font color="MediumSpringGreen">CAN_PLAY_GAME </font>: 底層進遊戲 通知Loading頁面 可以顯示主遊戲場景
* <font color="MediumSpringGreen">GET_GAME_HISTORY_RESULT </font>:  獲取遊戲歷史結果
* <font color="MediumSpringGreen">GET_HISTORY_DETAIL_RESULT </font>: 獲取遊戲祥單
* <font color="MediumSpringGreen">GROUP_ID </font>: 該局遊戲序號
* <font color="MediumSpringGreen">TABLE_INFO </font>: 進入遊戲後初始資訊
* <font color="MediumSpringGreen">UPDATE_POINTS </font>: 更新玩家金額
* <font color="MediumSpringGreen">WARNING </font>: 各種錯誤訊息





##### Game: GameListenerParameter ( )

* TODO









### Function

------





<font id = "gameEventSelector" color="Yellow">***gameEventSelector***</font>

<table>
  <tr>
    <th colspan="2">
        遊戲監聽橋接器
      </th>
  </tr>
  <tr>
    <td colspan="1">
        <font color="MediumSpringGreen">static readonly</font>
        cc.EventTarget 
      </td>
  </tr>
</table>




<font id = "serverEventSelector" color="Yellow">***serverEventSelector***</font>

<table>
  <tr>
    <th colspan="2">
        responese回傳橋接器
      </th>
  </tr>
  <tr>
    <td colspan="1">
        <font color="MediumSpringGreen">static readonly</font>
        cc.EventTarget 
      </td>
  </tr>
</table>




<font id = "gameEventListener" color="Yellow">***gameEventListener***</font>

| 遊戲內事件監聽                                               |
| ------------------------------------------------------------ |
| <font color="MediumSpringGreen">static</font>        Function (<font color="Orange">event,callback</font>) |
| event (事件名稱) : string   ,   callback (要做的事) : Function |





<font id = "serverEventListener" color="Yellow">***serverEventListener***</font>

| servlet事件監聽                                              |
| ------------------------------------------------------------ |
| <font color="MediumSpringGreen">static</font>        Function (<font color="Orange">event,callback</font>) |
| event (事件名稱) : string   ,   callback (要做的事) : Function |





<font id = "event" color="Yellow">***event***</font>

| 監聽事件輸出,呼叫已綁定的監聽者                              |
| ------------------------------------------------------------ |
| <font color="MediumSpringGreen">static</font>        Function (<font color="Orange">Selector,eventName,method?</font>) |
| Selector (橋接器) : cc.EventTarget                           |
| eventName (事件名稱) : string                                |
| method ? ( return給監聽者的參數 ) : Any                      |