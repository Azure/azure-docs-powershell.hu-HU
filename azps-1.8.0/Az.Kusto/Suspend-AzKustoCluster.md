---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/suspend-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
ms.openlocfilehash: 6eceaffb371226c9dda0099a32a309272d6bdb3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835554"
---
# <span data-ttu-id="93b05-101">Suspend-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="93b05-101">Suspend-AzKustoCluster</span></span>

## <span data-ttu-id="93b05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93b05-102">SYNOPSIS</span></span>
<span data-ttu-id="93b05-103">Meglévő Kusto-fürt felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="93b05-103">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="93b05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93b05-104">SYNTAX</span></span>

### <span data-ttu-id="93b05-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93b05-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93b05-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="93b05-106">ByResourceId</span></span>
```
Suspend-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93b05-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="93b05-107">ByInputObject</span></span>
```
Suspend-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93b05-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="93b05-108">DESCRIPTION</span></span>
<span data-ttu-id="93b05-109">Meglévő Kusto-fürt felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="93b05-109">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="93b05-110">Példák</span><span class="sxs-lookup"><span data-stu-id="93b05-110">EXAMPLES</span></span>

### <span data-ttu-id="93b05-111">Példa 1 – meglévő Kusto-fürt felfüggesztése név alapján</span><span class="sxs-lookup"><span data-stu-id="93b05-111">Example 1 - Suspend an existing Kusto cluster by name</span></span>

```
PS C:\> Suspend-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="93b05-112">A fenti parancs felfüggeszti a "mykustocluster" nevű Kusto-fürtöt, amely az "testrg" erőforráscsoport nevű erőforráscsoport területén található.</span><span class="sxs-lookup"><span data-stu-id="93b05-112">The above command suspends the Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="93b05-113">2. példa – meglévő Kusto-fürtök felfüggesztése csővezetéken</span><span class="sxs-lookup"><span data-stu-id="93b05-113">Example 2 - Suspend an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Suspend-AzKustoCluster
```

<span data-ttu-id="93b05-114">A fenti parancs az "mykustocluster" nevű Kusto-fürtöt az "testrg" erőforráscsoport nevében találja a `Get-AzKustoCluster` parancsmag használatával, majd a csöveket az eredményt `Suspend-AzKustoCluster` felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="93b05-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Suspend-AzKustoCluster` to suspend it.</span></span>

## <span data-ttu-id="93b05-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93b05-115">PARAMETERS</span></span>

### <span data-ttu-id="93b05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b05-116">-DefaultProfile</span></span>
<span data-ttu-id="93b05-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93b05-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93b05-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93b05-118">-InputObject</span></span>
<span data-ttu-id="93b05-119">Kusto.</span><span class="sxs-lookup"><span data-stu-id="93b05-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="93b05-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93b05-120">-Name</span></span>
<span data-ttu-id="93b05-121">A felfüggeszteni kívánt szektorcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93b05-121">Name of cluster to be suspend.</span></span>

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

### <span data-ttu-id="93b05-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93b05-122">-PassThru</span></span>
<span data-ttu-id="93b05-123">Annak megadása, hogy a megadott fürtöt sikeresen felfüggesztették-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="93b05-123">Return whether the specified cluster was successfully suspended or not.</span></span>

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

### <span data-ttu-id="93b05-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b05-124">-ResourceGroupName</span></span>
<span data-ttu-id="93b05-125">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="93b05-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="93b05-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93b05-126">-ResourceId</span></span>
<span data-ttu-id="93b05-127">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="93b05-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="93b05-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93b05-128">-Confirm</span></span>
<span data-ttu-id="93b05-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93b05-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93b05-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93b05-130">-WhatIf</span></span>
<span data-ttu-id="93b05-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93b05-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93b05-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93b05-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93b05-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b05-133">CommonParameters</span></span>
<span data-ttu-id="93b05-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93b05-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b05-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b05-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b05-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93b05-136">INPUTS</span></span>

### <span data-ttu-id="93b05-137">System. String</span><span class="sxs-lookup"><span data-stu-id="93b05-137">System.String</span></span>

### <span data-ttu-id="93b05-138">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="93b05-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="93b05-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93b05-139">OUTPUTS</span></span>

### <span data-ttu-id="93b05-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93b05-140">System.Boolean</span></span>

## <span data-ttu-id="93b05-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93b05-141">NOTES</span></span>

## <span data-ttu-id="93b05-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93b05-142">RELATED LINKS</span></span>
