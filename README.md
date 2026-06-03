# DrunkenDreamDriver
禁止用于非法用途，违者必究  
免责声明：使用者所做违规事项，均与开发者无关，将由违法者本人承担其所有法律责任  
Q群：1036733613  
使用说明：  
需要安装驱动，demo.cpp内为驱动完全示例展示  
功能如下：  
BOOL 安装驱动(ULONG 内部验证码, std::string 卡密);
std::vector<int> 获取本机可用通讯方式(); //返回的排序是按照通讯速度从快到慢排序的  且上本机可用的方式
DWORD 随机可用通讯方式(); //随机在可用通讯列表里随机选择通讯方式
DWORD 极速_随机可用通讯方式();//随机在可用通讯列表里取随机选择最快的几个通讯方式
DWORD 获取通讯速度(int 要查询的通讯方式);//返回的是纳秒（指定通讯方式的测试速度）
BOOL 卸载驱动();
BOOL 设置进程ID(ULONG ProcessID);
ULONG64 取模块地址(const char* ModuleName, DWORD 通讯方式 = 6);
BOOL 保护进程(ULONG ProcessID, DWORD 通讯方式 = 6);
BOOL 保护进程Pro(ULONG ProcessID, DWORD 通讯方式 = 6);
BOOL 保护进程Pro_清空保护列表(DWORD 通讯方式 = 6);
BOOL 进程提权Pro(ULONG ProcessID, DWORD 通讯方式 = 6);
BOOL 进程提权Pro_清空提权列表(DWORD 通讯方式 = 6);
BOOL 保护文件(const char* FilePath, DWORD 通讯方式 = 6);
BOOL 修改进程ID(ULONG 原PID, ULONG 改后PID, DWORD 通讯方式 = 6);
BOOL 还原进程ID(DWORD 通讯方式 = 1);
BOOL 创建进程(LPCWSTR FilePath, DWORD 父进程ID, DWORD 通讯方式 = 6);
BOOL 杀死进程(ULONG ProcessID, DWORD 通讯方式 = 6);
BOOL 进程提权(ULONG ProcessID, DWORD 通讯方式 = 6);
BOOL 进程降权(ULONG ProcessID, DWORD 通讯方式 = 6);
BOOL 内存注入(ULONG ProcessID, const std::vector<BYTE>& DLL数据, DWORD 通讯方式 = 6);
BOOL 远程注入(ULONG PID, PCWSTR DLLPath, DWORD 通讯方式 = 6);
BOOL 远程CALL(ULONG PID, ULONG64 Address, DWORD 通讯方式 = 6);
BOOL 修改父窗口(HWND 子窗口, HWND 新父窗口, DWORD 通讯方式 = 6);
BOOL 修改窗口样式(HWND 窗口句柄, int nIndex, LONG_PTR dwNewLong, DWORD 通讯方式 = 6);
BOOL 修改内存属性_禁止访问(ULONG PID, ULONG64 MemAddress, ULONG64 RegionSize, DWORD 通讯方式 = 6);
BOOL 修改内存属性_只读(ULONG PID, ULONG64 MemAddress, ULONG64 RegionSize, DWORD 通讯方式 = 6);
BOOL 修改内存属性_可读可写(ULONG PID, ULONG64 MemAddress, ULONG64 RegionSize, DWORD 通讯方式 = 6);
BOOL 修改内存属性_可执行(ULONG PID, ULONG64 MemAddress, ULONG64 RegionSize, DWORD 通讯方式 = 6);
BOOL 修改内存属性_可读可执行(ULONG PID, ULONG64 MemAddress, ULONG64 RegionSize, DWORD 通讯方式 = 6);
BOOL 修改内存属性_可读可写可执行(ULONG PID, ULONG64 MemAddress, ULONG64 RegionSize, DWORD 通讯方式 = 6);

