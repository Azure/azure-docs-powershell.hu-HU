---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012172"
---
# <span data-ttu-id="b37c7-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="b37c7-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="b37c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b37c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b37c7-103">Információt kap a Databox-feladatokról</span><span class="sxs-lookup"><span data-stu-id="b37c7-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="b37c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b37c7-104">SYNTAX</span></span>

### <span data-ttu-id="b37c7-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b37c7-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b37c7-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b37c7-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b37c7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b37c7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b37c7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b37c7-108">DESCRIPTION</span></span>
<span data-ttu-id="b37c7-109">A **Get-AzDataBoxJobs** parancsmag az Azure-előfizetések databox-feladatairól kap információkat.</span><span class="sxs-lookup"><span data-stu-id="b37c7-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="b37c7-110">Ha megadja az erőforráscsoport, ez a parancsmag az adott erőforráscsoport alatti összes databox-feladatot kapja.</span><span class="sxs-lookup"><span data-stu-id="b37c7-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="b37c7-111">Ha a feladat nevét az erőforráscsoport nevével együtt adja meg, ez a parancsmag információkat kap az adott databox-feladatról.</span><span class="sxs-lookup"><span data-stu-id="b37c7-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="b37c7-112">Ha nem ad meg semmit, mint az előfizetés azonosítóját, ez a parancsmag információkat kap az előfizetés alatti összes databox-feladatról.</span><span class="sxs-lookup"><span data-stu-id="b37c7-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="b37c7-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b37c7-113">EXAMPLES</span></span>

### <span data-ttu-id="b37c7-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b37c7-114">Example 1</span></span>
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

<span data-ttu-id="b37c7-115">Get-AzDataBoxJob paraméter nélkül az előfizetésben szereplő összes databox-feladatot lehívja.</span><span class="sxs-lookup"><span data-stu-id="b37c7-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="b37c7-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="b37c7-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="b37c7-117">Get-AzDataBoxJob a ResourceGroupName paraméterrel beolvassa a megadott erőforráscsoport alatti összes databox-feladatot.</span><span class="sxs-lookup"><span data-stu-id="b37c7-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="b37c7-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="b37c7-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="b37c7-119">Get-AzDataBoxJob a ResourceGroupName és a megadott névvel, az adott databox feladatot fogja beolvasni.</span><span class="sxs-lookup"><span data-stu-id="b37c7-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="b37c7-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="b37c7-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="b37c7-121">Get-AzDataBoxJob a megadott ResourceId az adott databox feladatot fogja beolvasni.</span><span class="sxs-lookup"><span data-stu-id="b37c7-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="b37c7-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b37c7-122">PARAMETERS</span></span>

### <span data-ttu-id="b37c7-123">-Megszakadt</span><span class="sxs-lookup"><span data-stu-id="b37c7-123">-Aborted</span></span>
<span data-ttu-id="b37c7-124">Paraméter váltása a megszakított feladatok beolvasásához</span><span class="sxs-lookup"><span data-stu-id="b37c7-124">Switch Parameter to fetch Aborted jobs</span></span>

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

### <span data-ttu-id="b37c7-125">-Visszavonva</span><span class="sxs-lookup"><span data-stu-id="b37c7-125">-Cancelled</span></span>
<span data-ttu-id="b37c7-126">Paraméter váltása a lemondott feladatok beolvasásához</span><span class="sxs-lookup"><span data-stu-id="b37c7-126">Switch Parameter to fetch Cancelled jobs</span></span>

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

### <span data-ttu-id="b37c7-127">– Befejezett</span><span class="sxs-lookup"><span data-stu-id="b37c7-127">-Completed</span></span>
<span data-ttu-id="b37c7-128">Paraméter váltása a Befejezett feladatok beolvasásához</span><span class="sxs-lookup"><span data-stu-id="b37c7-128">Switch Parameter to fetch Completed jobs</span></span>

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

### <span data-ttu-id="b37c7-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="b37c7-129">-CompletedWithError</span></span>
<span data-ttu-id="b37c7-130">Váltás a paraméterekkel Befejezett feladatok lehívására</span><span class="sxs-lookup"><span data-stu-id="b37c7-130">Switch Parameter to fetch jobs completed with errors</span></span>

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

### <span data-ttu-id="b37c7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37c7-131">-DefaultProfile</span></span>
<span data-ttu-id="b37c7-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b37c7-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b37c7-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b37c7-133">-Name</span></span>
<span data-ttu-id="b37c7-134">Databox-feladat neve</span><span class="sxs-lookup"><span data-stu-id="b37c7-134">Databox Job Name</span></span>

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

### <span data-ttu-id="b37c7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b37c7-135">-ResourceGroupName</span></span>
<span data-ttu-id="b37c7-136">Databox-munka erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="b37c7-136">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="b37c7-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b37c7-137">-ResourceId</span></span>
<span data-ttu-id="b37c7-138">Databox munka erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b37c7-138">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="b37c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37c7-139">CommonParameters</span></span>
<span data-ttu-id="b37c7-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b37c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37c7-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b37c7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37c7-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b37c7-142">INPUTS</span></span>

### <span data-ttu-id="b37c7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b37c7-143">System.String</span></span>

## <span data-ttu-id="b37c7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b37c7-144">OUTPUTS</span></span>

### <span data-ttu-id="b37c7-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="b37c7-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="b37c7-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b37c7-146">NOTES</span></span>

## <span data-ttu-id="b37c7-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b37c7-147">RELATED LINKS</span></span>
