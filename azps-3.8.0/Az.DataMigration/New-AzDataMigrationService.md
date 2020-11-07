---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845321"
---
# <span data-ttu-id="6aec7-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="6aec7-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="6aec7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6aec7-102">SYNOPSIS</span></span>
<span data-ttu-id="6aec7-103">Az Azure-adatbázis áttelepítési szolgáltatásának új példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6aec7-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="6aec7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6aec7-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aec7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6aec7-105">DESCRIPTION</span></span>
<span data-ttu-id="6aec7-106">Az New-AzDataMigrationService parancsmag az Azure adatbázis-áttelepítési szolgáltatás új példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6aec7-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="6aec7-107">Ez a parancsmag a meglévő Azure Resource Group nevet veszi fel, az Azure-adatbázis áttelepítési szolgáltatásának új példányának egyedi nevét, a példány kiépítési területét, a DMS-munkatárs SKU nevét, valamint annak az Azure virtuális alhálózatnak a nevét, amelyen a szolgáltatás található.</span><span class="sxs-lookup"><span data-stu-id="6aec7-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="6aec7-108">Nincs paraméter az előfizetés nevéhez, mert várhatóan a felhasználó megadhatja az Azure bejelentkezési munkamenet alapértelmezett előfizetését, vagy végrehajtja a Get-AzSubscription-SubscriptionName "MySubscription" | Select-AzSubscription másik előfizetést szeretne kiválasztani.</span><span class="sxs-lookup"><span data-stu-id="6aec7-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="6aec7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6aec7-109">EXAMPLES</span></span>

### <span data-ttu-id="6aec7-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6aec7-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="6aec7-111">A fenti példa azt szemlélteti, hogy miként hozhat létre új példányt az Azure Database áttelepítési szolgáltatás TestService nevű, Közép-amerikai régiójában.</span><span class="sxs-lookup"><span data-stu-id="6aec7-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="6aec7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6aec7-112">PARAMETERS</span></span>

### <span data-ttu-id="6aec7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aec7-113">-DefaultProfile</span></span>
<span data-ttu-id="6aec7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6aec7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aec7-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="6aec7-115">-Location</span></span>
<span data-ttu-id="6aec7-116">Annak a helynek a helye, amely az Azure-adatbázis áttelepítési példányát hozza létre, amely egy Azure-régiónak felel meg.</span><span class="sxs-lookup"><span data-stu-id="6aec7-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec7-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6aec7-117">-Name</span></span>
<span data-ttu-id="6aec7-118">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="6aec7-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aec7-119">-ResourceGroupName</span></span>
<span data-ttu-id="6aec7-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6aec7-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec7-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="6aec7-121">-Sku</span></span>
<span data-ttu-id="6aec7-122">Az Azure adatbázis-áttelepítési szolgáltatás példányának SKU-je.</span><span class="sxs-lookup"><span data-stu-id="6aec7-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="6aec7-123">A lehetséges értékek jelenleg az Basic_1vCore, a Basic_2vCores, a GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="6aec7-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec7-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="6aec7-124">-VirtualSubnetId</span></span>
<span data-ttu-id="6aec7-125">Annak az alhálózatnak a neve, amely az Azure adatbázis-áttelepítési szolgáltatás példányához használható megadott virtuális hálózatban van.</span><span class="sxs-lookup"><span data-stu-id="6aec7-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aec7-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6aec7-126">-Confirm</span></span>
<span data-ttu-id="6aec7-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6aec7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aec7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aec7-128">-WhatIf</span></span>
<span data-ttu-id="6aec7-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6aec7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6aec7-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6aec7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aec7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aec7-131">CommonParameters</span></span>
<span data-ttu-id="6aec7-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6aec7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aec7-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aec7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aec7-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6aec7-134">INPUTS</span></span>

### <span data-ttu-id="6aec7-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="6aec7-135">None</span></span>

## <span data-ttu-id="6aec7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6aec7-136">OUTPUTS</span></span>

### <span data-ttu-id="6aec7-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="6aec7-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="6aec7-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6aec7-138">NOTES</span></span>

## <span data-ttu-id="6aec7-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6aec7-139">RELATED LINKS</span></span>
