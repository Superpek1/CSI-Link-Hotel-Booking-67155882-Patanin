# CSI-Link Hotel Booking System

ระบบจองห้องพักออนไลน์สำหรับโรงแรม CSI-Link Hotel พัฒนาเพื่อตอบสนองความต้องการของผู้ใช้งานทั้ง 4 ส่วน ได้แก่ Customer, Receptionist, Manager และ System

---

## 1. System Architecture (Mermaid Diagram)

```mermaid
graph TD
    A[Customer / Receptionist / Manager] -->|ใช้งานผ่าน| B(Web App / Frontend)
    B --> C{API Gateway}
    C -->|จัดการการจอง| D[Booking Service]
    C -->|จัดการห้องพัก| E[Room Management Service]
    C -->|จัดการผู้ใช้| F[User Service]
    D --> G[(Hotel Database)]
    E --> G
    F --> G