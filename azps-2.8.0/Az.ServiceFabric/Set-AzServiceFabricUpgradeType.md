---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 9eba21106e5e2e7c22045d9aecdb86926e7e8ed7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837985"
---
# <span data-ttu-id="8f6c4-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="8f6c4-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="8f6c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6c4-103">Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="8f6c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f6c4-104">SYNTAX</span></span>

### <span data-ttu-id="8f6c4-105">Automatikus</span><span class="sxs-lookup"><span data-stu-id="8f6c4-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6c4-106">Kézi</span><span class="sxs-lookup"><span data-stu-id="8f6c4-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6c4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f6c4-107">DESCRIPTION</span></span>
<span data-ttu-id="8f6c4-108">A **set-AzServiceFabricUpgradeType** beállíthatja, hogy a frissítési típust az automatikus vagy a kézi beállítással állítsa be az adott szolgáltatás szövet-verziószáma.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="8f6c4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8f6c4-109">EXAMPLES</span></span>

### <span data-ttu-id="8f6c4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8f6c4-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="8f6c4-111">Ez a parancs automatikusan beállítja a cluster upgrade üzemmódot.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="8f6c4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f6c4-112">PARAMETERS</span></span>

### <span data-ttu-id="8f6c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6c4-113">-DefaultProfile</span></span>
<span data-ttu-id="8f6c4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6c4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8f6c4-115">-Name</span></span>
<span data-ttu-id="8f6c4-116">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="8f6c4-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="8f6c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f6c4-118">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8f6c4-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8f6c4-119">-UpgradeMode</span></span>
<span data-ttu-id="8f6c4-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8f6c4-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="8f6c4-121">-Verzió</span><span class="sxs-lookup"><span data-stu-id="8f6c4-121">-Version</span></span>
<span data-ttu-id="8f6c4-122">Szektorcsoport-kód verziója</span><span class="sxs-lookup"><span data-stu-id="8f6c4-122">Cluster code version</span></span>

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

### <span data-ttu-id="8f6c4-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f6c4-123">-Confirm</span></span>
<span data-ttu-id="8f6c4-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6c4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6c4-125">-WhatIf</span></span>
<span data-ttu-id="8f6c4-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6c4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6c4-128">CommonParameters</span></span>
<span data-ttu-id="8f6c4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f6c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6c4-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f6c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6c4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f6c4-131">INPUTS</span></span>

### <span data-ttu-id="8f6c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f6c4-132">System.String</span></span>

### <span data-ttu-id="8f6c4-133">Microsoft. Azure. Command. ServiceFabric. models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="8f6c4-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="8f6c4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f6c4-134">OUTPUTS</span></span>

### <span data-ttu-id="8f6c4-135">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="8f6c4-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8f6c4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f6c4-136">NOTES</span></span>

## <span data-ttu-id="8f6c4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f6c4-137">RELATED LINKS</span></span>
