# Pathfinder MPC: Charting the Way - Virtual Expo 2025

Welcome to **Pathfinder MPC**, a project exploring the future of autonomous navigation through a simulated Mars rover. This repository showcases a comparative study between **Pure Pursuit Control (PPC)** and **Model Predictive Control (MPC)** using MATLAB simulations. The objective? To identify the best control logic for autonomous rover navigation in dynamic, obstacle-laden 2D environments.

🔗 [GitHub Repository](https://github.com/galava-shubhang/MPC-Rover)

---

## Project Abstract

Autonomous navigation is crucial for the next generation of planetary rovers. This project simulates two control strategies—**Pure Pursuit Control (PPC)** and **Model Predictive Control (MPC)**—to guide a rover along a path while avoiding static and dynamic obstacles.  

- **PPC**: Lightweight and simple but struggles in complex terrains.  
- **MPC**: Robust, adaptive, and precise, albeit computationally intensive.

By evaluating these methods on path tracking accuracy, computational cost, and obstacle avoidance, this project lays the groundwork for smarter space exploration.

---

## Aim

To compare **PPC** and **MPC** for rover navigation in a 2D simulated environment by evaluating:

- Path tracking accuracy  
- Obstacle avoidance  
- Computational efficiency  
- Scalability for complex environments  

---

## Technologies & Models Used

- **MATLAB** – Simulation environment
- **Pure Pursuit Control (PPC)** – Geometric path tracking algorithm
- **Model Predictive Control (MPC)** – Optimization-based predictive controller
- **Bicycle Model (BM)** – Kinematic model for vehicle motion

---

## Methodology

### 1. **PPC Implementation**
- Path defined as a smooth sinusoidal curve
- Static circular obstacles included
- Uses a lookahead point to calculate steering angle
- Lightweight but not robust to dynamic or tight obstacle navigation

### 2. **MPC Implementation**
- State vector: `[x, y, θ, v]`
- Uses a prediction horizon to forecast motion
- Solves an optimization problem at each time step with MATLAB’s `fmincon`
- Penalizes deviation from path, speed spikes, steering changes, and proximity to obstacles
- Adaptable to dynamic obstacles and high-precision tracking

### 3. **Bicycle Model**
- Models the rover with a simplified 2-wheel representation
- Captures essential dynamics (position, orientation, velocity, steering angle)

---

## Results

Both controllers were tested in identical environments. The simulations visually demonstrate:

- **PPC**: Simpler, faster, but less effective at obstacle avoidance  
- **MPC**: Smoother paths, higher accuracy, handles dynamic scenarios better  

### MPC Demo with Dynamic Obstacles
> [View simulation code](https://github.com/galava-shubhang/MPC-Rover/blob/main/MPC%20Model%20with%20Dynamic%20Obstacles.pdf)
### PPC Demo with Dynamic Obstacles
> [View simulation code](https://github.com/galava-shubhang/MPC-Rover/blob/main/PPC%20Model.pdf)


---

## 📚 Literature & References

1. Model Predictive Control - A Review and Future Directions  
2. Pure Pursuit Path Tracking - Adaptive Lookahead  
3. Control Systems in Autonomous Robotics  
4. The Bicycle Model for Kinematic Path Tracking

---

## 📁 Folder Structure

```bash
MPC-Rover/
├── MPC%20Model%20with%20Dynamic%20Obstacles.pdf
├── MPC%20Model%20Demo.mp4
├── PPC%20Model.pdf
├── PPC%20Model%20Demo.mp4
├── README.md