BOOL 强删文件(const char* FilePath, DWORD 通讯方式 = 6);
ULONG64 申请内存(ULONG 申请目标PID, ULONG 申请长度, DWORD 通讯方式 = 6);
BOOL 释放内存(ULONG 释放目标PID, ULONG64 释放内存地址, DWORD 通讯方式 = 6);
BOOL 隐藏进程(ULONG ProcessID, DWORD 通讯方式 = 6);
BOOL 暂停进程(ULONG PID, DWORD 通讯方式 = 6);
BOOL 恢复进程(ULONG PID, DWORD 通讯方式 = 6);
BOOL 暂停线程(HANDLE ThreadHandle, PULONG 先前挂起计数地址 = NULL, DWORD 通讯方式 = 6);
BOOL 恢复线程(HANDLE ThreadHandle, PULONG 先前挂起计数地址 = NULL, DWORD 通讯方式 = 6);;
void 无畏契约Dump();
DWORD 取进程ID(const char* processName);
DWORD 内核_取进程ID(const char* processName, DWORD 通讯方式 = 6);
BOOL 修改窗口标题(LPCWSTR 窗口标题名, LPCWSTR 修改后窗口标题);
BOOL 窗口隐藏(HWND hwnd, DWORD 通讯方式 = 6);
BOOL 保护窗口Pro(HWND hwnd, DWORD 通讯方式 = 6);
BOOL 保护窗口Pro_清空保护列表(DWORD 通讯方式 = 6);
BOOL 调试器进程Pro(ULONG DebugProcessId, DWORD 通讯方式 = 6);
BOOL 调试器进程Pro_清空调试器列表(DWORD 通讯方式 = 6);
BOOL 键盘按下(USHORT keyCode, DWORD 通讯方式 = 6);
BOOL 键盘弹起(USHORT keyCode, DWORD 通讯方式 = 6);
BOOL 鼠标左键按下(DWORD 通讯方式 = 6);
BOOL 鼠标左键弹起(DWORD 通讯方式 = 6);
BOOL 鼠标右键按下(DWORD 通讯方式 = 6);
BOOL 鼠标右键弹起(DWORD 通讯方式 = 6);
BOOL 鼠标滚轮按下(DWORD 通讯方式 = 6);
BOOL 鼠标滚轮弹起(DWORD 通讯方式 = 6);
BOOL 鼠标相对移动(LONG dx, LONG dy, DWORD 通讯方式 = 6);
BOOL 鼠标绝对移动(LONG dx, LONG dy, DWORD 通讯方式 = 6);
BOOL 内核_鼠标相对移动(LONG dx, LONG dy, DWORD 通讯方式 = 6);
BOOL 内核_鼠标绝对移动(LONG dx, LONG dy, DWORD 通讯方式 = 6);
BOOL 内核_强制鼠标相对移动(LONG dx, LONG dy, DWORD 通讯方式 = 6);
BOOL 内核_强制鼠标绝对移动(LONG dx, LONG dy, DWORD 通讯方式 = 6);
ULONG64 特征码搜索_只读(ULONG64 起始搜索地址, const std::vector<BYTE>& vCode, DWORD 通讯方式 = 6);
ULONG64 特征码搜索_可读可写(ULONG64 起始搜索地址, const std::vector<BYTE>& vCode, DWORD 通讯方式 = 6);
ULONG64 特征码搜索_可执行(ULONG64 起始搜索地址, const std::vector<BYTE>& vCode, DWORD 通讯方式 = 6);
ULONG64 特征码搜索_可读可执行(ULONG64 起始搜索地址, const std::vector<BYTE>& vCode, DWORD 通讯方式 = 6);
ULONG64 特征码搜索_可读可写可执行(ULONG64 起始搜索地址, const std::vector<BYTE>& vCode, DWORD 通讯方式 = 6);

//漏驱加载
BOOL 漏驱加载开();
BOOL 漏驱加载关();

