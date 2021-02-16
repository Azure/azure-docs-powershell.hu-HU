---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144403"
---
# <span data-ttu-id="5ba9d-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="5ba9d-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="5ba9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba9d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba9d-103">Információkat kap a Databox-feladatokról</span><span class="sxs-lookup"><span data-stu-id="5ba9d-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="5ba9d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ba9d-104">SYNTAX</span></span>

### <span data-ttu-id="5ba9d-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ba9d-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ba9d-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ba9d-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ba9d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ba9d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba9d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ba9d-108">DESCRIPTION</span></span>
<span data-ttu-id="5ba9d-109">A **Get-AzDataBox Jobss** parancsmag információkat kap az Azure-előfizetésben található adatkapcsolatú feladatokról.</span><span class="sxs-lookup"><span data-stu-id="5ba9d-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="5ba9d-110">Ha megadja az erőforráscsoportot, ez a parancsmag az adott erőforráscsoport összes adatdoboz-feladatát megkapja.</span><span class="sxs-lookup"><span data-stu-id="5ba9d-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="5ba9d-111">Ha megadja a feladat nevét az erőforráscsoport nevével együtt, ez a parancsmag információt kap az adott adatdoboz-feladatról.</span><span class="sxs-lookup"><span data-stu-id="5ba9d-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="5ba9d-112">Ha nem ad meg semmit, csak az előfizetés azonosítóját, ez a parancsmag információt kap az adott előfizetésben található összes adatdoboz-feladatról.</span><span class="sxs-lookup"><span data-stu-id="5ba9d-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="5ba9d-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ba9d-113">EXAMPLES</span></span>

### <span data-ttu-id="5ba9d-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="5ba9d-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="5ba9d-115">Get-AzDataBoxJob nélküli lekérdezés az előfizetés összes adatbox-feladatát lehívja</span><span class="sxs-lookup"><span data-stu-id="5ba9d-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="5ba9d-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="5ba9d-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="5ba9d-117">Get-AzDataBoxJob ResourceGroupName paraméterrel való hozzárendelés a megadott erőforráscsoport összes adatbox-feladatát lekéri</span><span class="sxs-lookup"><span data-stu-id="5ba9d-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="5ba9d-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="5ba9d-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="5ba9d-119">Get-AzDataBoxJob ResourceGroupName és Name érték megadva esetén az adott adatdoboz-feladat lekéri</span><span class="sxs-lookup"><span data-stu-id="5ba9d-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="5ba9d-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="5ba9d-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="5ba9d-121">Get-AzDataBoxJob ResourceId érték van megadva, az adott adatkészlet-feladat lehívása</span><span class="sxs-lookup"><span data-stu-id="5ba9d-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="5ba9d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ba9d-122">PARAMETERS</span></span>

### <span data-ttu-id="5ba9d-123">-Megszakítva</span><span class="sxs-lookup"><span data-stu-id="5ba9d-123">-Aborted</span></span>
<span data-ttu-id="5ba9d-124">Switch Parameter to fetch Aborted jobs</span><span class="sxs-lookup"><span data-stu-id="5ba9d-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba9d-125">-Megszakítva</span><span class="sxs-lookup"><span data-stu-id="5ba9d-125">-Cancelled</span></span>
<span data-ttu-id="5ba9d-126">Switch Parameter to fetch Cancelled jobs</span><span class="sxs-lookup"><span data-stu-id="5ba9d-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba9d-127">-Completed</span><span class="sxs-lookup"><span data-stu-id="5ba9d-127">-Completed</span></span>
<span data-ttu-id="5ba9d-128">Switch Parameter to fetch Completed jobs</span><span class="sxs-lookup"><span data-stu-id="5ba9d-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba9d-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="5ba9d-129">-CompletedWithError</span></span>
<span data-ttu-id="5ba9d-130">Switch Parameter to fetch jobs completed with errors</span><span class="sxs-lookup"><span data-stu-id="5ba9d-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba9d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba9d-131">-DefaultProfile</span></span>
<span data-ttu-id="5ba9d-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ba9d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba9d-133">-Name</span><span class="sxs-lookup"><span data-stu-id="5ba9d-133">-Name</span></span>
<span data-ttu-id="5ba9d-134">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="5ba9d-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba9d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba9d-135">-ResourceGroupName</span></span>
<span data-ttu-id="5ba9d-136">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="5ba9d-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba9d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ba9d-137">-ResourceId</span></span>
<span data-ttu-id="5ba9d-138">Databox Job Resource Id</span><span class="sxs-lookup"><span data-stu-id="5ba9d-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba9d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba9d-139">CommonParameters</span></span>
<span data-ttu-id="5ba9d-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba9d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba9d-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ba9d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba9d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ba9d-142">INPUTS</span></span>

### <span data-ttu-id="5ba9d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5ba9d-143">System.String</span></span>

## <span data-ttu-id="5ba9d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ba9d-144">OUTPUTS</span></span>

### <span data-ttu-id="5ba9d-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="5ba9d-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="5ba9d-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ba9d-146">NOTES</span></span>

## <span data-ttu-id="5ba9d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ba9d-147">RELATED LINKS</span></span>
