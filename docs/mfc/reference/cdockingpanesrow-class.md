---
description: 了解详细信息： CDockingPanesRow 类
title: CDockingPanesRow 类
ms.date: 10/18/2018
f1_keywords:
- CDockingPanesRow
- AFXDOCKINGPANESROW/CDockingPanesRow
- AFXDOCKINGPANESROW/CDockingPanesRow::AddPane
- AFXDOCKINGPANESROW/CDockingPanesRow::AddPaneFromRow
- AFXDOCKINGPANESROW/CDockingPanesRow::ArrangePanes
- AFXDOCKINGPANESROW/CDockingPanesRow::CalcFixedLayout
- AFXDOCKINGPANESROW/CDockingPanesRow::Create
- AFXDOCKINGPANESROW/CDockingPanesRow::ExpandStretchedPanes
- AFXDOCKINGPANESROW/CDockingPanesRow::ExpandStretchedPanesRect
- AFXDOCKINGPANESROW/CDockingPanesRow::FixupVirtualRects
- AFXDOCKINGPANESROW/CDockingPanesRow::GetAvailableLength
- AFXDOCKINGPANESROW/CDockingPanesRow::GetAvailableSpace
- AFXDOCKINGPANESROW/CDockingPanesRow::GetClientRect
- AFXDOCKINGPANESROW/CDockingPanesRow::GetDockSite
- AFXDOCKINGPANESROW/CDockingPanesRow::GetExtraSpace
- AFXDOCKINGPANESROW/CDockingPanesRow::GetGroupFromPane
- AFXDOCKINGPANESROW/CDockingPanesRow::GetID
- AFXDOCKINGPANESROW/CDockingPanesRow::GetMaxPaneSize
- AFXDOCKINGPANESROW/CDockingPanesRow::GetPaneCount
- AFXDOCKINGPANESROW/CDockingPanesRow::GetPaneList
- AFXDOCKINGPANESROW/CDockingPanesRow::GetRowAlignment
- AFXDOCKINGPANESROW/CDockingPanesRow::GetRowHeight
- AFXDOCKINGPANESROW/CDockingPanesRow::GetRowOffset
- AFXDOCKINGPANESROW/CDockingPanesRow::GetVisibleCount
- AFXDOCKINGPANESROW/CDockingPanesRow::GetWindowRect
- AFXDOCKINGPANESROW/CDockingPanesRow::HasPane
- AFXDOCKINGPANESROW/CDockingPanesRow::IsEmpty
- AFXDOCKINGPANESROW/CDockingPanesRow::IsExclusiveRow
- AFXDOCKINGPANESROW/CDockingPanesRow::IsHorizontal
- AFXDOCKINGPANESROW/CDockingPanesRow::IsVisible
- AFXDOCKINGPANESROW/CDockingPanesRow::Move
- AFXDOCKINGPANESROW/CDockingPanesRow::MovePane
- AFXDOCKINGPANESROW/CDockingPanesRow::OnResizePane
- AFXDOCKINGPANESROW/CDockingPanesRow::RedrawAll
- AFXDOCKINGPANESROW/CDockingPanesRow::RemovePane
- AFXDOCKINGPANESROW/CDockingPanesRow::ReplacePane
- AFXDOCKINGPANESROW/CDockingPanesRow::RepositionPanes
- AFXDOCKINGPANESROW/CDockingPanesRow::Resize
- AFXDOCKINGPANESROW/CDockingPanesRow::ResizeByPaneDivider
- AFXDOCKINGPANESROW/CDockingPanesRow::ScreenToClient
- AFXDOCKINGPANESROW/CDockingPanesRow::SetExtra
- AFXDOCKINGPANESROW/CDockingPanesRow::ShowDockSiteRow
- AFXDOCKINGPANESROW/CDockingPanesRow::ShowPane
- AFXDOCKINGPANESROW/CDockingPanesRow::UpdateVisibleState
helpviewer_keywords:
- CDockingPanesRow [MFC], AddPane
- CDockingPanesRow [MFC], AddPaneFromRow
- CDockingPanesRow [MFC], ArrangePanes
- CDockingPanesRow [MFC], CalcFixedLayout
- CDockingPanesRow [MFC], Create
- CDockingPanesRow [MFC], ExpandStretchedPanes
- CDockingPanesRow [MFC], ExpandStretchedPanesRect
- CDockingPanesRow [MFC], FixupVirtualRects
- CDockingPanesRow [MFC], GetAvailableLength
- CDockingPanesRow [MFC], GetAvailableSpace
- CDockingPanesRow [MFC], GetClientRect
- CDockingPanesRow [MFC], GetDockSite
- CDockingPanesRow [MFC], GetExtraSpace
- CDockingPanesRow [MFC], GetGroupFromPane
- CDockingPanesRow [MFC], GetID
- CDockingPanesRow [MFC], GetMaxPaneSize
- CDockingPanesRow [MFC], GetPaneCount
- CDockingPanesRow [MFC], GetPaneList
- CDockingPanesRow [MFC], GetRowAlignment
- CDockingPanesRow [MFC], GetRowHeight
- CDockingPanesRow [MFC], GetRowOffset
- CDockingPanesRow [MFC], GetVisibleCount
- CDockingPanesRow [MFC], GetWindowRect
- CDockingPanesRow [MFC], HasPane
- CDockingPanesRow [MFC], IsEmpty
- CDockingPanesRow [MFC], IsExclusiveRow
- CDockingPanesRow [MFC], IsHorizontal
- CDockingPanesRow [MFC], IsVisible
- CDockingPanesRow [MFC], Move
- CDockingPanesRow [MFC], MovePane
- CDockingPanesRow [MFC], OnResizePane
- CDockingPanesRow [MFC], RedrawAll
- CDockingPanesRow [MFC], RemovePane
- CDockingPanesRow [MFC], ReplacePane
- CDockingPanesRow [MFC], RepositionPanes
- CDockingPanesRow [MFC], Resize
- CDockingPanesRow [MFC], ResizeByPaneDivider
- CDockingPanesRow [MFC], ScreenToClient
- CDockingPanesRow [MFC], SetExtra
- CDockingPanesRow [MFC], ShowDockSiteRow
- CDockingPanesRow [MFC], ShowPane
- CDockingPanesRow [MFC], UpdateVisibleState
ms.assetid: e7a17832-0ebb-4bce-b799-cec9b60f76fe
ms.openlocfilehash: bf031b19c25cde36705333feb3baa3af9e1932ae
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185006"
---
# <a name="cdockingpanesrow-class"></a>CDockingPanesRow 类

