# Azure Composite SLA  

## Overview  
Understanding how to calculate the **Composite SLA** for applications using multiple Azure services.  

---  

## Key Points  

### 1. **Individual Service SLAs**  
   - Each Azure service has its own **Service Level Agreement (SLA)**, which defines its **availability percentage**.  
   - Example SLAs:  
     - **Azure App Service**: **99.95%**  
     - **Azure SQL Database**: **99.99%**  

### 2. **Calculating Composite SLA**  
   - When an application depends on multiple services, the **overall SLA** is calculated using:  

   **Formula:**  
   \[
   \text{Composite SLA} = (\text{SLA of Service A}) \times (\text{SLA of Service B})
   \]

   **Example Calculation:**  
   - **Azure App Service SLA** = **99.95%**  
   - **Azure SQL Database SLA** = **99.99%**  
   - **Composite SLA**:  
     \[
     99.95\% \times 99.99\% = 99.94\%
     \]
   - The final **availability percentage** is lower than the SLA of any individual service.  

### 3. **Improving Composite SLA**  
   - Strategies to enhance overall application availability:  
     - **Redundancy**: Deploy services across **multiple Availability Zones** or **Regions**.  
     - **Load Balancing**: Distribute traffic across multiple instances.  
     - **Fault Tolerance**: Implement **database replication** and **failover strategies**.  

---  

## Summary  
- **Composite SLA** represents the combined availability of multiple Azure services.  
- It is **calculated by multiplying** the SLAs of individual services.  
- The **overall SLA is lower** than any single service SLA.  
- **High availability strategies** can improve composite SLA reliability.  
