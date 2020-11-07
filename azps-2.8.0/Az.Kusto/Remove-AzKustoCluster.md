---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 3556ff99dafe804ab78899f8b0eefc64db4ca82b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666108"
---
# <span data-ttu-id="86c20-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="86c20-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="86c20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86c20-102">SYNOPSIS</span></span>
<span data-ttu-id="86c20-103">Töröl egy meglévő Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="86c20-103">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="86c20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86c20-104">SYNTAX</span></span>

### <span data-ttu-id="86c20-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86c20-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c20-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="86c20-106">ByResourceId</span></span>
```
Remove-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c20-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="86c20-107">ByInputObject</span></span>
```
Remove-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c20-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="86c20-108">DESCRIPTION</span></span>
<span data-ttu-id="86c20-109">Töröl egy meglévő Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="86c20-109">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="86c20-110">Példák</span><span class="sxs-lookup"><span data-stu-id="86c20-110">EXAMPLES</span></span>

### <span data-ttu-id="86c20-111">Példa 1 – meglévő Kusto-fürt törlése név szerint</span><span class="sxs-lookup"><span data-stu-id="86c20-111">Example 1 - Delete an existing Kusto cluster by name</span></span>

```
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="86c20-112">A fenti parancs törli a "mykustocluster" nevű Kusto-fürtöt az "testrg" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="86c20-112">The above command deletes the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="86c20-113">2. példa – meglévő Kusto-fürt törlése csővezetékről</span><span class="sxs-lookup"><span data-stu-id="86c20-113">Example 2 - Delete an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Remove-AzKustoCluster
```

<span data-ttu-id="86c20-114">A fenti parancs az "mykustocluster" nevű Kusto-fürtöt az "testrg" erőforráscsoport nevében a `Get-AzKustoCluster` parancsmag használatával kapja, majd az eredményt a `Remove-AzKustoCluster` törléséhez.</span><span class="sxs-lookup"><span data-stu-id="86c20-114">The above command gets the Kusto cluster named "mykustocluster" in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Remove-AzKustoCluster` to delete it.</span></span>

## <span data-ttu-id="86c20-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86c20-115">PARAMETERS</span></span>

### <span data-ttu-id="86c20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c20-116">-DefaultProfile</span></span>
<span data-ttu-id="86c20-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86c20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86c20-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86c20-118">-InputObject</span></span>
<span data-ttu-id="86c20-119">Kusto.</span><span class="sxs-lookup"><span data-stu-id="86c20-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="86c20-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86c20-120">-Name</span></span>
<span data-ttu-id="86c20-121">Eltávolítandó szektorcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86c20-121">Name of cluster to be removed.</span></span>

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

### <span data-ttu-id="86c20-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86c20-122">-PassThru</span></span>
<span data-ttu-id="86c20-123">Annak megadása, hogy a megadott fürtöt sikeresen törölték-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="86c20-123">Return whether the specified cluster was successfully deleted or not.</span></span>

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

### <span data-ttu-id="86c20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c20-124">-ResourceGroupName</span></span>
<span data-ttu-id="86c20-125">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="86c20-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="86c20-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86c20-126">-ResourceId</span></span>
<span data-ttu-id="86c20-127">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="86c20-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="86c20-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86c20-128">-Confirm</span></span>
<span data-ttu-id="86c20-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86c20-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c20-130">-WhatIf</span></span>
<span data-ttu-id="86c20-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86c20-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c20-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86c20-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c20-133">CommonParameters</span></span>
<span data-ttu-id="86c20-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86c20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c20-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c20-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c20-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86c20-136">INPUTS</span></span>

### <span data-ttu-id="86c20-137">System. String</span><span class="sxs-lookup"><span data-stu-id="86c20-137">System.String</span></span>

### <span data-ttu-id="86c20-138">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="86c20-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="86c20-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86c20-139">OUTPUTS</span></span>

### <span data-ttu-id="86c20-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86c20-140">System.Boolean</span></span>

## <span data-ttu-id="86c20-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86c20-141">NOTES</span></span>

## <span data-ttu-id="86c20-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86c20-142">RELATED LINKS</span></span>
