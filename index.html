<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>歌曲信息管理系统</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  <style>
    .cell-editing {
      background-color: rgba(59, 130, 246, 0.05);
      border-color: rgba(59, 130, 246, 0.5);
    }
    .required-field::after {
      content: '*';
      color: #ef4444;
      margin-left: 0.25rem;
    }
    .editable-cell {
      cursor: text;
    }
    [data-style~="bold"] { font-weight: bold; }
    [data-style~="italic"] { font-style: italic; }
    [data-style~="underline"] { text-decoration: underline; }
    .btn-active {
      background-color: rgba(59, 130, 246, 0.1);
      color: #3b82f6;
    }
    .table-shadow {
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
    }
    .selected-col {
      background-color: rgba(59, 130, 246, 0.07);
    }
    .selected-col-header {
      background-color: rgba(59, 130, 246, 0.15);
    }
    .btn-primary {
      background-color: #3b82f6;
      color: white;
    }
    .btn-primary:hover {
      background-color: #2563eb;
    }
    .btn-outline {
      border: 1px solid #3b82f6;
      color: #3b82f6;
    }
    .btn-outline:hover {
      background-color: rgba(59, 130, 246, 0.1);
    }
    .toast-success {
      background-color: #10b981;
    }
    .toast-error {
      background-color: #ef4444;
    }
    .toast-warning {
      background-color: #f59e0b;
    }
    .toast-info {
      background-color: #06b6d4;
    }
    .cell-wrapper {
      position: relative;
      height: 100%;
      padding: 8px;
    }
    .debug-info {
      background-color: #f8fafc;
      border-top: 1px solid #e2e8f0;
      padding: 12px;
      font-size: 13px;
      color: #64748b;
    }
    .debug-info strong {
      color: #334155;
    }
    th {
      position: relative;
    }
    td {
      position: relative;
    }
    .debug-toggle {
      position: fixed;
      bottom: 20px;
      left: 20px;
      background: #f1f5f9;
      border: 1px solid #cbd5e1;
      padding: 6px 12px;
      border-radius: 20px;
      font-size: 13px;
      cursor: pointer;
      z-index: 100;
    }
    .status-bar {
      display: flex;
      justify-content: space-between;
      padding: 8px 16px;
      background: #f1f5f9;
      border-top: 1px solid #e2e8f0;
      font-size: 14px;
    }
    .row-controls {
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .col-controls {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-left: 12px;
    }
    .format-controls {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-left: 12px;
    }
    .controls-container {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }
    .toolbar-section {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 4px 8px;
      background: rgba(241, 245, 249, 0.5);
      border-radius: 6px;
    }
    .toolbar-divider {
      height: 24px;
      width: 1px;
      background: #cbd5e1;
      margin: 0 8px;
    }
    .btn-outline {
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 6px 8px;
      border-radius: 6px;
      transition: all 0.2s;
      min-width: 36px;
    }
    .btn-outline i {
      font-size: 14px;
    }
    .btn-text {
      padding: 6px 12px;
      font-size: 14px;
    }
  </style>
</head>

<body class="font-inter bg-gray-50 text-neutral-800 min-h-screen flex flex-col">
  <!-- 顶部导航栏 -->
  <header class="bg-white border-b border-gray-200 shadow-sm sticky top-0 z-50">
    <div class="container mx-auto px-4 py-3 flex items-center justify-between">
      <div class="flex items-center space-x-2">
        <i class="fa fa-music text-blue-500 text-2xl"></i>
        <h1 class="text-xl font-bold text-neutral-800">歌曲信息管理<span></h1>
      </div>

      <div class="flex items-center space-x-4">
        <input type="text" id="table-name" placeholder="未命名歌曲表" class="border rounded-md px-3 py-1.5 text-sm" value="热门歌曲列表">
        <button id="save-btn" class="bg-green-600 hover:bg-green-700 text-white px-4 py-1.5 rounded-md">
          <i class="fa fa-save mr-1"></i> 保存
        </button>
      </div>
    </div>
  </header>

  <!-- 表格编辑区域 -->
  <main class="flex-grow container mx-auto px-4 py-6">
    <div class="bg-white rounded-lg table-shadow overflow-hidden">
      <!-- 表格工具栏 -->
      <div class="border-b border-gray-200 p-3 bg-gray-50">
        <div class="controls-container">
          <div class="toolbar-section">
            <span class="text-sm font-medium text-gray-700">行操作</span>
            <button id="add-row-btn" class="btn-outline" title="添加行">
              <i class="fa fa-plus"></i>
            </button>
            <button id="delete-row-btn" class="btn-outline" title="删除选中行">
              <i class="fa fa-trash-o"></i>
            </button>
            <button id="move-row-up-btn" class="btn-outline" title="上移选中行">
              <i class="fa fa-arrow-up"></i>
            </button>
            <button id="move-row-down-btn" class="btn-outline" title="下移选中行">
              <i class="fa fa-arrow-down"></i>
            </button>
          </div>

          <div class="toolbar-divider"></div>

          <div class="toolbar-section">
            <span class="text-sm font-medium text-gray-700">列操作</span>
            <button id="add-col-btn" class="btn-outline" title="添加列">
              <i class="fa fa-plus-square-o"></i>
            </button>
            <button id="delete-col-btn" class="btn-outline" title="删除选中列">
              <i class="fa fa-trash"></i>
            </button>
            <button id="move-col-left-btn" class="btn-outline" title="左移选中列">
              <i class="fa fa-arrow-left"></i>
            </button>
            <button id="move-col-right-btn" class="btn-outline" title="右移选中列">
              <i class="fa fa-arrow-right"></i>
            </button>
          </div>

          <div class="toolbar-divider"></div>

          <div class="toolbar-section">
            <span class="text-sm font-medium text-gray-700">格式</span>
            <button id="btn-bold" class="btn-outline" title="加粗">
              <i class="fa fa-bold"></i>
            </button>
            <button id="btn-italic" class="btn-outline" title="斜体">
              <i class="fa fa-italic"></i>
            </button>
            <button id="btn-underline" class="btn-outline" title="下划线">
              <i class="fa fa-underline"></i>
            </button>
          </div>
          
          <div class="toolbar-section ml-auto">
            <div class="text-sm text-gray-700 px-2 py-1 bg-gray-100 rounded-md">
              <i class="fa fa-columns mr-1"></i> 当前选中列: <span id="current-col-display">-</span>
            </div>
          </div>
        </div>
      </div>

      <!-- 表格内容 -->
      <div class="overflow-x-auto">
        <table id="collab-table" class="w-full border-collapse">
          <thead>
            <tr>
              <th class="border p-2 text-center w-12 relative">
                <input type="checkbox" id="select-all">
              </th>
              <th class="border p-2 text-left min-w-[150px] relative" data-col="0">
                <div class="cell-wrapper">
                  <span class="required-field">歌名</span>
                </div>
              </th>
              <th class="border p-2 text-left min-w-[150px] relative" data-col="1">
                <div class="cell-wrapper">
                  <span class="required-field">作曲</span>
                </div>
              </th>
              <th class="border p-2 text-left min-w-[150px] relative" data-col="2">
                <div class="cell-wrapper">
                  <span>作词</span>
                </div>
              </th>
              <th class="border p-2 text-left min-w-[150px] relative" data-col="3">
                <div class="cell-wrapper">
                  <span>专辑</span>
                </div>
              </th>
              <th class="border p-2 text-left min-w-[150px] relative" data-col="4">
                <div class="cell-wrapper">
                  <span>发行年份</span>
                </div>
              </th>
              <th class="border p-2 text-left min-w-[150px] relative" data-col="5">
                <div class="cell-wrapper">
                  <span>时长</span>
                </div>
              </th>
            </tr>
          </thead>
          <tbody>
            <tr data-row="0">
              <td class="border p-2 text-center relative">
                <input type="checkbox" class="row-select">
              </td>
              <td class="border p-2 editable-cell required relative" data-col="0">
                <div class="cell-wrapper">
                  晴天
                </div>
              </td>
              <td class="border p-2 editable-cell required relative" data-col="1">
                <div class="cell-wrapper">
                  周杰伦
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="2">
                <div class="cell-wrapper">
                  周杰伦
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="3">
                <div class="cell-wrapper">
                  叶惠美
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="4">
                <div class="cell-wrapper">
                  2003-07-31
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="5">
                <div class="cell-wrapper">
                  04:26
                </div>
              </td>
            </tr>
            <tr data-row="1">
              <td class="border p-2 text-center relative">
                <input type="checkbox" class="row-select">
              </td>
              <td class="border p-2 editable-cell required relative" data-col="0">
                <div class="cell-wrapper">
                  简单爱
                </div>
              </td>
              <td class="border p-2 editable-cell required relative" data-col="1">
                <div class="cell-wrapper">
                  周杰伦
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="2">
                <div class="cell-wrapper">
                  周杰伦
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="3">
                <div class="cell-wrapper">
                  范特西
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="4">
                <div class="cell-wrapper">
                  2001-09-20
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="5">
                <div class="cell-wrapper">
                  04:00
                </div>
              </td>
            </tr>
            <tr data-row="2">
              <td class="border p-2 text-center relative">
                <input type="checkbox" class="row-select">
              </td>
              <td class="border p-2 editable-cell required relative" data-col="0">
                <div class="cell-wrapper">
                  小幸运
                </div>
              </td>
              <td class="border p-2 editable-cell required relative" data-col="1">
                <div class="cell-wrapper">
                  JerryC
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="2">
                <div class="cell-wrapper">
                  徐世珍
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="3">
                <div class="cell-wrapper">
                  我的少女时代
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="4">
                <div class="cell-wrapper">
                  2015-10-23
                </div>
              </td>
              <td class="border p-2 editable-cell relative" data-col="5">
                <div class="cell-wrapper">
                  03:42
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      
      <!-- 状态栏 -->
      <div class="status-bar">
        <div>
          <span class="text-sm"><i class="fa fa-list mr-1"></i> 总行数: <span id="total-rows">3</span></span>
          <span class="text-sm ml-4"><i class="fa fa-columns mr-1"></i> 总列数: <span id="total-cols">6</span></span>
          <span class="text-sm ml-4"><i class="fa fa-check-square-o mr-1"></i> 选中列: <span id="current-col-index">-</span></span>
        </div>
        <div>
          <span class="text-sm text-gray-600"><i class="fa fa-lightbulb-o mr-1"></i> 双击单元格编辑内容</span>
        </div>
      </div>
    </div>
  </main>

  <script>
    let currentEditingCell = null;
    let currentEditingCol = null;
    let activeStyles = new Set();
    let debugMode = true;

    // 更新调试信息
    function updateDebugInfo() {
      document.getElementById('current-col-index').textContent = currentEditingCol || '-';
      document.getElementById('total-cols').textContent = document.querySelectorAll('thead th:not(:first-child)').length;
      document.getElementById('total-rows').textContent = document.querySelectorAll('tbody tr').length;
      document.getElementById('current-col-display').textContent = currentEditingCol || '-';
    }

    // 单元格编辑功能
    function setupCellEditing() {
      document.querySelectorAll('.editable-cell').forEach(cell => {
        cell.addEventListener('dblclick', () => {
          if (currentEditingCell) exitEditing();
          enterEditing(cell);
        });

        cell.addEventListener('keydown', (e) => {
          if (e.key === 'Escape') exitEditing();
          if (e.key === 'Enter' && !e.shiftKey) {
            e.preventDefault();
            exitEditing();
          }
        });
        
        cell.addEventListener('click', () => {
          selectColumn(cell);
        });
      });
      
      // 表头编辑功能
      document.querySelectorAll('thead th:not(:first-child)').forEach(th => {
        th.addEventListener('dblclick', () => {
          const span = th.querySelector('.cell-wrapper > span:first-child');
          if (!span) return;
          
          const original = span.textContent;
          th.innerHTML = `<input type="text" class="w-full h-full border-none bg-transparent p-0" value="${original}">`;
          const input = th.querySelector('input');
          input.focus();
          
          input.addEventListener('blur', () => {
            const colIndex = th.dataset.col;
            th.innerHTML = `
              <div class="cell-wrapper">
                <span class="${span.classList.contains('required-field') ? 'required-field' : ''}">${input.value}</span>
              </div>
            `;
          });
          
          input.addEventListener('keydown', (e) => {
            if (e.key === 'Enter') {
              const colIndex = th.dataset.col;
              th.innerHTML = `
                <div class="cell-wrapper">
                  <span class="${span.classList.contains('required-field') ? 'required-field' : ''}">${input.value}</span>
                </div>
              `;
            }
          });
        });
      });
    }

    function enterEditing(cell) {
      currentEditingCell = cell;
      const value = cell.querySelector('.cell-wrapper').textContent.trim();
      const style = cell.getAttribute('data-style');
      
      cell.innerHTML = `<input type="text" class="w-full h-full border-none bg-transparent p-0" value="${value}">`;
      cell.classList.add('cell-editing');
      
      const input = cell.querySelector('input');
      input.focus();
      
      // 应用当前样式到输入框
      if (style) {
        if (style.includes('bold')) input.style.fontWeight = 'bold';
        if (style.includes('italic')) input.style.fontStyle = 'italic';
        if (style.includes('underline')) input.style.textDecoration = 'underline';
      }
      
      // 更新按钮状态
      updateStyleButtons(style);
    }

    function exitEditing() {
      if (!currentEditingCell) return;
      const input = currentEditingCell.querySelector('input');
      
      if (currentEditingCell.classList.contains('required') && !input.value.trim()) {
        showToast('必填字段不能为空', 'error');
        input.focus();
        return;
      }
      
      // 保存样式
      let style = '';
      if (input.style.fontWeight === 'bold') style += 'bold ';
      if (input.style.fontStyle === 'italic') style += 'italic ';
      if (input.style.textDecoration === 'underline') style += 'underline ';
      style = style.trim();
      
      if (style) {
        currentEditingCell.setAttribute('data-style', style);
      } else {
        currentEditingCell.removeAttribute('data-style');
      }
      
      const col = currentEditingCell.dataset.col;
      currentEditingCell.innerHTML = `
        <div class="cell-wrapper">
          ${input.value}
        </div>
      `;
      currentEditingCell.classList.remove('cell-editing');
      currentEditingCell = null;
      
      // 重置按钮状态
      resetStyleButtons();
    }

    // 选择列
    function selectColumn(cell) {
      // 移除之前选中列的高亮
      clearColumnSelection();
      
      // 高亮当前选中列
      const col = cell.dataset.col;
      currentEditingCol = col;
      
      // 高亮表头
      const header = document.querySelector(`thead th[data-col="${col}"]`);
      if (header) header.classList.add('selected-col-header');
      
      // 高亮所有单元格
      document.querySelectorAll(`td[data-col="${col}"]`).forEach(el => {
        el.classList.add('selected-col');
      });
      
      updateDebugInfo();
    }

    function clearColumnSelection() {
    // 移除表头高亮
    const headers = document.querySelectorAll('thead th.selected-col-header');
    headers.forEach(header => {
      header.classList.remove('selected-col-header');
    });
  
    // 移除单元格高亮
    const cells = document.querySelectorAll('td.selected-col');
    cells.forEach(cell => {
      cell.classList.remove('selected-col');
    });
  
    // 重置状态变量
    currentEditingCol = null;
    updateDebugInfo();
  }

    // 行操作
    function deleteSelectedRows() {
      const selectedRows = document.querySelectorAll('.row-select:checked');
      if (selectedRows.length === 0) {
        showToast('请先选择要删除的行', 'warning');
        return;
      }
      
      if (confirm(`确定要删除选中的 ${selectedRows.length} 行数据吗？`)) {
        // 从下往上删除，避免索引变化
        Array.from(selectedRows).reverse().forEach(row => {
          row.closest('tr').remove();
        });
        renumberRows();
        showToast('行删除成功', 'success');
        updateDebugInfo();
      }
    }

    // 修复行移动功能
    function moveRow(direction) {
      const selectedRows = document.querySelectorAll('.row-select:checked');
      if (selectedRows.length === 0) {
        showToast('请先选择要移动的行', 'warning');
        return;
      }
      
      const tbody = document.querySelector('tbody');
      const rows = Array.from(tbody.querySelectorAll('tr'));
      const selectedRowElements = Array.from(selectedRows).map(checkbox => checkbox.closest('tr'));
      
      // 保存选中状态
      const rowStates = selectedRowElements.map(row => row.querySelector('.row-select').checked);
      
      // 根据移动方向排序
      if (direction === 'up') {
        // 上移：按索引升序排列，从顶部开始移动
        selectedRowElements.sort((a, b) => rows.indexOf(a) - rows.indexOf(b));
      } else {
        // 下移：按索引降序排列，从底部开始移动
        selectedRowElements.sort((a, b) => rows.indexOf(b) - rows.indexOf(a));
      }
      
      // 移动行
      selectedRowElements.forEach(row => {
        const currentIndex = rows.indexOf(row);
        let targetIndex;
        
        if (direction === 'up') {
          targetIndex = currentIndex - 1;
          if (targetIndex >= 0) {
            tbody.insertBefore(row, rows[targetIndex]);
          }
        } else {
          targetIndex = currentIndex + 1;
          if (targetIndex < rows.length) {
            // 插入到下一行的后面
            tbody.insertBefore(row, rows[targetIndex].nextSibling);
          }
        }
      });
      
      // 恢复选中状态
      selectedRowElements.forEach((row, index) => {
        row.querySelector('.row-select').checked = rowStates[index];
      });
      
      renumberRows();
      showToast(`行${direction === 'up' ? '上' : '下'}移成功`, 'success');
      updateDebugInfo();
    }

    // 列操作
    function deleteSelectedColumns() {
      if (currentEditingCol === null) {
        showToast('请先选择要删除的列', 'warning');
        return;
      }
      
      const col = currentEditingCol;
      const header = document.querySelector(`thead th[data-col="${col}"]`);
      const colName = header.querySelector('.cell-wrapper > span:first-child').textContent;
      
      if (confirm(`确定要删除"${colName}"列吗？`)) {
        // 删除表头
        document.querySelector(`thead th[data-col="${col}"]`).remove();
        
        // 删除所有行中的该列
        document.querySelectorAll(`tbody tr`).forEach(row => {
          const cell = row.querySelector(`td[data-col="${col}"]`);
          if (cell) cell.remove();
        });
        
        clearColumnSelection();
        renumberColumns();
        showToast('列删除成功', 'success');
        updateDebugInfo();
      }
    }

    function moveColumn(direction) {
      if (currentEditingCol === null) {
        showToast('请先选择要移动的列', 'warning');
        return;
      }
      
      const col = currentEditingCol;
      const headers = document.querySelectorAll('thead th:not(:first-child)');
      const colIndex = Array.from(headers).findIndex(th => th.dataset.col === col);
      
      // 边界检查
      if ((direction === 'left' && colIndex <= 0) || 
          (direction === 'right' && colIndex >= headers.length - 1)) {
        showToast('列已在边缘位置，无法继续移动', 'warning');
        return;
      }
      
      const targetIndex = direction === 'left' ? colIndex - 1 : colIndex + 1;
      const targetCol = headers[targetIndex].dataset.col;
      
      // 移动表头
      const headerRow = document.querySelector('thead tr');
      const sourceHeader = headers[colIndex];
      const targetHeader = headers[targetIndex];
      
      if (direction === 'left') {
        headerRow.insertBefore(sourceHeader, targetHeader);
      } else {
        headerRow.insertBefore(sourceHeader, targetHeader.nextSibling);
      }
      
      // 移动所有行的单元格
      document.querySelectorAll('tbody tr').forEach(row => {
        const cells = Array.from(row.querySelectorAll('td'));
        const sourceCell = cells.find(cell => cell.dataset.col === col);
        const targetCell = cells.find(cell => cell.dataset.col === targetCol);
        
        if (sourceCell && targetCell) {
          if (direction === 'left') {
            row.insertBefore(sourceCell, targetCell);
          } else {
            row.insertBefore(sourceCell, targetCell.nextSibling);
          }
        }
      });
      
      renumberColumns();
      showToast(`列${direction === 'left' ? '左' : '右'}移成功`, 'success');
      clearColumnSelection();
      updateDebugInfo();
    }

    // 字体样式调整
    function applyStyle(style) {
      if (!currentEditingCell) return;
      
      const input = currentEditingCell.querySelector('input');
      
      // 切换样式状态
      if (input.style.fontWeight === 'bold' && style === 'bold') {
        input.style.fontWeight = 'normal';
        activeStyles.delete('bold');
      } else if (style === 'bold') {
        input.style.fontWeight = 'bold';
        activeStyles.add('bold');
      }
      
      if (input.style.fontStyle === 'italic' && style === 'italic') {
        input.style.fontStyle = 'normal';
        activeStyles.delete('italic');
      } else if (style === 'italic') {
        input.style.fontStyle = 'italic';
        activeStyles.add('italic');
      }
      
      if (input.style.textDecoration === 'underline' && style === 'underline') {
        input.style.textDecoration = 'none';
        activeStyles.delete('underline');
      } else if (style === 'underline') {
        input.style.textDecoration = 'underline';
        activeStyles.add('underline');
      }
      
      updateStyleButtons(Array.from(activeStyles).join(' '));
    }

    function updateStyleButtons(style) {
      resetStyleButtons();
      
      if (style && style.includes('bold')) document.getElementById('btn-bold').classList.add('btn-active');
      if (style && style.includes('italic')) document.getElementById('btn-italic').classList.add('btn-active');
      if (style && style.includes('underline')) document.getElementById('btn-underline').classList.add('btn-active');
    }

    function resetStyleButtons() {
      document.getElementById('btn-bold').classList.remove('btn-active');
      document.getElementById('btn-italic').classList.remove('btn-active');
      document.getElementById('btn-underline').classList.remove('btn-active');
      activeStyles.clear();
    }

    // 辅助函数
    function renumberRows() {
      document.querySelectorAll('tbody tr').forEach((row, index) => {
        row.dataset.row = index;
      });
    }

    function renumberColumns() {
      // 重新编号表头
      document.querySelectorAll('thead th:not(:first-child)').forEach((th, index) => {
        th.dataset.col = index;
      });
      
      // 重新编号所有行中的列
      document.querySelectorAll('tbody tr').forEach(row => {
        const cells = Array.from(row.querySelectorAll('td:not(:first-child)'));
        cells.forEach((cell, colIndex) => {
          cell.dataset.col = colIndex;
        });
      });
      
      // 清除列选择
      clearColumnSelection();
    }

    function addRow() {
      const tbody = document.querySelector('tbody');
      const rowIndex = tbody.children.length;
      
      // 获取当前列数
      const colCount = document.querySelectorAll('thead th:not(:first-child)').length;
      
      let rowHtml = `<td class="border p-2 text-center relative">
        <input type="checkbox" class="row-select">
      </td>`;
      
      // 为每一列创建单元格
      for (let i = 0; i < colCount; i++) {
        // 前两列为必填字段
        const required = i === 0 || i === 1 ? 'required' : '';
        rowHtml += `
          <td class="border p-2 editable-cell ${required} relative" data-col="${i}">
            <div class="cell-wrapper">
            </div>
          </td>
        `;
      }
      
      const newRow = document.createElement('tr');
      newRow.dataset.row = rowIndex;
      newRow.innerHTML = rowHtml;
      
      tbody.appendChild(newRow);
      setupCellEditing();
      
      setTimeout(() => {
        const firstCell = newRow.querySelector('.editable-cell');
        if (firstCell) firstCell.click();
      }, 100);
      
      showToast('行添加成功', 'success');
      updateDebugInfo();
    }

    function addColumn() {
      // 获取当前列数（跳过复选框列）
      const colCount = document.querySelectorAll('thead th:not(:first-child)').length;
      const newColIndex = colCount;
      
      // 添加表头
      const headerRow = document.querySelector('thead tr');
      const newTh = document.createElement('th');
      newTh.className = 'border p-2 text-left min-w-[150px] relative';
      newTh.dataset.col = newColIndex;
      newTh.innerHTML = `
        <div class="cell-wrapper">
          新列${newColIndex + 1}
        </div>
      `;
      headerRow.appendChild(newTh);
      
      // 添加表体单元格
      document.querySelectorAll('tbody tr').forEach((row, rowIndex) => {
        const newTd = document.createElement('td');
        newTd.className = 'border p-2 editable-cell relative';
        newTd.dataset.col = newColIndex;
        newTd.innerHTML = `
          <div class="cell-wrapper">
          </div>
        `;
        row.appendChild(newTd);
      });
      
      setupCellEditing();
      showToast('列添加成功', 'success');
      updateDebugInfo();
    }

    // 显示提示消息
    function showToast(message, type = 'success') {
      const toast = document.createElement('div');
      toast.className = `fixed bottom-4 right-4 px-4 py-2 rounded-md shadow-lg text-white z-50 transition-all duration-300`;
      toast.style.opacity = '0';
      toast.style.transform = 'translateY(20px)';
      
      if (type === 'success') {
        toast.classList.add('toast-success');
        toast.innerHTML = `<i class="fa fa-check-circle mr-2"></i>${message}`;
      } else if (type === 'error') {
        toast.classList.add('toast-error');
        toast.innerHTML = `<i class="fa fa-exclamation-circle mr-2"></i>${message}`;
      } else if (type === 'warning') {
        toast.classList.add('toast-warning');
        toast.innerHTML = `<i class="fa fa-exclamation-triangle mr-2"></i>${message}`;
      } else if (type === 'info') {
        toast.classList.add('toast-info');
        toast.innerHTML = `<i class="fa fa-info-circle mr-2"></i>${message}`;
      }
      
      document.body.appendChild(toast);
      
      // 显示动画
      setTimeout(() => {
        toast.style.transition = 'all 0.3s ease';
        toast.style.opacity = '1';
        toast.style.transform = 'translateY(0)';
      }, 10);
      
      // 隐藏动画
      setTimeout(() => {
        toast.style.opacity = '0';
        toast.style.transform = 'translateY(20px)';
        setTimeout(() => document.body.removeChild(toast), 300);
      }, 3000);
    }

    // 初始化
    document.addEventListener('DOMContentLoaded', () => {
      setupCellEditing();
      updateDebugInfo();

      // 行操作绑定
      document.getElementById('add-row-btn').addEventListener('click', addRow);
      document.getElementById('delete-row-btn').addEventListener('click', deleteSelectedRows);
      document.getElementById('move-row-up-btn').addEventListener('click', () => moveRow('up'));
      document.getElementById('move-row-down-btn').addEventListener('click', () => moveRow('down'));

      // 列操作绑定
      document.getElementById('add-col-btn').addEventListener('click', addColumn);
      document.getElementById('delete-col-btn').addEventListener('click', deleteSelectedColumns);
      document.getElementById('move-col-left-btn').addEventListener('click', () => moveColumn('left'));
      document.getElementById('move-col-right-btn').addEventListener('click', () => moveColumn('right'));

      // 样式按钮绑定
      document.getElementById('btn-bold').addEventListener('click', () => applyStyle('bold'));
      document.getElementById('btn-italic').addEventListener('click', () => applyStyle('italic'));
      document.getElementById('btn-underline').addEventListener('click', () => applyStyle('underline'));

      // 全选功能
      document.getElementById('select-all').addEventListener('change', (e) => {
        document.querySelectorAll('.row-select').forEach(checkbox => {
          checkbox.checked = e.target.checked;
        });
      });

      // 保存功能
      document.getElementById('save-btn').addEventListener('click', () => {
        const tableName = document.getElementById('table-name').value || '未命名歌曲表';
        showToast(`"${tableName}" 保存成功`, 'success');
      });

      // 退出编辑模式
      document.addEventListener('click', (e) => {
        // 点击工具栏或表格空白处时清除高亮
        if (!e.target.closest('.cell-editing') && 
            !e.target.closest('.btn-outline') && 
            !e.target.closest('.row-select') &&
            !e.target.closest('.selected-col') && 
            !e.target.closest('.selected-col-header')) {
          clearColumnSelection();
        }
      });
    });
  </script>
</body>
</html>
