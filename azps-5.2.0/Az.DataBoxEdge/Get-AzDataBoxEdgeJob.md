---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330353"
---
# <span data-ttu-id="d08bf-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="d08bf-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="d08bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d08bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d08bf-103">Egy eszközön ütemezi a feladatokat.</span><span class="sxs-lookup"><span data-stu-id="d08bf-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="d08bf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d08bf-104">SYNTAX</span></span>

### <span data-ttu-id="d08bf-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d08bf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d08bf-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="d08bf-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d08bf-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d08bf-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="d08bf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d08bf-108">DESCRIPTION</span></span>
<span data-ttu-id="d08bf-109">A **Get-AzDataBoxEdgeCm** parancsmag aktív feladatokat kap egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="d08bf-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="d08bf-110">Megemlítheti a Name paramétert egy adott feladat részleteinek lekértérte.</span><span class="sxs-lookup"><span data-stu-id="d08bf-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="d08bf-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d08bf-111">EXAMPLES</span></span>

### <span data-ttu-id="d08bf-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d08bf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="d08bf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d08bf-113">PARAMETERS</span></span>

### <span data-ttu-id="d08bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08bf-114">-DefaultProfile</span></span>
<span data-ttu-id="d08bf-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d08bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d08bf-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d08bf-116">-DeviceName</span></span>
<span data-ttu-id="d08bf-117">Az eszköz neve</span><span class="sxs-lookup"><span data-stu-id="d08bf-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bf-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d08bf-118">-DeviceObject</span></span>
<span data-ttu-id="d08bf-119">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="d08bf-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="d08bf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d08bf-120">-Name</span></span>
<span data-ttu-id="d08bf-121">A feladat neve, általánosan guid azonosító</span><span class="sxs-lookup"><span data-stu-id="d08bf-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d08bf-122">-ResourceGroupName</span></span>
<span data-ttu-id="d08bf-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d08bf-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d08bf-124">-ResourceId</span></span>
<span data-ttu-id="d08bf-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d08bf-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08bf-126">CommonParameters</span></span>
<span data-ttu-id="d08bf-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d08bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08bf-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d08bf-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08bf-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d08bf-129">INPUTS</span></span>

### <span data-ttu-id="d08bf-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d08bf-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="d08bf-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d08bf-131">OUTPUTS</span></span>

### <span data-ttu-id="d08bf-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="d08bf-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="d08bf-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d08bf-133">NOTES</span></span>

## <span data-ttu-id="d08bf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d08bf-134">RELATED LINKS</span></span>
