SCRATCH

# Running Docker container locally  
    docker run -p 80:80 -it nginx-app



Pipeline 
- Dockerfile is linted to validate code
- Docker Image is built from the Dockerfile 
- Image is pushed into ECR (Elastic Container Registry)
        - aws ecr get-login-password --region eu-west-1 | docker login --username AWS --password-stdin 908905824345.dkr.ecr.eu-west-1.amazonaws.com
        - docker build -t udacity-capstone-nginx .
        - docker tag udacity-capstone-nginx:latest 908905824345.dkr.ecr.eu-west-1.amazonaws.com/udacity-capstone-nginx:latest
        - docker push 908905824345.dkr.ecr.eu-west-1.amazonaws.com/udacity-capstone-nginx:latest
- Create VPC for running cluster 
        aws cloudformation deploy \
        --no-fail-on-empty-changeset  \ 
        --template-file eks-cluster-creation.yaml \
        --stack-name udacity-capstone-nginx-eks-cluster         
- DeplOY EKS Cluster  
    
- EKS Cluster 