管理位于停靠站点中同一水平或垂直行（列）的窗格的列表。

有关更多详细信息，请参阅位于 Visual Studio 安装的 **VC \\ atlmfc \\ src \\ mfc** 文件夹中的源代码。

## <a name="syntax"></a>语法

```
class CDockingPanesRow : public CObject
```

## <a name="members"></a>成员

### <a name="public-constructors"></a>公共构造函数

|“属性”|描述|
|----------|-----------------|
|`CDockingPanesRow::CDockingPanesRow`|默认构造函数。|

### <a name="public-methods"></a>公共方法

|“属性”|描述|
|----------|-----------------|
|[CDockingPanesRow::AddPane](#addpane)||
|[CDockingPanesRow::AddPaneFromRow](#addpanefromrow)||
|[CDockingPanesRow：： ArrangePanes](#arrangepanes)|根据指定边距和间距参数将窗格排成行。|
|[CDockingPanesRow::CalcFixedLayout](#calcfixedlayout)||
|[CDockingPanesRow::Create](#create)||
|[CDockingPanesRow：： ExpandStretchedPanes](#expandstretchedpanes)||
|[CDockingPanesRow：： ExpandStretchedPanesRect](#expandstretchedpanesrect)||
|[CDockingPanesRow::FixupVirtualRects](#fixupvirtualrects)||
|[CDockingPanesRow：： GetAvailableLength](#getavailablelength)||
|[CDockingPanesRow：： GetAvailableSpace](#getavailablespace)||
|[CDockingPanesRow：： GetClientRect](#getclientrect)||
|[CDockingPanesRow：： GetDockSite](#getdocksite)||
|[CDockingPanesRow：： GetExtraSpace](#getextraspace)||
|[CDockingPanesRow：： GetGroupFromPane](#getgroupfrompane)||
|[CDockingPanesRow：： GetID](#getid)||
|[CDockingPanesRow：： GetMaxPaneSize](#getmaxpanesize)||
|[CDockingPanesRow::GetPaneCount](#getpanecount)||
|[CDockingPanesRow：： GetPaneList](#getpanelist)||
|[CDockingPanesRow：： GetRowAlignment](#getrowalignment)||
|[CDockingPanesRow：： GetRowHeight](#getrowheight)||
|[CDockingPanesRow：： GetRowOffset](#getrowoffset)||
|[CDockingPanesRow：： GetVisibleCount](#getvisiblecount)||
|[CDockingPanesRow：： GetWindowRect](#getwindowrect)||
|[CDockingPanesRow::HasPane](#haspane)||
|[CDockingPanesRow::IsEmpty](#isempty)||
|[CDockingPanesRow::IsExclusiveRow](#isexclusiverow)||
|[CDockingPanesRow::IsHorizontal](#ishorizontal)||
|[CDockingPanesRow::IsVisible](#isvisible)||
|[CDockingPanesRow::Move](#move)||
|[CDockingPanesRow::MovePane](#movepane)||
|[CDockingPanesRow::OnResizePane](#onresizepane)||
|[CDockingPanesRow::RedrawAll](#redrawall)||
|[CDockingPanesRow::RemovePane](#removepane)||
|[CDockingPanesRow::ReplacePane](#replacepane)||
|[CDockingPanesRow::RepositionPanes](#repositionpanes)||
|[CDockingPanesRow::Resize](#resize)||
|[CDockingPanesRow::ResizeByPaneDivider](#resizebypanedivider)||
|[CDockingPanesRow::ScreenToClient](#screentoclient)||
|[CDockingPanesRow::SetExtra](#setextra)||
|[CDockingPanesRow::ShowDockSiteRow](#showdocksiterow)||
|[CDockingPanesRow::ShowPane](#showpane)||
|[CDockingPanesRow::UpdateVisibleState](#updatevisiblestate)||

## <a name="remarks"></a>备注

`CDockingPanesRow` 对象由停靠站点对象在内部创建。

## <a name="example"></a>示例

下面的示例演示如何从 `CMFCAutoHideBar` 对象获取 `CDockingPanesRow` 对象。

[!code-cpp[NVC_MFC_RibbonApp#26](../../mfc/reference/codesnippet/cpp/cdockingpanesrow-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>继承层次结构

[CObject](../../mfc/reference/cobject-class.md)

[CDockingPanesRow](../../mfc/reference/cdockingpanesrow-class.md)

## <a name="requirements"></a>要求

**标头：** afxDockingPanesRow

## <a name="cdockingpanesrowaddpane"></a><a name="addpane"></a> CDockingPanesRow：： AddPane

```
virtual void AddPane(
    CPane* pControlBar,
    AFX_DOCK_METHOD dockMethod,
    LPCRECT lpRect = NULL,
    BOOL bAddLast = FALSE);
```

### <a name="parameters"></a>parameters

中 *pControlBar*<br/>

中 *dockMethod*<br/>

中 *lpRect*<br/>

中 *bAddLast*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowaddpanefromrow"></a><a name="addpanefromrow"></a> CDockingPanesRow：： AddPaneFromRow

```
virtual void AddPaneFromRow(
    CPane* pControlBar,
    AFX_DOCK_METHOD dockMethod);
```

### <a name="parameters"></a>parameters

中 *pControlBar*<br/>

中 *dockMethod*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowarrangepanes"></a><a name="arrangepanes"></a> CDockingPanesRow：： ArrangePanes

根据指定的边距和间距参数将停靠窗格排列在一行中。

```
virtual void ArrangePanes(
    int nMargin,
    int nSpacing);
```

### <a name="parameters"></a>parameters

*nMargin*<br/>
中指定行左上角第一个窗格的偏移量（以像素为单位）。

*nSpacing*<br/>
中指定窗格之间的间距（以像素为单位）。

### <a name="remarks"></a>备注

调用此方法以在其将停靠的行中排列窗格。 调用此方法后，必须调用 `CDockingPanesRow::FixupVirtualRects(FALSE, NULL)` 。

## <a name="cdockingpanesrowcalcfixedlayout"></a><a name="calcfixedlayout"></a> CDockingPanesRow：： CalcFixedLayout

```
virtual CSize CalcFixedLayout(
    BOOL bStretch,
    BOOL bHorz);
```

### <a name="parameters"></a>parameters

中 *bStretch*<br/>

中 *bHorz*<br/>

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowcdockingpanesrow"></a><a name="cdockingpanesrow"></a> CDockingPanesRow：： CDockingPanesRow

```
CDockingPanesRow(
    CDockSite* pParentDockBar,
    int nOffset,
    int nHeight);
```

### <a name="parameters"></a>parameters

中 *pParentDockBar*<br/>

中 *nOffset*<br/>

中 *nHeight*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowcreate"></a><a name="create"></a> CDockingPanesRow：： Create

```
virtual BOOL Create();
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowexpandstretchedpanes"></a><a name="expandstretchedpanes"></a> CDockingPanesRow：： ExpandStretchedPanes

```cpp
void ExpandStretchedPanes();
```

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowexpandstretchedpanesrect"></a><a name="expandstretchedpanesrect"></a> CDockingPanesRow：： ExpandStretchedPanesRect

```cpp
void ExpandStretchedPanesRect();
```

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowfixupvirtualrects"></a><a name="fixupvirtualrects"></a> CDockingPanesRow：： FixupVirtualRects

```cpp
void FixupVirtualRects(
    bool bMoveBackToVirtualRect,
    CPane* pBarToExclude = NULL);
```

### <a name="parameters"></a>parameters

中 *bMoveBackToVirtualRect*<br/>

中 *pBarToExclude*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetavailablelength"></a><a name="getavailablelength"></a> CDockingPanesRow：： GetAvailableLength

```
virtual int GetAvailableLength(BOOL bUseVirtualRect = FALSE) const;
```

### <a name="parameters"></a>parameters

中 *bUseVirtualRect*<br/>

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetavailablespace"></a><a name="getavailablespace"></a> CDockingPanesRow：： GetAvailableSpace

```
virtual void GetAvailableSpace(CRect& rect);
```

### <a name="parameters"></a>parameters

中 *rect*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetclientrect"></a><a name="getclientrect"></a> CDockingPanesRow：： GetClientRect

```cpp
void GetClientRect(CRect& rect) const;
```

### <a name="parameters"></a>parameters

中 *rect*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetdocksite"></a><a name="getdocksite"></a> CDockingPanesRow：： GetDockSite

```
CDockSite* GetDockSite() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetextraspace"></a><a name="getextraspace"></a> CDockingPanesRow：： GetExtraSpace

```
int GetExtraSpace() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetgroupfrompane"></a><a name="getgroupfrompane"></a> CDockingPanesRow：： GetGroupFromPane

```cpp
void GetGroupFromPane(
    CPane* pBar,
    CObList& lst);
```

### <a name="parameters"></a>parameters

中 *pBar*<br/>

中 *.lst*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetid"></a><a name="getid"></a> CDockingPanesRow：： GetID

```
int GetID() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetmaxpanesize"></a><a name="getmaxpanesize"></a> CDockingPanesRow：： GetMaxPaneSize

```
int GetMaxPaneSize(BOOL bSkipHiddenBars = TRUE) const;
```

### <a name="parameters"></a>parameters

中 *bSkipHiddenBars*<br/>

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetpanecount"></a><a name="getpanecount"></a> CDockingPanesRow：： GetPaneCount

```
int GetPaneCount() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetpanelist"></a><a name="getpanelist"></a> CDockingPanesRow：： GetPaneList

```
const CObList& GetPaneList() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetrowalignment"></a><a name="getrowalignment"></a> CDockingPanesRow：： GetRowAlignment

```
DWORD GetRowAlignment() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetrowheight"></a><a name="getrowheight"></a> CDockingPanesRow：： GetRowHeight

```
int GetRowHeight() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetrowoffset"></a><a name="getrowoffset"></a> CDockingPanesRow：： GetRowOffset

```
int GetRowOffset() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetvisiblecount"></a><a name="getvisiblecount"></a> CDockingPanesRow：： GetVisibleCount

```
virtual int GetVisibleCount();
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowgetwindowrect"></a><a name="getwindowrect"></a> CDockingPanesRow：： GetWindowRect

```cpp
void GetWindowRect(CRect& rect) const;
```

### <a name="parameters"></a>parameters

中 *rect*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowhaspane"></a><a name="haspane"></a> CDockingPanesRow：： HasPane

```
BOOL HasPane(CBasePane* pControlBar);
```

### <a name="parameters"></a>parameters

中 *pControlBar*<br/>

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowisempty"></a><a name="isempty"></a> CDockingPanesRow：： IsEmpty

```
virtual BOOL IsEmpty() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowisexclusiverow"></a><a name="isexclusiverow"></a> CDockingPanesRow：： IsExclusiveRow

```
virtual BOOL IsExclusiveRow() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowishorizontal"></a><a name="ishorizontal"></a> CDockingPanesRow：： IsHorizontal

```
bool IsHorizontal() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowisvisible"></a><a name="isvisible"></a> CDockingPanesRow：： IsVisible

```
virtual BOOL IsVisible() const;
```

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowmove"></a><a name="move"></a> CDockingPanesRow：： Move

```
virtual void Move(int nOffset);
```

### <a name="parameters"></a>parameters

中 *nOffset*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowmovepane"></a><a name="movepane"></a> CDockingPanesRow：： MovePane

```cpp
void MovePane(
    CPane* pControlBar,
    CPoint ptOffset,
    BOOL bSwapControlBars,
    HDWP& hdwp);

void MovePane(
    CPane* pControlBar,
    CRect rectTarget,
    HDWP& hdwp);

void MovePane(
    CPane* pControlBar,
    int nOffset,
    bool bForward,
    HDWP& hdwp);

void MovePane(
    CPane* pControlBar,
    int nAbsolutOffset,
    HDWP& hdwp);
```

### <a name="parameters"></a>parameters

中 *pControlBar*<br/>

中 *ptOffset*<br/>

中 *bSwapControlBars*<br/>

中 *hdwp*<br/>

中 *rectTarget*<br/>

中 *nOffset*<br/>

中 *bForward*<br/>

中 *nAbsolutOffset*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowonresizepane"></a><a name="onresizepane"></a> CDockingPanesRow：： OnResizePane

```
virtual void OnResizePane(CBasePane* pControlBar);
```

### <a name="parameters"></a>parameters

中 *pControlBar*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowredrawall"></a><a name="redrawall"></a> CDockingPanesRow：： RedrawAll

```cpp
void RedrawAll();
```

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowremovepane"></a><a name="removepane"></a> CDockingPanesRow：： RemovePane

```
virtual void RemovePane(CPane* pControlBar);
```

### <a name="parameters"></a>parameters

中 *pControlBar*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowreplacepane"></a><a name="replacepane"></a> CDockingPanesRow：： ReplacePane

```
virtual BOOL ReplacePane(
    CPane* pBarOld,
    CPane* pBarNew);
```

### <a name="parameters"></a>parameters

中 *pBarOld*<br/>

中 *pBarNew*<br/>

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowrepositionpanes"></a><a name="repositionpanes"></a> CDockingPanesRow：： RepositionPanes

```
virtual void RepositionPanes(
    CRect& rectNewParentBarArea,
    UINT nSide = (UINT)-1,
    BOOL bExpand = FALSE,
    int nOffset = 0);
```

### <a name="parameters"></a>parameters

中 *rectNewParentBarArea*<br/>

中 *nSide*<br/>

中 *bExpand*<br/>

中 *nOffset*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowresize"></a><a name="resize"></a> CDockingPanesRow：： Resize

```
virtual int Resize(int nOffset);
```

### <a name="parameters"></a>parameters

中 *nOffset*<br/>

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowresizebypanedivider"></a><a name="resizebypanedivider"></a> CDockingPanesRow：： ResizeByPaneDivider

```
virtual int ResizeByPaneDivider(int /*ignored*/);
```

### <a name="parameters"></a>parameters

中已 *忽略*<br/>

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowscreentoclient"></a><a name="screentoclient"></a> CDockingPanesRow：： ScreenToClient

```cpp
void ScreenToClient(CRect& rect) const;
```

### <a name="parameters"></a>parameters

中 *rect*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowsetextra"></a><a name="setextra"></a> CDockingPanesRow：： SetExtra

```cpp
void SetExtra(
    int nExtraSpace,
    AFX_ROW_ALIGNMENT rowExtraAlign);
```

### <a name="parameters"></a>parameters

中 *nExtraSpace*<br/>

中 *rowExtraAlign*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowshowdocksiterow"></a><a name="showdocksiterow"></a> CDockingPanesRow：： ShowDockSiteRow

```
virtual void ShowDockSiteRow(
    BOOL bShow,
    BOOL bDelay);
```

### <a name="parameters"></a>parameters

中 *bShow*<br/>

中 *bDelay*<br/>

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowshowpane"></a><a name="showpane"></a> CDockingPanesRow：： ShowPane

```
virtual BOOL ShowPane(
    CPane* pControlBar,
    BOOL bShow,
    BOOL bDelay = FALSE);
```

### <a name="parameters"></a>parameters

中 *pControlBar*<br/>

中 *bShow*<br/>

中 *bDelay*<br/>

### <a name="return-value"></a>返回值

### <a name="remarks"></a>备注

## <a name="cdockingpanesrowupdatevisiblestate"></a><a name="updatevisiblestate"></a> CDockingPanesRow：： UpdateVisibleState

```
virtual void UpdateVisibleState(BOOL bDelay);
```

### <a name="parameters"></a>parameters

中 *bDelay*<br/>

### <a name="remarks"></a>备注

## <a name="see-also"></a>请参阅

[层次结构图](../../mfc/hierarchy-chart.md)<br/>
[Classes](../../mfc/reference/mfc-classes.md)<br/>
[CObject 类](../../mfc/reference/cobject-class.md)<br/>
[CDockSite 类](../../mfc/reference/cdocksite-class.md)<br/>
[CPane 类](../../mfc/reference/cpane-class.md)
