---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 5f2dfec045364852d9846fa3bb35bd903c78ca5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186516"
---
# <span data-ttu-id="9d292-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9d292-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="9d292-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d292-102">SYNOPSIS</span></span>
<span data-ttu-id="9d292-103">Információt kap a sávszélesség-ütemtervekről</span><span class="sxs-lookup"><span data-stu-id="9d292-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="9d292-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d292-104">SYNTAX</span></span>

### <span data-ttu-id="9d292-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d292-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d292-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d292-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d292-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d292-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d292-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d292-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="9d292-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d292-109">DESCRIPTION</span></span>
<span data-ttu-id="9d292-110">A **Get-AzStackEdgeBandwidthSchedule** parancsmag a sávszélesség-ütemtervekre vonatkozó információkat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9d292-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="9d292-111">Az ütemezés nevét az erőforráscsoport neve és az eszköz neve mellett megadhatja, hogy egy adott sávszélesség-ütemezésről szeretne információt kapni.</span><span class="sxs-lookup"><span data-stu-id="9d292-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="9d292-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9d292-112">EXAMPLES</span></span>

### <span data-ttu-id="9d292-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9d292-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="9d292-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9d292-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="9d292-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d292-115">PARAMETERS</span></span>

### <span data-ttu-id="9d292-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d292-116">-DefaultProfile</span></span>
<span data-ttu-id="9d292-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d292-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d292-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9d292-118">-DeviceName</span></span>
<span data-ttu-id="9d292-119">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="9d292-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d292-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9d292-120">-DeviceObject</span></span>
<span data-ttu-id="9d292-121">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="9d292-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d292-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d292-122">-Name</span></span>
<span data-ttu-id="9d292-123">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="9d292-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: BandwidthScheduleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d292-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d292-124">-ResourceGroupName</span></span>
<span data-ttu-id="9d292-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9d292-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d292-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d292-126">-ResourceId</span></span>
<span data-ttu-id="9d292-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d292-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="9d292-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d292-128">CommonParameters</span></span>
<span data-ttu-id="9d292-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d292-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d292-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9d292-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d292-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d292-131">INPUTS</span></span>

### <span data-ttu-id="9d292-132">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9d292-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="9d292-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d292-133">OUTPUTS</span></span>

### <span data-ttu-id="9d292-134">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9d292-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="9d292-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d292-135">NOTES</span></span>

## <span data-ttu-id="9d292-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d292-136">RELATED LINKS</span></span>