//MDL读写
ULONG64 MDL_读长整数(uint64_t Address, DWORD 通讯方式 = 6);
DOUBLE MDL_读双浮点(uint64_t Address, DWORD 通讯方式 = 6);
FLOAT MDL_读单浮点(uint64_t Address, DWORD 通讯方式 = 6);
int MDL_读整数(uint64_t Address, DWORD 通讯方式 = 6);
SHORT  MDL_读短整数(uint64_t Address, DWORD 通讯方式 = 6);
BYTE MDL_读字节(uint64_t Address, DWORD 通讯方式 = 6);
vector<BYTE> MDL_读字节数组(uint64_t Address, ULONG MySize, DWORD 通讯方式 = 6);
BOOL MDL_写长整数(uint64_t Address, ULONG64 WriteValue, DWORD 通讯方式 = 6);
BOOL MDL_写双浮点(uint64_t Address, DOUBLE WriteValue, DWORD 通讯方式 = 6);
BOOL MDL_写单浮点(uint64_t Address, FLOAT WriteValue, DWORD 通讯方式 = 6);
BOOL MDL_写整数(uint64_t Address, int WriteValue, DWORD 通讯方式 = 6);
BOOL MDL_写短整数(uint64_t Address, SHORT WriteValue, DWORD 通讯方式 = 6);
BOOL MDL_写字节(uint64_t Address, BYTE WriteValue, DWORD 通讯方式 = 6);
BOOL MDL_写字节数组(uint64_t Address, const std::vector<BYTE>& data, DWORD 通讯方式 = 6);
//附加读写
ULONG64 附加_读长整数(uint64_t Address, DWORD 通讯方式 = 6);
DOUBLE 附加_读双浮点(uint64_t Address, DWORD 通讯方式 = 6);
FLOAT 附加_读单浮点(uint64_t Address, DWORD 通讯方式 = 6);
int 附加_读整数(uint64_t Address, DWORD 通讯方式 = 6);
BYTE 附加_读字节(uint64_t Address, DWORD 通讯方式 = 6);
SHORT 附加_读短整数(uint64_t Address, DWORD 通讯方式 = 6);
vector<BYTE> 附加_读字节数组(uint64_t Address, ULONG MySize, DWORD 通讯方式 = 6);
BOOL 附加_写长整数(uint64_t Address, ULONG64 WriteValue, DWORD 通讯方式 = 6);
BOOL 附加_写双浮点(uint64_t Address, DOUBLE WriteValue, DWORD 通讯方式 = 6);
BOOL 附加_写单浮点(uint64_t Address, FLOAT WriteValue, DWORD 通讯方式 = 6);
BOOL 附加_写整数(uint64_t Address, int WriteValue, DWORD 通讯方式 = 6);
BOOL 附加_写字节(uint64_t Address, BYTE WriteValue, DWORD 通讯方式 = 6);
BOOL 附加_写短整数(uint64_t Address, SHORT WriteValue, DWORD 通讯方式 = 6);
BOOL 附加_写字节数组(uint64_t Address, const std::vector<BYTE>& data, DWORD 通讯方式 = 6);
//内核拷贝读写
ULONG64 内核拷贝_读长整数(uint64_t Address, DWORD 通讯方式 = 6);
DOUBLE 内核拷贝_读双浮点(uint64_t Address, DWORD 通讯方式 = 6);
FLOAT 内核拷贝_读单浮点(uint64_t Address, DWORD 通讯方式 = 6);
int 内核拷贝_读整数(uint64_t Address, DWORD 通讯方式 = 6);
BYTE 内核拷贝_读字节(uint64_t Address, DWORD 通讯方式 = 6);
SHORT  内核拷贝_读短整数(uint64_t Address, DWORD 通讯方式 = 6);
vector<BYTE> 内核拷贝_读字节数组(uint64_t Address, ULONG MySize, DWORD 通讯方式 = 6);
BOOL 内核拷贝_写长整数(uint64_t Address, ULONG64 WriteValue, DWORD 通讯方式 = 6);
BOOL 内核拷贝_写双浮点(uint64_t Address, DOUBLE WriteValue, DWORD 通讯方式 = 6);
BOOL 内核拷贝_写单浮点(uint64_t Address, FLOAT WriteValue, DWORD 通讯方式 = 6);
BOOL 内核拷贝_写整数(uint64_t Address, int WriteValue, DWORD 通讯方式 = 6);
BOOL 内核拷贝_写短整数(uint64_t Address, SHORT WriteValue, DWORD 通讯方式 = 6);
BOOL 内核拷贝_写字节(uint64_t Address, BYTE WriteValue, DWORD 通讯方式 = 6);
BOOL 内核拷贝_写字节数组(uint64_t Address, const std::vector<BYTE>& data, DWORD 通讯方式 = 6);
//CR3读写
ULONG64 CR3_读长整数(uint64_t Address, DWORD 通讯方式 = 6);
DOUBLE CR3_读双浮点(uint64_t Address, DWORD 通讯方式 = 6);
FLOAT CR3_读单浮点(uint64_t Address, DWORD 通讯方式 = 6);
int CR3_读整数(uint64_t Address, DWORD 通讯方式 = 6);
BYTE CR3_读字节(uint64_t Address, DWORD 通讯方式 = 6);
SHORT  CR3_读短整数(uint64_t Address, DWORD 通讯方式 = 6);
vector<BYTE> CR3_读字节数组(uint64_t Address, ULONG MySize, DWORD 通讯方式 = 6);
BOOL CR3_写长整数(uint64_t Address, ULONG64 WriteValue, DWORD 通讯方式 = 6);
BOOL CR3_写双浮点(uint64_t Address, DOUBLE WriteValue, DWORD 通讯方式 = 6);
BOOL CR3_写单浮点(uint64_t Address, FLOAT WriteValue, DWORD 通讯方式 = 6);
BOOL CR3_写整数(uint64_t Address, int WriteValue, DWORD 通讯方式 = 6);
BOOL CR3_写字节(uint64_t Address, BYTE WriteValue, DWORD 通讯方式 = 6);
BOOL CR3_写短整数(uint64_t Address, SHORT WriteValue, DWORD 通讯方式 = 6);
BOOL CR3_写字节数组(uint64_t Address, const std::vector<BYTE>& data, DWORD 通讯方式 = 6);
PVOID 读物理内存(ULONG64 Address, SIZE_T Length, DWORD 通讯方式 = 6);
BOOL 写物理内存(ULONG64 Address, PVOID Buffer, SIZE_T Length, DWORD 通讯方式 = 6);

