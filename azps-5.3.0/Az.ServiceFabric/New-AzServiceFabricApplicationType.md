---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479557"
---
# <span data-ttu-id="c3ea7-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c3ea7-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="c3ea7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ea7-103">Hozzon létre új service fabric application type under the specified resource group and cluster.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="c3ea7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3ea7-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3ea7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ea7-106">A parancsmag létrehoz egy új service fabric alkalmazástípust a megadott erőforráscsoport és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="c3ea7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="c3ea7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3ea7-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="c3ea7-109">Ebben a példában egy új alkalmazástípust hozunk létre "testAppType" néven az erőforráscsoport és a megadott fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="c3ea7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3ea7-110">PARAMETERS</span></span>

### <span data-ttu-id="c3ea7-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c3ea7-111">-ClusterName</span></span>
<span data-ttu-id="c3ea7-112">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c3ea7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ea7-113">-DefaultProfile</span></span>
<span data-ttu-id="c3ea7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3ea7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c3ea7-115">-Name</span></span>
<span data-ttu-id="c3ea7-116">Az alkalmazástípus nevének megadása</span><span class="sxs-lookup"><span data-stu-id="c3ea7-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="c3ea7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ea7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3ea7-118">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c3ea7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3ea7-119">-Confirm</span></span>
<span data-ttu-id="c3ea7-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3ea7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ea7-121">-WhatIf</span></span>
<span data-ttu-id="c3ea7-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3ea7-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3ea7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ea7-124">CommonParameters</span></span>
<span data-ttu-id="c3ea7-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3ea7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ea7-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3ea7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ea7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3ea7-127">INPUTS</span></span>

### <span data-ttu-id="c3ea7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c3ea7-128">System.String</span></span>

## <span data-ttu-id="c3ea7-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3ea7-129">OUTPUTS</span></span>

### <span data-ttu-id="c3ea7-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="c3ea7-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="c3ea7-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3ea7-131">NOTES</span></span>

## <span data-ttu-id="c3ea7-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3ea7-132">RELATED LINKS</span></span>
