---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 7884e45c2b4f635c9236f213a93eb69524b37fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672405"
---
# <span data-ttu-id="cb404-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="cb404-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="cb404-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb404-102">SYNOPSIS</span></span>
<span data-ttu-id="cb404-103">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="cb404-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb404-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb404-104">SYNTAX</span></span>

### <span data-ttu-id="cb404-105">Automatikus</span><span class="sxs-lookup"><span data-stu-id="cb404-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb404-106">Kézi</span><span class="sxs-lookup"><span data-stu-id="cb404-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb404-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb404-107">DESCRIPTION</span></span>
<span data-ttu-id="cb404-108">A **set-AzureRmServiceFabricUpgradeType** beállíthatja, hogy a frissítési típust az automatikus vagy a kézi beállítással állítsa be az adott szolgáltatás szövet-verziószáma.</span><span class="sxs-lookup"><span data-stu-id="cb404-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="cb404-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cb404-109">EXAMPLES</span></span>

### <span data-ttu-id="cb404-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cb404-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="cb404-111">Ez a parancs automatikusan beállítja a cluster upgrade üzemmódot.</span><span class="sxs-lookup"><span data-stu-id="cb404-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="cb404-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb404-112">PARAMETERS</span></span>

### <span data-ttu-id="cb404-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb404-113">-Name</span></span>
<span data-ttu-id="cb404-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="cb404-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cb404-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb404-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb404-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb404-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cb404-117">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cb404-117">-UpgradeMode</span></span>
<span data-ttu-id="cb404-118">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cb404-118">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="cb404-119">-Verzió</span><span class="sxs-lookup"><span data-stu-id="cb404-119">-Version</span></span>
<span data-ttu-id="cb404-120">Szektorcsoport-kód verziója.</span><span class="sxs-lookup"><span data-stu-id="cb404-120">Cluster code version.</span></span>

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

### <span data-ttu-id="cb404-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb404-121">-Confirm</span></span>
<span data-ttu-id="cb404-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb404-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb404-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb404-123">-WhatIf</span></span>
<span data-ttu-id="cb404-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb404-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb404-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb404-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb404-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb404-126">-DefaultProfile</span></span>
<span data-ttu-id="cb404-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb404-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb404-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb404-128">CommonParameters</span></span>
<span data-ttu-id="cb404-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb404-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb404-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb404-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb404-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb404-131">INPUTS</span></span>

### <span data-ttu-id="cb404-132">Microsoft. Azure. Command. ServiceFabric. models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cb404-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="cb404-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cb404-133">System.String</span></span>

## <span data-ttu-id="cb404-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb404-134">OUTPUTS</span></span>

### <span data-ttu-id="cb404-135">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="cb404-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="cb404-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb404-136">NOTES</span></span>

## <span data-ttu-id="cb404-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb404-137">RELATED LINKS</span></span>

