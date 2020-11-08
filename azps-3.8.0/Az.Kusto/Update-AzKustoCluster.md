---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 0b5e066255a0757c7aaafb6aee6c4ca37d03c7fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011117"
---
# <span data-ttu-id="d6a73-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d6a73-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="d6a73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6a73-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a73-103">Meglévő Kusto-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="d6a73-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="d6a73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6a73-104">SYNTAX</span></span>

### <span data-ttu-id="d6a73-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6a73-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6a73-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6a73-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6a73-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d6a73-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6a73-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6a73-108">DESCRIPTION</span></span>
<span data-ttu-id="d6a73-109">Meglévő Kusto-fürt frissítése</span><span class="sxs-lookup"><span data-stu-id="d6a73-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="d6a73-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d6a73-110">EXAMPLES</span></span>

### <span data-ttu-id="d6a73-111">Példa 1 – meglévő fürt frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="d6a73-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="d6a73-112">A fenti parancs frissíti a "mykustocluster" Kusto-szektorcsoport rétegét az "testrg" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="d6a73-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d6a73-113">2. példa: meglévő fürt frissítése csővezetéken</span><span class="sxs-lookup"><span data-stu-id="d6a73-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="d6a73-114">A fenti parancs az "mykustocluster" Kusto-fürtöt a parancsmag használatával, a "testrg" erőforráscsoport segítségével kapja meg `Get-AzKustoCluster` , majd a csöveket az eredmény a `Update-AzKustoCluster` "normál" értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="d6a73-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="d6a73-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6a73-115">PARAMETERS</span></span>

### <span data-ttu-id="d6a73-116">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="d6a73-116">-Capacity</span></span>
<span data-ttu-id="d6a73-117">A VM példányának száma.</span><span class="sxs-lookup"><span data-stu-id="d6a73-117">The instance number of the VM.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a73-118">-DefaultProfile</span></span>
<span data-ttu-id="d6a73-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6a73-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a73-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6a73-120">-InputObject</span></span>
<span data-ttu-id="d6a73-121">Kusto.</span><span class="sxs-lookup"><span data-stu-id="d6a73-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6a73-122">-Name</span></span>
<span data-ttu-id="d6a73-123">Frissítendő szektorcsoport neve</span><span class="sxs-lookup"><span data-stu-id="d6a73-123">Name of cluster to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a73-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6a73-125">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="d6a73-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6a73-126">-ResourceId</span></span>
<span data-ttu-id="d6a73-127">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="d6a73-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d6a73-128">-SkuName</span></span>
<span data-ttu-id="d6a73-129">A fürt létrehozásához használt SKU neve</span><span class="sxs-lookup"><span data-stu-id="d6a73-129">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-130">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="d6a73-130">-Tier</span></span>
<span data-ttu-id="d6a73-131">A fürt létrehozásához használt szint neve</span><span class="sxs-lookup"><span data-stu-id="d6a73-131">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6a73-132">-Confirm</span></span>
<span data-ttu-id="d6a73-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6a73-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6a73-134">-WhatIf</span></span>
<span data-ttu-id="d6a73-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6a73-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6a73-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6a73-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a73-137">CommonParameters</span></span>
<span data-ttu-id="d6a73-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6a73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a73-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a73-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a73-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6a73-140">INPUTS</span></span>

### <span data-ttu-id="d6a73-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d6a73-141">System.String</span></span>

### <span data-ttu-id="d6a73-142">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d6a73-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d6a73-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6a73-143">OUTPUTS</span></span>

### <span data-ttu-id="d6a73-144">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d6a73-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="d6a73-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6a73-145">NOTES</span></span>

## <span data-ttu-id="d6a73-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6a73-146">RELATED LINKS</span></span>
