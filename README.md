# ELK
some ELK concepts

# replica vs shard
  Replica : دقیقا یک کپی از داده قبلی است
  
  Shard : به فرض اگر داده کلا 1 ترابایت باشد و 4 شرد داشته باشیم هر شرد 256 گیگ از دیتا را خواهد داشت.
  ![image](https://github.com/ehsanDadashi/ELK/assets/29996315/09124616-468a-43dd-8eb5-43b62ed181eb)
# ELK Cluster
ELK cluster node rolls:

    Master : cluster management
    وظایفی مانند ایجاد/حذف ایندکس ها مدیریت shard allocation و حفظ وضعیت کلی کلاستر  
    Data : 
    ذخیره و مدیریت index ها و انجام عملیات search و analyze  
    Ingest : process data before indexing (change format , parsing , …)


![image](https://github.com/ehsanDadashi/ELK/assets/29996315/9dff2b69-f7e2-4e18-9fed-832f7518f041)
    Coordinate : it is a data less node that receive data and send it to other node
    
    Machine learning : it manage and runs machine learning process
    
    Voting only : it is a node that just vote about choose master node and it is not be able to be master

![image](https://github.com/ehsanDadashi/ELK/assets/29996315/97fcceb7-13c0-40bb-a8d2-25d8c7cc86b6)

    Remote cluster : it is a client that will be used to connect to elasticsearch cluster. It will be use to cross cluster search

