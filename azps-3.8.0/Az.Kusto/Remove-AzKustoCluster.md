---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 1949cc2a875f2e55c2d35dcbbd7b062ff2cae021
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011129"
---
# <span data-ttu-id="27100-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="27100-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="27100-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27100-102">SYNOPSIS</span></span>
<span data-ttu-id="27100-103">Töröl egy meglévő Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="27100-103">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="27100-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27100-104">SYNTAX</span></span>

### <span data-ttu-id="27100-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27100-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27100-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27100-106">ByResourceId</span></span>
```
Remove-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27100-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27100-107">ByInputObject</span></span>
```
Remove-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27100-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="27100-108">DESCRIPTION</span></span>
<span data-ttu-id="27100-109">Töröl egy meglévő Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="27100-109">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="27100-110">Példák</span><span class="sxs-lookup"><span data-stu-id="27100-110">EXAMPLES</span></span>

### <span data-ttu-id="27100-111">Példa 1 – meglévő Kusto-fürt törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="27100-111">Example 1 - Delete an existing Kusto cluster by name</span></span>

```
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="27100-112">A fenti parancs törli a "mykustocluster" nevű Kusto-fürtöt az "testrg" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="27100-112">The above command deletes the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="27100-113">2. példa – meglévő Kusto-fürt törlése csővezetékről</span><span class="sxs-lookup"><span data-stu-id="27100-113">Example 2 - Delete an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Remove-AzKustoCluster
```

<span data-ttu-id="27100-114">A fenti parancs az "mykustocluster" nevű Kusto-fürtöt az "testrg" erőforráscsoport nevében a `Get-AzKustoCluster` parancsmag használatával kapja, majd az eredményt a `Remove-AzKustoCluster` törléséhez.</span><span class="sxs-lookup"><span data-stu-id="27100-114">The above command gets the Kusto cluster named "mykustocluster" in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Remove-AzKustoCluster` to delete it.</span></span>

## <span data-ttu-id="27100-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27100-115">PARAMETERS</span></span>

### <span data-ttu-id="27100-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27100-116">-DefaultProfile</span></span>
<span data-ttu-id="27100-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27100-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27100-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27100-118">-InputObject</span></span>
<span data-ttu-id="27100-119">Kusto.</span><span class="sxs-lookup"><span data-stu-id="27100-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="27100-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="27100-120">-Name</span></span>
<span data-ttu-id="27100-121">Eltávolítandó szektorcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="27100-121">Name of cluster to be removed.</span></span>

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

### <span data-ttu-id="27100-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27100-122">-PassThru</span></span>
<span data-ttu-id="27100-123">Annak megadása, hogy a megadott fürtöt sikeresen törölték-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="27100-123">Return whether the specified cluster was successfully deleted or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27100-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27100-124">-ResourceGroupName</span></span>
<span data-ttu-id="27100-125">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="27100-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="27100-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27100-126">-ResourceId</span></span>
<span data-ttu-id="27100-127">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="27100-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="27100-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27100-128">-Confirm</span></span>
<span data-ttu-id="27100-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27100-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27100-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27100-130">-WhatIf</span></span>
<span data-ttu-id="27100-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27100-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27100-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27100-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27100-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27100-133">CommonParameters</span></span>
<span data-ttu-id="27100-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27100-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27100-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27100-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27100-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27100-136">INPUTS</span></span>

### <span data-ttu-id="27100-137">System. String</span><span class="sxs-lookup"><span data-stu-id="27100-137">System.String</span></span>

### <span data-ttu-id="27100-138">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="27100-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="27100-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27100-139">OUTPUTS</span></span>

### <span data-ttu-id="27100-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27100-140">System.Boolean</span></span>

## <span data-ttu-id="27100-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27100-141">NOTES</span></span>

## <span data-ttu-id="27100-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27100-142">RELATED LINKS</span></span>
