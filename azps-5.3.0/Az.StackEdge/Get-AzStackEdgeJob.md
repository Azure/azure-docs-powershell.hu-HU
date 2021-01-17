---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480313"
---
# <span data-ttu-id="3bf3e-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="3bf3e-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="3bf3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bf3e-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf3e-103">Eszközre ütemezi a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="3bf3e-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="3bf3e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3bf3e-104">SYNTAX</span></span>

### <span data-ttu-id="3bf3e-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bf3e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bf3e-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="3bf3e-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bf3e-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bf3e-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="3bf3e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3bf3e-108">DESCRIPTION</span></span>
<span data-ttu-id="3bf3e-109">A **Get-AzStackEdge Jobs** parancsmag az aktív feladatokat egy Stack Edge eszközön kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3bf3e-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="3bf3e-110">Megemlítheti a Name paramétert egy adott feladat részleteinek lekértérte.</span><span class="sxs-lookup"><span data-stu-id="3bf3e-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="3bf3e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3bf3e-111">EXAMPLES</span></span>

### <span data-ttu-id="3bf3e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3bf3e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="3bf3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bf3e-113">PARAMETERS</span></span>

### <span data-ttu-id="3bf3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf3e-114">-DefaultProfile</span></span>
<span data-ttu-id="3bf3e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bf3e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bf3e-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3bf3e-116">-DeviceName</span></span>
<span data-ttu-id="3bf3e-117">Az eszköz neve</span><span class="sxs-lookup"><span data-stu-id="3bf3e-117">Name of the device</span></span>

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

### <span data-ttu-id="3bf3e-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="3bf3e-118">-DeviceObject</span></span>
<span data-ttu-id="3bf3e-119">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="3bf3e-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3bf3e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3bf3e-120">-Name</span></span>
<span data-ttu-id="3bf3e-121">A feladat neve, általánosan guid azonosító</span><span class="sxs-lookup"><span data-stu-id="3bf3e-121">Name of the Job, Generally a GUID</span></span>

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

### <span data-ttu-id="3bf3e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bf3e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3bf3e-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3bf3e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3bf3e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf3e-124">-ResourceId</span></span>
<span data-ttu-id="3bf3e-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bf3e-125">Azure ResourceId</span></span>

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

### <span data-ttu-id="3bf3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf3e-126">CommonParameters</span></span>
<span data-ttu-id="3bf3e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bf3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf3e-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bf3e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf3e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bf3e-129">INPUTS</span></span>

### <span data-ttu-id="3bf3e-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3bf3e-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="3bf3e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bf3e-131">OUTPUTS</span></span>

### <span data-ttu-id="3bf3e-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeSor</span><span class="sxs-lookup"><span data-stu-id="3bf3e-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="3bf3e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3bf3e-133">NOTES</span></span>

## <span data-ttu-id="3bf3e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bf3e-134">RELATED LINKS</span></span>
