---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: ce2fbe2f598ca6d08033c397a988f140379fda96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666107"
---
# <span data-ttu-id="7b61d-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="7b61d-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="7b61d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b61d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b61d-103">Felfüggesztett Kusto-fürt folytatása</span><span class="sxs-lookup"><span data-stu-id="7b61d-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="7b61d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b61d-104">SYNTAX</span></span>

### <span data-ttu-id="7b61d-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b61d-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b61d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b61d-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b61d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7b61d-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b61d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b61d-108">DESCRIPTION</span></span>
<span data-ttu-id="7b61d-109">Felfüggesztett Kusto-fürt folytatása</span><span class="sxs-lookup"><span data-stu-id="7b61d-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="7b61d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7b61d-110">EXAMPLES</span></span>

### <span data-ttu-id="7b61d-111">Példa 1 – felfüggesztett Kusto-fürt folytatása név szerint</span><span class="sxs-lookup"><span data-stu-id="7b61d-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="7b61d-112">A fenti parancs a "mykustocluster" nevű felfüggesztett Kusto-fürtöt a "testrg" erőforráscsoport nevében találja.</span><span class="sxs-lookup"><span data-stu-id="7b61d-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="7b61d-113">Példa 2 – felfüggesztett Kusto-fürt folytatása csővezetékek használatával</span><span class="sxs-lookup"><span data-stu-id="7b61d-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="7b61d-114">A fenti parancs az "mykustocluster" nevű Kusto-fürtöt az "testrg" nevű erőforráscsoport nevében találja a parancsmag használatával, majd az eredmény visszahúzása a `Get-AzKustoCluster` `Resume-AzKustoCluster` folytatáshoz.</span><span class="sxs-lookup"><span data-stu-id="7b61d-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="7b61d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b61d-115">PARAMETERS</span></span>

### <span data-ttu-id="7b61d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b61d-116">-DefaultProfile</span></span>
<span data-ttu-id="7b61d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7b61d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b61d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b61d-118">-InputObject</span></span>
<span data-ttu-id="7b61d-119">Kusto.</span><span class="sxs-lookup"><span data-stu-id="7b61d-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="7b61d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7b61d-120">-Name</span></span>
<span data-ttu-id="7b61d-121">Az önéletrajz neve.</span><span class="sxs-lookup"><span data-stu-id="7b61d-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="7b61d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b61d-122">-PassThru</span></span>
<span data-ttu-id="7b61d-123">A megadott szektorcsoport sikeres folytatásának visszaadása.</span><span class="sxs-lookup"><span data-stu-id="7b61d-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="7b61d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b61d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b61d-125">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="7b61d-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b61d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b61d-126">-ResourceId</span></span>
<span data-ttu-id="7b61d-127">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="7b61d-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="7b61d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b61d-128">-Confirm</span></span>
<span data-ttu-id="7b61d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b61d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b61d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b61d-130">-WhatIf</span></span>
<span data-ttu-id="7b61d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b61d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b61d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b61d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b61d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b61d-133">CommonParameters</span></span>
<span data-ttu-id="7b61d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b61d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b61d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b61d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b61d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b61d-136">INPUTS</span></span>

### <span data-ttu-id="7b61d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7b61d-137">System.String</span></span>

### <span data-ttu-id="7b61d-138">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="7b61d-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="7b61d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b61d-139">OUTPUTS</span></span>

### <span data-ttu-id="7b61d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b61d-140">System.Boolean</span></span>

## <span data-ttu-id="7b61d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b61d-141">NOTES</span></span>

## <span data-ttu-id="7b61d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b61d-142">RELATED LINKS</span></span>
