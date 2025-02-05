# VBA Project Guide

This directory contains all **VBA-related scripts, modules, and data** for structured development.

## 📂 Project Structure

```
📂 VBA_Project/
│── 📂 Modules/            # Contains VBA modules
│   │── Main.bas           # Main execution script
│   │── Utils.bas          # Utility functions
│   │── ErrorHandler.bas   # Centralized error handling
│── 📂 Forms/              # UserForms for UI components
│── 📂 Data/               # Sample input data files
│── README.md              # VBA-specific documentation
```

## 📌 **Modules and Usage**

### **1. Main.bas (Entry Point)**
```vba
Option Explicit

' =============================================
' Module: Main
' Purpose: Entry point for the VBA application
' Author: Joseph
' Date: 2025-02-05
' =============================================

Sub RunMain()
    ' Main execution logic here
    Debug.Print "Executing Main VBA script..."
End Sub
```

### **2. Utils.bas (Helper Functions)**
```vba
Option Explicit

' =============================================
' Module: Utils
' Purpose: Contains reusable utility functions
' Author: Joseph
' Date: 2025-02-05
' =============================================

' Function to get the last used row in a worksheet
Function GetLastRow(ByVal ws As Worksheet, ByVal col As Integer) As Long
    On Error Resume Next
    GetLastRow = ws.Cells(ws.Rows.Count, col).End(xlUp).Row
    On Error GoTo 0
End Function
```

### **3. ErrorHandler.bas (Error Management)**
```vba
Option Explicit

' =============================================
' Module: ErrorHandler
' Purpose: Centralized error handling
' Author: Joseph
' Date: 2025-02-05
' =============================================

Sub HandleError()
    MsgBox "Error " & Err.Number & ": " & Err.Description, vbCritical, "Error Occurred"
    Err.Clear
End Sub
```

## ✅ Professional VBA Coding Standards

- **Use `Option Explicit`** in every module.
- **Follow modular structure** with clear separation of concerns.
- **Comment functions** properly to explain functionality.

---
Designed for **clean, structured, and maintainable VBA development** 🚀.
