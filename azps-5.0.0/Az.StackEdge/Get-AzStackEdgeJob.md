---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187988"
---
# <span data-ttu-id="8a169-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="8a169-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="8a169-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a169-102">SYNOPSIS</span></span>
<span data-ttu-id="8a169-103">Az eszközön ütemezett feladatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="8a169-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="8a169-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a169-104">SYNTAX</span></span>

### <span data-ttu-id="8a169-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a169-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a169-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="8a169-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a169-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a169-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8a169-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a169-108">DESCRIPTION</span></span>
<span data-ttu-id="8a169-109">A **Get-AzStackEdgeJob** parancsmag az aktív feladatokat egy halom szélén álló eszközön kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8a169-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="8a169-110">Megemlítheti a Name (név) paramétert egy adott feladat részleteinek beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="8a169-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="8a169-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8a169-111">EXAMPLES</span></span>

### <span data-ttu-id="8a169-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8a169-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="8a169-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a169-113">PARAMETERS</span></span>

### <span data-ttu-id="8a169-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a169-114">-DefaultProfile</span></span>
<span data-ttu-id="8a169-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a169-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a169-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8a169-116">-DeviceName</span></span>
<span data-ttu-id="8a169-117">Az eszköz neve</span><span class="sxs-lookup"><span data-stu-id="8a169-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a169-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8a169-118">-DeviceObject</span></span>
<span data-ttu-id="8a169-119">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="8a169-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a169-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a169-120">-Name</span></span>
<span data-ttu-id="8a169-121">A feladat neve általában egy globálisan egyedi azonosító</span><span class="sxs-lookup"><span data-stu-id="8a169-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a169-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a169-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a169-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8a169-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a169-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a169-124">-ResourceId</span></span>
<span data-ttu-id="8a169-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a169-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a169-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a169-126">CommonParameters</span></span>
<span data-ttu-id="8a169-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a169-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a169-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8a169-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a169-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a169-129">INPUTS</span></span>

### <span data-ttu-id="8a169-130">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8a169-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="8a169-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a169-131">OUTPUTS</span></span>

### <span data-ttu-id="8a169-132">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="8a169-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="8a169-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a169-133">NOTES</span></span>

## <span data-ttu-id="8a169-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a169-134">RELATED LINKS</span></span>
