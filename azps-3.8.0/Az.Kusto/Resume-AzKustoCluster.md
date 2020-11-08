---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: 94e5525b1d783eea794b7e98e76e809b9d7e0f3b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011123"
---
# <span data-ttu-id="601cc-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="601cc-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="601cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="601cc-102">SYNOPSIS</span></span>
<span data-ttu-id="601cc-103">Felfüggesztett Kusto-fürt folytatása</span><span class="sxs-lookup"><span data-stu-id="601cc-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="601cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="601cc-104">SYNTAX</span></span>

### <span data-ttu-id="601cc-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="601cc-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601cc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="601cc-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601cc-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="601cc-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="601cc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="601cc-108">DESCRIPTION</span></span>
<span data-ttu-id="601cc-109">Felfüggesztett Kusto-fürt folytatása</span><span class="sxs-lookup"><span data-stu-id="601cc-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="601cc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="601cc-110">EXAMPLES</span></span>

### <span data-ttu-id="601cc-111">Példa 1 – felfüggesztett Kusto-fürt folytatása név szerint</span><span class="sxs-lookup"><span data-stu-id="601cc-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="601cc-112">A fenti parancs a "mykustocluster" nevű felfüggesztett Kusto-fürtöt a "testrg" erőforráscsoport nevében találja.</span><span class="sxs-lookup"><span data-stu-id="601cc-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="601cc-113">Példa 2 – felfüggesztett Kusto-fürt folytatása csővezetékek használatával</span><span class="sxs-lookup"><span data-stu-id="601cc-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="601cc-114">A fenti parancs az "mykustocluster" nevű Kusto-fürtöt az "testrg" nevű erőforráscsoport nevében találja a parancsmag használatával, majd az eredmény visszahúzása a `Get-AzKustoCluster` `Resume-AzKustoCluster` folytatáshoz.</span><span class="sxs-lookup"><span data-stu-id="601cc-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="601cc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="601cc-115">PARAMETERS</span></span>

### <span data-ttu-id="601cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601cc-116">-DefaultProfile</span></span>
<span data-ttu-id="601cc-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="601cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="601cc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="601cc-118">-InputObject</span></span>
<span data-ttu-id="601cc-119">Kusto.</span><span class="sxs-lookup"><span data-stu-id="601cc-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="601cc-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="601cc-120">-Name</span></span>
<span data-ttu-id="601cc-121">Az önéletrajz neve.</span><span class="sxs-lookup"><span data-stu-id="601cc-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="601cc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="601cc-122">-PassThru</span></span>
<span data-ttu-id="601cc-123">A megadott szektorcsoport sikeres folytatásának visszaadása.</span><span class="sxs-lookup"><span data-stu-id="601cc-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="601cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="601cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="601cc-125">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="601cc-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="601cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="601cc-126">-ResourceId</span></span>
<span data-ttu-id="601cc-127">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="601cc-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="601cc-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="601cc-128">-Confirm</span></span>
<span data-ttu-id="601cc-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="601cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="601cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="601cc-130">-WhatIf</span></span>
<span data-ttu-id="601cc-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="601cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="601cc-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="601cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="601cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601cc-133">CommonParameters</span></span>
<span data-ttu-id="601cc-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="601cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601cc-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="601cc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601cc-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="601cc-136">INPUTS</span></span>

### <span data-ttu-id="601cc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="601cc-137">System.String</span></span>

### <span data-ttu-id="601cc-138">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="601cc-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="601cc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="601cc-139">OUTPUTS</span></span>

### <span data-ttu-id="601cc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="601cc-140">System.Boolean</span></span>

## <span data-ttu-id="601cc-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="601cc-141">NOTES</span></span>

## <span data-ttu-id="601cc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="601cc-142">RELATED LINKS</span></span>
