#kubeflow-node-red
cd example 
sudo ./run.sh 1.connect-kubeflow
點選 install dependency方塊安裝必要軟件
拖曳bagging方塊
執行bagging方塊
#kubeflow-pipline
cd bagging
docker build -t lance410247/kubeflow:bagging_v3  . -f Dockerfile
#推送到Docker Hub
docker push lance410247/kubeflow:bagging_v2
cd ..
python pipline2.py
