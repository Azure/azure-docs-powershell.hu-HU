---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195163"
---
# <span data-ttu-id="228a1-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="228a1-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="228a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="228a1-102">SYNOPSIS</span></span>
<span data-ttu-id="228a1-103">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="228a1-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="228a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="228a1-104">SYNTAX</span></span>

### <span data-ttu-id="228a1-105">Automatikus</span><span class="sxs-lookup"><span data-stu-id="228a1-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="228a1-106">Kézi</span><span class="sxs-lookup"><span data-stu-id="228a1-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="228a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="228a1-107">DESCRIPTION</span></span>
<span data-ttu-id="228a1-108">A **set-AzServiceFabricUpgradeType** beállíthatja, hogy a frissítési típust az automatikus vagy a kézi beállítással állítsa be az adott szolgáltatás szövet-verziószáma.</span><span class="sxs-lookup"><span data-stu-id="228a1-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="228a1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="228a1-109">EXAMPLES</span></span>

### <span data-ttu-id="228a1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="228a1-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="228a1-111">Ez a parancs automatikusan beállítja a cluster upgrade üzemmódot.</span><span class="sxs-lookup"><span data-stu-id="228a1-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="228a1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="228a1-112">PARAMETERS</span></span>

### <span data-ttu-id="228a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="228a1-113">-DefaultProfile</span></span>
<span data-ttu-id="228a1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="228a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="228a1-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="228a1-115">-Name</span></span>
<span data-ttu-id="228a1-116">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="228a1-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="228a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="228a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="228a1-118">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="228a1-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="228a1-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="228a1-119">-UpgradeMode</span></span>
<span data-ttu-id="228a1-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="228a1-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="228a1-121">-Verzió</span><span class="sxs-lookup"><span data-stu-id="228a1-121">-Version</span></span>
<span data-ttu-id="228a1-122">Szektorcsoport-kód verziója</span><span class="sxs-lookup"><span data-stu-id="228a1-122">Cluster code version</span></span>

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

### <span data-ttu-id="228a1-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="228a1-123">-Confirm</span></span>
<span data-ttu-id="228a1-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="228a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="228a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="228a1-125">-WhatIf</span></span>
<span data-ttu-id="228a1-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="228a1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="228a1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="228a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="228a1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228a1-128">CommonParameters</span></span>
<span data-ttu-id="228a1-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="228a1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228a1-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="228a1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228a1-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="228a1-131">INPUTS</span></span>

### <span data-ttu-id="228a1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="228a1-132">System.String</span></span>

### <span data-ttu-id="228a1-133">Microsoft. Azure. Command. ServiceFabric. models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="228a1-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="228a1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="228a1-134">OUTPUTS</span></span>

### <span data-ttu-id="228a1-135">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="228a1-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="228a1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="228a1-136">NOTES</span></span>

## <span data-ttu-id="228a1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="228a1-137">RELATED LINKS</span></span>
