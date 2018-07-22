### redis
import redis
conn = redis.Redis() # デフォルトポートは6379

#### 全てのkey
conn.keys('*')

#### 値を入れる/取得する
conn.set('secret',"hei!") #文字列
conn.set('secret',24) #整数
conn.set('secret','101.5') #少数
conn.setnx('secret','value') #値がない時だけ挿入
conn.getset('secret','value') #元の値を取得した後挿入
conn.getrange('secret',-4,-1) #範囲指定で値を取得
conn.setrange('secret',0,'value') #値を入れる
conn.mset({}) #複数キーの同時入力
conn.mget([]) #複数キーの同時取得
conn.delete('secret') #削除
