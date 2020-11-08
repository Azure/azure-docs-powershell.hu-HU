---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013411"
---
# <span data-ttu-id="a1ec6-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a1ec6-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="a1ec6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ec6-103">Beilleszti egy eszköz konfigurált felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="a1ec6-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="a1ec6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1ec6-104">SYNTAX</span></span>

### <span data-ttu-id="a1ec6-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1ec6-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ec6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1ec6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ec6-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1ec6-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ec6-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1ec6-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a1ec6-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1ec6-109">DESCRIPTION</span></span>
<span data-ttu-id="a1ec6-110">A **Get-AzDataBoxEdgeUser** parancsmag felsorolja azokat a felhasználókat, akiknek konfigurálva van az adatmező szélén lévő eszköz.</span><span class="sxs-lookup"><span data-stu-id="a1ec6-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="a1ec6-111">Ha egy adott felhasználóról szeretne részleteket bemutatni, a paraméterekben Megemlítheti a nevet.</span><span class="sxs-lookup"><span data-stu-id="a1ec6-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="a1ec6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a1ec6-112">EXAMPLES</span></span>

### <span data-ttu-id="a1ec6-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a1ec6-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="a1ec6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1ec6-114">PARAMETERS</span></span>

### <span data-ttu-id="a1ec6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ec6-115">-DefaultProfile</span></span>
<span data-ttu-id="a1ec6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1ec6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ec6-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a1ec6-117">-DeviceName</span></span>
<span data-ttu-id="a1ec6-118">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="a1ec6-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ec6-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a1ec6-119">-DeviceObject</span></span>
<span data-ttu-id="a1ec6-120">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="a1ec6-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ec6-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1ec6-121">-Name</span></span>
<span data-ttu-id="a1ec6-122">Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="a1ec6-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ec6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1ec6-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1ec6-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a1ec6-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ec6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1ec6-125">-ResourceId</span></span>
<span data-ttu-id="a1ec6-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1ec6-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ec6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ec6-127">CommonParameters</span></span>
<span data-ttu-id="a1ec6-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1ec6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ec6-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1ec6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ec6-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1ec6-130">INPUTS</span></span>

### <span data-ttu-id="a1ec6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a1ec6-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a1ec6-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1ec6-132">OUTPUTS</span></span>

### <span data-ttu-id="a1ec6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a1ec6-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="a1ec6-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1ec6-134">NOTES</span></span>

## <span data-ttu-id="a1ec6-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1ec6-135">RELATED LINKS</span></span>