//文本操作
string 取微云笔记标题(const char* Url);//返回标题
string 取微云笔记内容(const char* Url);//返回全内容
ULONG 取微云笔记标题数值(const char* Url);//返回标题的数值
string 取字符串中间内容(std::string 字符串, std::string 前缀, std::string 后缀);
ULONG 字符串转整数(std::string 字符串);
string 整数转字符串(ULONG 整数);
bool 搜索特定字符串(const std::string& 目标字符串, const std::string& 子字符串);
vector<string> 获取本机登录QQ列表();
//绘制函数
typedef void(*功能回调)(void);
//参数1:类名 参数2:标题名 参数3：要创建的窗口类名 参数4：要创建的窗口名称 参数5:回调 参数6:字体路径 参数7:字体大小 参数8:垂直同步 参数9:菜单样式 0为黑色,1为蓝色，2为白色，3为典雅 4为暗紫色 5为淡蓝色
int 创建绘制窗口(LPCSTR 目标进程类名, LPCSTR 目标进程标题, LPCWSTR 创建窗口类名, LPCWSTR 创建窗口标题, 功能回调 Fun, const char* Fontsname = NULL, float Fonts_size = 17, bool Synclnterval = TRUE, int Menustyle = 3);
void 绘制射线(const float x1, const float y1, const float x2, const float y2, Color color, float thickness);
void 绘制文本(const float x, const float y, const char* 绘制文本, Color color, bool outline = false, float fontSize = 15.0f);
void 绘制空心圆(const float x, const float y, float radius, int numSegments, Color color, float thickness);
void 绘制实心圆(const float x, const float y, float radius, int numSegments, Color color);
void 绘制矩形(const float 左边, const float 顶边, const float 宽度, const float 高度, Color color, float thickness);
void 绘制实心矩形(const float 左边, const float 顶边, const float 宽度, const float 高度, Color color);

void 黑色风格();
void 经典风格();
void 白色风格();
void 典雅风格();
void 暗紫色风格();
void 淡蓝色风格();

