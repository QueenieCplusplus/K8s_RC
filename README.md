# K8s_RC
Replication Controller &amp; Controller Manager

能定義 Pod 抄本數量。在 Master 內透過 RC 定義在 Controller Manager 實現了 Pod 建立、監聽、啟動、停止其生命週期。

# Replica 示意圖


           etcd (log) 
                    
                 |
                 |
                _|______________                   
               |                |----- get ---  __ Node___               _ anotherNode_ 
               | Core API (Auth)|----- list --- |Kuberlet|---k8sProxy---|   Kuberlet   |
               |________________|               ----------               --------------
                   |           |
                   |           |
                   |           |
                   |           
                   |       Resorces Controll (cotains Node Controller, Replication Controller)
                   |
                   |
                       
              Event Listener (by Scheduler)




