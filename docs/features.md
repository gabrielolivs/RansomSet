## Ransomware Features - System Call Analysis

In this section, we present the 240 features extracted from system call logs, which are essential for analyzing the behavior of ransomware. Each feature corresponds to a specific system call made during the execution of the ransomware samples. These features help in characterizing the interactions of the malware with the underlying operating system, providing valuable insights for detection and classification.

The table below lists each feature, along with a brief description of its role in the analysis and the relevant source for the explanation.

| **Category**               | **Features**                                                                                                                                                      |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **File Access**            | NtCreateFile, NtReadFile, NtWriteFile, NtClose, CreateDirectoryW, GetFileAttributesW, GetFileSize, SetFilePointer, NtOpenFile, DeleteFileW, GetFileSizeEx, GetFileInformationByHandleEx, SetFileTime, SetFileAttributesW, CopyFileW, CopyFileA, RemoveDirectoryA, MoveFileWithProgressW, SetEndOfFile, FindResourceW, FindResourceExW |
| **Process Manipulation**   | NtAllocateVirtualMemory, NtFreeVirtualMemory, NtCreateSection, NtMapViewOfSection, NtTerminateProcess, NtSuspendThread, NtOpenProcess, NtOpenThread, CreateProcessInternalW, Process32FirstW, Process32NextW, Module32FirstW, Module32NextW, Thread32First, Thread32Next |
| **Registry Keys**          | NtOpenKey, NtQueryValueKey, RegOpenKeyExA, RegOpenKeyExW, RegQueryValueExW, RegCloseKey, RegSetValueExA, RegSetValueExW, RegDeleteValueW, RegDeleteKeyW, RegEnumKeyExW, RegEnumValueW, RegQueryInfoKeyW, RegQueryInfoKeyA |
| **Memory and System**      | GetSystemWindowsDirectoryW, GetSystemDirectoryW, NtQuerySystemInformation, NtDuplicateObject, GlobalMemoryStatusEx, GetNativeSystemInfo, GetSystemInfo, GetSystemMetrics, GetComputerNameW, GetUserNameW, GetDiskFreeSpaceExW, GlobalMemoryStatus, NtReadVirtualMemory |
| **Network & Communication**| socket, listen, connect, accept, ioctlsocket, send, recv, WSAStartup, WSASocketW, bind, setsockopt, getsockname, WSASend, WSARecv, closesocket, InternetOpenA, InternetConnectA, HttpOpenRequestA, HttpQueryInfoA, InternetReadFile, InternetCloseHandle, InternetCrackUrlW, InternetQueryOptionA, InternetSetOptionA, InternetOpenUrlW |
| **Process Execution & Control**| NtQueryInformationFile, NtSetInformationFile, NtCreateThreadEx, SetWindowsHookExW, NtCreateKey, NtDeleteKey, SetStdHandle, RegisterHotKey |
| **Cryptography & Security**| CryptAcquireContextA, CryptCreateHash, CryptHashData, CryptExportKey, CryptDecrypt, CryptGenKey, CryptEncrypt, CertOpenStore, CryptDecodeObjectEx, CertControlStore, EncryptMessage, DecryptMessage |
| **Window Interface & Management**| FindWindowW, FindWindowExW, GetCursorPos, GetKeyState, MessageBoxTimeoutW, LoadStringW, DrawTextExW, EnumWindows |
| **Services & Control**     | OpenSCManagerW, OpenServiceW, ControlService, DeleteService, StartServiceW, SendNotifyMessageW |
| **Other Functions**        | UuidCreate, GetAdaptersInfo, GetAdaptersAddresses, GetBestInterfaceEx, GetVolumeNameForVolumeMountPointW, GetVolumePathNamesForVolumeNameW |
| **File Access (cont.)**    | NtCreateFile, NtReadFile, NtWriteFile, NtClose, CreateDirectoryW, GetFileAttributesW, GetFileSize, SetFilePointer, NtOpenFile, DeleteFileW, GetFileSizeEx, GetFileInformationByHandleEx, SetFileTime, SetFileAttributesW, CopyFileW, CopyFileA, RemoveDirectoryA, MoveFileWithProgressW, SetEndOfFile, FindResourceW, FindResourceExW |
| **Memory & Thread Management** | NtCreateMutant, NtSuspendThread, NtOpenThread, NtCreateSection, NtMapViewOfSection, NtDuplicateObject, GetSystemMetrics |
| **Network & Protocols**     | WSAStartup, WSASocketW, bind, setsockopt, getsockname, WSASend, WSARecv, closesocket, InternetOpenA, InternetConnectA, HttpOpenRequestA, HttpQueryInfoA |
| **File Handling**           | SetFilePointer, NtQueryInformationFile, NtOpenFile, SetFileAttributesW, RemoveDirectoryA, LookupAccountSidW, NtDeviceIoControlFile |
| **Memory & Resource Management** | GlobalMemoryStatusEx, NtProtectVirtualMemory, NtReadVirtualMemory, NtQuerySystemInformation, NtDuplicateObject |

