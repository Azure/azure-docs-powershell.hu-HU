---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: ddab39c3ad575cd46c427c7346fd635217c0dbca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497295"
---
# <span data-ttu-id="f265b-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="f265b-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="f265b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f265b-102">SYNOPSIS</span></span>
<span data-ttu-id="f265b-103">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="f265b-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f265b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f265b-104">SYNTAX</span></span>

### <span data-ttu-id="f265b-105">Automatikus</span><span class="sxs-lookup"><span data-stu-id="f265b-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f265b-106">Kézi</span><span class="sxs-lookup"><span data-stu-id="f265b-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f265b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f265b-107">DESCRIPTION</span></span>
<span data-ttu-id="f265b-108">A **set-AzureRmServiceFabricUpgradeType** beállíthatja, hogy a frissítési típust az automatikus vagy a kézi beállítással állítsa be az adott szolgáltatás szövet-verziószáma.</span><span class="sxs-lookup"><span data-stu-id="f265b-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="f265b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f265b-109">EXAMPLES</span></span>

### <span data-ttu-id="f265b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f265b-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="f265b-111">Ez a parancs automatikusan beállítja a cluster upgrade üzemmódot.</span><span class="sxs-lookup"><span data-stu-id="f265b-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="f265b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f265b-112">PARAMETERS</span></span>

### <span data-ttu-id="f265b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f265b-113">-DefaultProfile</span></span>
<span data-ttu-id="f265b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f265b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f265b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f265b-115">-Name</span></span>
<span data-ttu-id="f265b-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="f265b-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f265b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f265b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f265b-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f265b-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f265b-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="f265b-119">-UpgradeMode</span></span>
<span data-ttu-id="f265b-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="f265b-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="f265b-121">-Verzió</span><span class="sxs-lookup"><span data-stu-id="f265b-121">-Version</span></span>
<span data-ttu-id="f265b-122">Szektorcsoport-kód verziója.</span><span class="sxs-lookup"><span data-stu-id="f265b-122">Cluster code version.</span></span>

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

### <span data-ttu-id="f265b-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f265b-123">-Confirm</span></span>
<span data-ttu-id="f265b-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f265b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f265b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f265b-125">-WhatIf</span></span>
<span data-ttu-id="f265b-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f265b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f265b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f265b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f265b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f265b-128">CommonParameters</span></span>
<span data-ttu-id="f265b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f265b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f265b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f265b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f265b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f265b-131">INPUTS</span></span>

### <span data-ttu-id="f265b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f265b-132">System.String</span></span>
<span data-ttu-id="f265b-133">Paraméterek: verzió (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f265b-133">Parameters: Version (ByValue)</span></span>

### <span data-ttu-id="f265b-134">Microsoft. Azure. Command. ServiceFabric. models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="f265b-134">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="f265b-135">Paraméterek: UpgradeMode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f265b-135">Parameters: UpgradeMode (ByValue)</span></span>

## <span data-ttu-id="f265b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f265b-136">OUTPUTS</span></span>

### <span data-ttu-id="f265b-137">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="f265b-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f265b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f265b-138">NOTES</span></span>

## <span data-ttu-id="f265b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f265b-139">RELATED LINKS</span></span>
