# Mandatory Configuration - Cấu hình Bắt Buộc

## 🔒 Locked Versions - Các Version Bị Khóa

### Core Dependencies

| Dependency | Version | Rationale |
|------------|---------|----------|
| **Kotlin** | `2.2.0` | Version ổn định với Compose Compiler mới nhất |
| **KSP** | `2.2.0-2.0.2` | Tương thích hoàn hảo với Kotlin 2.2.0 |
| **Hilt** | `2.56` | Version ổn định, tránh các bug trong version mới hơn |

## 🚫 Enforcement Rules - Quy Tắc Thực Thi

### STRICT MODE
- ❌ **NGHIÊM CẤM** thay đổi các version này mà không có approval
- ✅ **BẮT BUỘC** kiểm tra version trước khi build
- ✅ **BẮT BUỘC** test compatibility khi có thay đổi

### Configuration Files
- `gradle/libs.versions.toml` - Main version catalog
- `.project-identity` - Project configuration enforcement

## ⚠️ Common Issues Prevention

### Known Problems
1. **Hilt version mới** có thể gây conflict với KSP
2. **Kotlin version không match** có thể gây compilation error  
3. **KSP version không tương thích** có thể gây annotation processing failure

### Prevention Measures
1. ✅ Lock version trong `libs.versions.toml`
2. ✅ Document trong `.project-identity`
3. ✅ Setup CI/CD validation

## 🔧 How to Validate - Cách Kiểm Tra

### Before Build
```bash
# Kiểm tra version hiện tại
grep -E "(kotlin|ksp|hilt)" gradle/libs.versions.toml

# Expected output:
kotlin = "2.2.0"
ksp = "2.2.0-2.0.2"  
hilt = "2.56"
```

### Build Validation
```bash
# Clean build để đảm bảo không có cache issues
./gradlew clean build
```

## 📋 Change Request Process

Nếu cần thay đổi version:

1. **Tạo issue** với lý do chi tiết
2. **Test thoroughly** trên branch riêng
3. **Update documentation** trong `.project-identity`
4. **Get approval** từ team lead
5. **Update** cả hai files cùng lúc:
   - `gradle/libs.versions.toml`
   - `.project-identity`

## 🎯 Benefits - Lợi Ích

- ✅ **Stability** - Tránh các lỗi không mong muốn
- ✅ **Consistency** - Đồng nhất trong team
- ✅ **Predictability** - Build results có thể dự đoán được
- ✅ **Debugging** - Dễ dàng troubleshoot khi có vấn đề

---

> **Note**: File này được tự động tạo và sync với `.project-identity`. 
> Mọi thay đổi cần được reflect trong cả hai nơi.