bool 开始绘制(const char* name, bool* p_open = NULL, int flags = 0);
void 设置窗口透明度(float alpha);
bool 选择框(const char* label, bool* v);
bool 按钮(const char* label);
bool 按钮(const char* label, const ImVec2& size_arg);
void 彩色文本(const 颜色转换& col, const char* fmt, ...);
void 相同行();
bool 列表开始(const char* str_id, int columns, int flags = 0, float inner_width = 0.0f);
bool 列表换行();
void 列表结束();
bool 选择列表(const char* label, int* current_item, const char* const items[], int items_count, int popup_max_height_in_items = -1);
bool 选择列表(const char* label, int* current_item, const char* items_separated_by_zeros, int popup_max_height_in_items = -1);
void 文本(const char* fmt, ...);
bool 整数滑动条(const char* label, int* v, int v_min, int v_max, const char* format = NULL, int flags = 0);
bool 小数滑动条(const char* label, float* v, float v_min, float v_max, const char* format = NULL, int flags = 0);
bool 单选框(const char* label, int* v, int v_button);
bool 折叠标题头(const char* label, bool* p_visible, ImGuiTreeNodeFlags flags = 0); //CollapsingHeader
bool 折叠标题头(const char* label, ImGuiTreeNodeFlags flags = 0);//CollapsingHeader
void 设置控件宽度(float item_width);//PushItemWidth
void 结束控件宽度();//PopItemWidth
bool 垂直小数滑动条(const char* label, const ImVec2& size, float* v, float v_min, float v_max, const char* format = "%.3f", ImGuiSliderFlags flags = 0); //VSliderFloat
bool 垂直整数滑动条(const char* label, const ImVec2& size, int* v, int v_min, int v_max, const char* format = "%d", ImGuiSliderFlags flags = 0);//VSliderInt
bool 通用垂直滑动条(const char* label, const ImVec2& size, ImGuiDataType data_type, void* p_data, const void* p_min, const void* p_max, const char* format = NULL, ImGuiSliderFlags flags = 0);//VSliderScalar
void 绘制图像(ImTextureRef tex_ref, const ImVec2& p_min, const ImVec2& p_max, const ImVec2& uv_min = ImVec2(0, 0), const ImVec2& uv_max = ImVec2(1, 1), ImU32 col = IM_COL32_WHITE);//AddImage
void 绘制任意变形图像(ImTextureRef tex_ref, const ImVec2& p1, const ImVec2& p2, const ImVec2& p3, const ImVec2& p4, const ImVec2& uv1 = ImVec2(0, 0), const ImVec2& uv2 = ImVec2(1, 0), const ImVec2& uv3 = ImVec2(1, 1), const ImVec2& uv4 = ImVec2(0, 1), ImU32 col = IM_COL32_WHITE);//AddImageQuad
void 绘制圆角图像(ImTextureRef tex_ref, const ImVec2& p_min, const ImVec2& p_max, const ImVec2& uv_min, const ImVec2& uv_max, ImU32 col, float rounding, ImDrawFlags flags = 0);//AddImageRounded
void 设置风格颜色(ImGuiCol idx, ImU32 col);//PushStyleColor
ImVec2 计算文本尺寸(const char* text, const char* text_end = NULL, bool hide_text_after_double_hash = false, float wrap_width = -1.0f);//CalcTextSize
bool RGB颜色编辑控件(const char* label, float col[3], ImGuiColorEditFlags flags = 0);//ColorEdit3
bool RGBA颜色编辑控件(const char* label, float col[4], ImGuiColorEditFlags flags = 0);//ColorEdit4
float 获取每帧时间差();//ImGui::GetIO().DeltaTime
void  绘制折线图(const char* label, const float* values, int values_count, int values_offset = 0, const char* overlay_text = NULL, float scale_min = FLT_MAX, float scale_max = FLT_MAX, ImVec2 graph_size = ImVec2(0, 0), int stride = sizeof(float));//PlotLines
void  绘制折线图(const char* label, float(*values_getter)(void* data, int idx), void* data, int values_count, int values_offset = 0, const char* overlay_text = NULL, float scale_min = FLT_MAX, float scale_max = FLT_MAX, ImVec2 graph_size = ImVec2(0, 0));//PlotLines
void  绘制柱状图(const char* label, const float* values, int values_count, int values_offset = 0, const char* overlay_text = NULL, float scale_min = FLT_MAX, float scale_max = FLT_MAX, ImVec2 graph_size = ImVec2(0, 0), int stride = sizeof(float));//PlotHistogram
void  绘制柱状图(const char* label, float (*values_getter)(void* data, int idx), void* data, int values_count, int values_offset = 0, const char* overlay_text = NULL, float scale_min = FLT_MAX, float scale_max = FLT_MAX, ImVec2 graph_size = ImVec2(0, 0));//PlotHistogram
bool  开始表格控件(const char* label, bool* p_open = NULL, ImGuiTabItemFlags flags = 0); // BeginTabItem
void  结束表格控件();// EndTabItem
bool  开始子表格(const char* str_id, const ImVec2& size = ImVec2(0, 0), ImGuiChildFlags child_flags = 0, ImGuiWindowFlags window_flags = 0);//BeginChild
bool  开始子表格(ImGuiID id, const ImVec2& size = ImVec2(0, 0), ImGuiChildFlags child_flags = 0, ImGuiWindowFlags window_flags = 0);//BeginChild
void  结束子表格();//EndChild
void  开始禁用(bool disabled = true);//BeginDisabled
void  结束禁用();//EndDisabled
void  帮助标记(const char* desc);//HelpMarker
void  绘制禁用文本(const char* fmt, ...); // TextDisabled
bool  上个控件是否悬停(ImGuiHoveredFlags flags = 0);//IsItemHovered
bool  开始工具提示(); //BeginTooltip
void  结束工具提示();//EndTooltip
ImVec2 线性插值(const ImVec2& a, const ImVec2& b, float t);//ImLerp
ImVec2 线性插值(const ImVec2& a, const ImVec2& b, const ImVec2& t);//ImLerp
ImVec4 线性插值(const ImVec4& a, const ImVec4& b, float t);//ImLerp
void  设置光标位置(const ImVec2& local_pos);//SetCursorPos
void  设置光标X位置(float local_x);//SetCursorPosX
void  设置光标Y位置(float local_y);//SetCursorPosY
void  结束绘制();
//提供的调用函数
int 求距离(D3D坐标 自身坐标, D3D坐标 对象坐标);
void 读矩阵(uint64_t 矩阵地址, float(&返回矩阵)[4][4]);
template<typename 类型>
类型 读(uint64_t 地址)
{
    if (地址 == 0) return 0;
    if (is_same<类型, int>::value)
        return MDL_读整数(地址, 极速_随机可用通讯方式());
    if (is_same<类型, uint64_t>::value)
        return MDL_读长整数(地址, 极速_随机可用通讯方式());
    if (is_same<类型, double>::value)
        return MDL_读双浮点(地址, 极速_随机可用通讯方式());
    if (is_same<类型, float>::value)
        return MDL_读单浮点(地址, 极速_随机可用通讯方式());
    if (is_same<类型, BYTE>::value)
        return MDL_读字节(地址, 极速_随机可用通讯方式());
    if (is_same<类型, SHORT>::value)
        return MDL_读短整数(地址, 极速_随机可用通讯方式());
}

