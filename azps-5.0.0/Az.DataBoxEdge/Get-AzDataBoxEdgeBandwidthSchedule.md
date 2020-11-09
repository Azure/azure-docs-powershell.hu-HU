---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e3453e3359bb800180ebdeb3fa5158b890fd237a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298868"
---
# <span data-ttu-id="723b1-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="723b1-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="723b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="723b1-102">SYNOPSIS</span></span>
<span data-ttu-id="723b1-103">Információt kap a sávszélesség-ütemtervekről</span><span class="sxs-lookup"><span data-stu-id="723b1-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="723b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="723b1-104">SYNTAX</span></span>

### <span data-ttu-id="723b1-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="723b1-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="723b1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="723b1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="723b1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="723b1-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="723b1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="723b1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="723b1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="723b1-109">DESCRIPTION</span></span>
<span data-ttu-id="723b1-110">A **Get-AzDataBoxEdgeBandwidthSchedule** parancsmag a sávszélesség-ütemtervekre vonatkozó információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="723b1-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="723b1-111">Az ütemezés nevét az erőforráscsoport neve és az eszköz neve mellett megadhatja, hogy egy adott sávszélesség-ütemezésről szeretne információt kapni.</span><span class="sxs-lookup"><span data-stu-id="723b1-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="723b1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="723b1-112">EXAMPLES</span></span>

### <span data-ttu-id="723b1-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="723b1-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="723b1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="723b1-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="723b1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="723b1-115">PARAMETERS</span></span>

### <span data-ttu-id="723b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723b1-116">-DefaultProfile</span></span>
<span data-ttu-id="723b1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="723b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="723b1-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="723b1-118">-DeviceName</span></span>
<span data-ttu-id="723b1-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="723b1-119">Device Name</span></span>

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

### <span data-ttu-id="723b1-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="723b1-120">-DeviceObject</span></span>
<span data-ttu-id="723b1-121">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="723b1-121">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="723b1-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="723b1-122">-Name</span></span>
<span data-ttu-id="723b1-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="723b1-123">Resource Name</span></span>

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

### <span data-ttu-id="723b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="723b1-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="723b1-125">Resource Group Name</span></span>

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

### <span data-ttu-id="723b1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="723b1-126">-ResourceId</span></span>
<span data-ttu-id="723b1-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="723b1-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="723b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723b1-128">CommonParameters</span></span>
<span data-ttu-id="723b1-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="723b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723b1-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="723b1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723b1-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="723b1-131">INPUTS</span></span>

### <span data-ttu-id="723b1-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="723b1-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="723b1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="723b1-133">OUTPUTS</span></span>

### <span data-ttu-id="723b1-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="723b1-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="723b1-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="723b1-135">NOTES</span></span>

## <span data-ttu-id="723b1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="723b1-136">RELATED LINKS</span></span>
