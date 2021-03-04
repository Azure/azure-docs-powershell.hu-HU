---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: f8724fe13cb44ac3e2640f747026c121303be252
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932233"
---
# <span data-ttu-id="7ded3-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7ded3-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="7ded3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ded3-102">SYNOPSIS</span></span>
<span data-ttu-id="7ded3-103">Hozzon létre új service fabric application type under the specified resource group and cluster.</span><span class="sxs-lookup"><span data-stu-id="7ded3-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="7ded3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ded3-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ded3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ded3-105">DESCRIPTION</span></span>
<span data-ttu-id="7ded3-106">A parancsmag létrehoz egy új service fabric alkalmazástípust a megadott erőforráscsoport és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="7ded3-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="7ded3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ded3-107">EXAMPLES</span></span>

### <span data-ttu-id="7ded3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7ded3-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="7ded3-109">Ebben a példában egy új alkalmazástípust hozunk létre "testAppType" néven az erőforráscsoport és a megadott fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="7ded3-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="7ded3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ded3-110">PARAMETERS</span></span>

### <span data-ttu-id="7ded3-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7ded3-111">-ClusterName</span></span>
<span data-ttu-id="7ded3-112">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="7ded3-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ded3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ded3-113">-DefaultProfile</span></span>
<span data-ttu-id="7ded3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ded3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ded3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7ded3-115">-Name</span></span>
<span data-ttu-id="7ded3-116">Az alkalmazástípus nevének megadása</span><span class="sxs-lookup"><span data-stu-id="7ded3-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ded3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ded3-117">-ResourceGroupName</span></span>
<span data-ttu-id="7ded3-118">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="7ded3-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ded3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ded3-119">-Confirm</span></span>
<span data-ttu-id="7ded3-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ded3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ded3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ded3-121">-WhatIf</span></span>
<span data-ttu-id="7ded3-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ded3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ded3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ded3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ded3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ded3-124">CommonParameters</span></span>
<span data-ttu-id="7ded3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ded3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ded3-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ded3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ded3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ded3-127">INPUTS</span></span>

### <span data-ttu-id="7ded3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7ded3-128">System.String</span></span>

## <span data-ttu-id="7ded3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ded3-129">OUTPUTS</span></span>

### <span data-ttu-id="7ded3-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="7ded3-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="7ded3-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ded3-131">NOTES</span></span>

## <span data-ttu-id="7ded3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ded3-132">RELATED LINKS</span></span>