template<typename 类型>
类型 读(uint64_t 地址, uint64_t 读取长度)
{
    if (地址 == 0) return {};
    if (is_same<类型, std::vector<BYTE>>::value)
        return MDL_读字节数组(地址, 读取长度, 极速_随机可用通讯方式());
}

template<typename 类型>
bool 写(uint64_t 地址, 类型 写入值)
{
    if (地址 == 0) return false;
    if constexpr (is_same<类型, int>::value)
        return CR3_写整数(地址, 写入值, 极速_随机可用通讯方式());
    if constexpr (is_same<类型, uint64_t>::value)
        return CR3_写长整数(地址, 写入值, 极速_随机可用通讯方式());
    if constexpr (is_same<类型, double>::value)
        return CR3_写双浮点(地址, 写入值, 极速_随机可用通讯方式());
    if constexpr (is_same<类型, float>::value)
        return CR3_写单浮点(地址, 写入值, 极速_随机可用通讯方式());
    if constexpr (is_same<类型, BYTE>::value)
        return CR3_写字节(地址, 写入值, 极速_随机可用通讯方式());
    if constexpr (is_same<类型, SHORT>::value)
        return CR3_写短整数(地址, 写入值, 极速_随机可用通讯方式());
    return FALSE;
}
template<typename 类型>
bool 写(uint64_t 地址, 类型 写入值, int 写入长度)
{
    if constexpr (is_same<类型, std::vector<BYTE>>::value)
        return CR3_写字节数组(地址, 写入值, 写入长度, 极速_随机可用通讯方式());
    return FALSE;
}
