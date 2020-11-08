---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: c29a1bf4b5b60034a8f38ff8388f36997dbddfc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014293"
---
# <span data-ttu-id="bda4e-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="bda4e-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="bda4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bda4e-102">SYNOPSIS</span></span>
<span data-ttu-id="bda4e-103">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="bda4e-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="bda4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bda4e-104">SYNTAX</span></span>

### <span data-ttu-id="bda4e-105">Automatikus</span><span class="sxs-lookup"><span data-stu-id="bda4e-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bda4e-106">Kézi</span><span class="sxs-lookup"><span data-stu-id="bda4e-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bda4e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bda4e-107">DESCRIPTION</span></span>
<span data-ttu-id="bda4e-108">A **set-AzServiceFabricUpgradeType** beállíthatja, hogy a frissítési típust az automatikus vagy a kézi beállítással állítsa be az adott szolgáltatás szövet-verziószáma.</span><span class="sxs-lookup"><span data-stu-id="bda4e-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="bda4e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bda4e-109">EXAMPLES</span></span>

### <span data-ttu-id="bda4e-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bda4e-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="bda4e-111">Ez a parancs automatikusan beállítja a cluster upgrade üzemmódot.</span><span class="sxs-lookup"><span data-stu-id="bda4e-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="bda4e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bda4e-112">PARAMETERS</span></span>

### <span data-ttu-id="bda4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda4e-113">-DefaultProfile</span></span>
<span data-ttu-id="bda4e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bda4e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bda4e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bda4e-115">-Name</span></span>
<span data-ttu-id="bda4e-116">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="bda4e-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda4e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda4e-117">-ResourceGroupName</span></span>
<span data-ttu-id="bda4e-118">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="bda4e-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bda4e-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="bda4e-119">-UpgradeMode</span></span>
<span data-ttu-id="bda4e-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="bda4e-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bda4e-121">-Verzió</span><span class="sxs-lookup"><span data-stu-id="bda4e-121">-Version</span></span>
<span data-ttu-id="bda4e-122">Szektorcsoport-kód verziója</span><span class="sxs-lookup"><span data-stu-id="bda4e-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bda4e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bda4e-123">-Confirm</span></span>
<span data-ttu-id="bda4e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bda4e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bda4e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bda4e-125">-WhatIf</span></span>
<span data-ttu-id="bda4e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bda4e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bda4e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bda4e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bda4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda4e-128">CommonParameters</span></span>
<span data-ttu-id="bda4e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bda4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda4e-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bda4e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda4e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bda4e-131">INPUTS</span></span>

### <span data-ttu-id="bda4e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bda4e-132">System.String</span></span>

### <span data-ttu-id="bda4e-133">Microsoft. Azure. Command. ServiceFabric. models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="bda4e-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="bda4e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bda4e-134">OUTPUTS</span></span>

### <span data-ttu-id="bda4e-135">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="bda4e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bda4e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bda4e-136">NOTES</span></span>

## <span data-ttu-id="bda4e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bda4e-137">RELATED LINKS</span></span>
