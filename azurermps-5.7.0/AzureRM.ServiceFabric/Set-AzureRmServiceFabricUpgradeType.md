---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 8a675355806a8b4579abcea965a5e0e0b8128207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502415"
---
# <span data-ttu-id="cc731-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="cc731-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="cc731-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc731-102">SYNOPSIS</span></span>
<span data-ttu-id="cc731-103">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="cc731-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc731-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc731-104">SYNTAX</span></span>

### <span data-ttu-id="cc731-105">Automatikus</span><span class="sxs-lookup"><span data-stu-id="cc731-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc731-106">Kézi</span><span class="sxs-lookup"><span data-stu-id="cc731-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc731-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc731-107">DESCRIPTION</span></span>
<span data-ttu-id="cc731-108">A **set-AzureRmServiceFabricUpgradeType** beállíthatja, hogy a frissítési típust az automatikus vagy a kézi beállítással állítsa be az adott szolgáltatás szövet-verziószáma.</span><span class="sxs-lookup"><span data-stu-id="cc731-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="cc731-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cc731-109">EXAMPLES</span></span>

### <span data-ttu-id="cc731-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cc731-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="cc731-111">Ez a parancs automatikusan beállítja a cluster upgrade üzemmódot.</span><span class="sxs-lookup"><span data-stu-id="cc731-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="cc731-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc731-112">PARAMETERS</span></span>

### <span data-ttu-id="cc731-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc731-113">-DefaultProfile</span></span>
<span data-ttu-id="cc731-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc731-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc731-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cc731-115">-Name</span></span>
<span data-ttu-id="cc731-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="cc731-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc731-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc731-117">-ResourceGroupName</span></span>
<span data-ttu-id="cc731-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc731-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc731-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cc731-119">-UpgradeMode</span></span>
<span data-ttu-id="cc731-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cc731-120">ClusterUpgradeMode</span></span>

```yaml
Type: ClusterUpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc731-121">-Verzió</span><span class="sxs-lookup"><span data-stu-id="cc731-121">-Version</span></span>
<span data-ttu-id="cc731-122">Szektorcsoport-kód verziója.</span><span class="sxs-lookup"><span data-stu-id="cc731-122">Cluster code version.</span></span>

```yaml
Type: String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc731-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc731-123">-Confirm</span></span>
<span data-ttu-id="cc731-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc731-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc731-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc731-125">-WhatIf</span></span>
<span data-ttu-id="cc731-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc731-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc731-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc731-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc731-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc731-128">CommonParameters</span></span>
<span data-ttu-id="cc731-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc731-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc731-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc731-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc731-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc731-131">INPUTS</span></span>

### <span data-ttu-id="cc731-132">Microsoft. Azure. Command. ServiceFabric. models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="cc731-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="cc731-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cc731-133">System.String</span></span>

## <span data-ttu-id="cc731-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc731-134">OUTPUTS</span></span>

### <span data-ttu-id="cc731-135">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="cc731-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="cc731-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc731-136">NOTES</span></span>

## <span data-ttu-id="cc731-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc731-137">RELATED LINKS</span></span>

