---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 2e878c562c8f60ecebc9b6a43b3980e06fd0e355
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011722"
---
# <span data-ttu-id="69261-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="69261-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="69261-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69261-102">SYNOPSIS</span></span>
<span data-ttu-id="69261-103">Új szolgáltatásból álló anyag típusú alkalmazás létrehozása a megadott erőforráscsoport és fürt csoportban</span><span class="sxs-lookup"><span data-stu-id="69261-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="69261-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69261-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69261-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69261-105">DESCRIPTION</span></span>
<span data-ttu-id="69261-106">A parancsmag a megadott erőforráscsoport és fürt területéhez létrehoz egy új szolgáltatás szövet-alkalmazási típust.</span><span class="sxs-lookup"><span data-stu-id="69261-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="69261-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69261-107">EXAMPLES</span></span>

### <span data-ttu-id="69261-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="69261-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="69261-109">Ebben a példában az új "testAppType" típusú alkalmazás jön létre az erőforráscsoport és a fürt mezőben.</span><span class="sxs-lookup"><span data-stu-id="69261-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="69261-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69261-110">PARAMETERS</span></span>

### <span data-ttu-id="69261-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="69261-111">-ClusterName</span></span>
<span data-ttu-id="69261-112">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="69261-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="69261-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69261-113">-DefaultProfile</span></span>
<span data-ttu-id="69261-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69261-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69261-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69261-115">-Name</span></span>
<span data-ttu-id="69261-116">Adja meg az alkalmazás típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="69261-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="69261-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69261-117">-ResourceGroupName</span></span>
<span data-ttu-id="69261-118">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="69261-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="69261-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69261-119">-Confirm</span></span>
<span data-ttu-id="69261-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69261-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69261-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69261-121">-WhatIf</span></span>
<span data-ttu-id="69261-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69261-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69261-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69261-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69261-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69261-124">CommonParameters</span></span>
<span data-ttu-id="69261-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69261-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69261-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69261-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69261-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69261-127">INPUTS</span></span>

### <span data-ttu-id="69261-128">System. String</span><span class="sxs-lookup"><span data-stu-id="69261-128">System.String</span></span>

## <span data-ttu-id="69261-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69261-129">OUTPUTS</span></span>

### <span data-ttu-id="69261-130">Microsoft. Azure. Command. ServiceFabric. models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="69261-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="69261-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69261-131">NOTES</span></span>

## <span data-ttu-id="69261-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69261-132">RELATED LINKS</span></span>
