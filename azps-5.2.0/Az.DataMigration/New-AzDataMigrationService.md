---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350405"
---
# <span data-ttu-id="64c16-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="64c16-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="64c16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c16-102">SYNOPSIS</span></span>
<span data-ttu-id="64c16-103">Létrehozza az Azure Database Migration Service új példányát.</span><span class="sxs-lookup"><span data-stu-id="64c16-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="64c16-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64c16-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64c16-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64c16-105">DESCRIPTION</span></span>
<span data-ttu-id="64c16-106">A New-AzDataMigrationService parancsmag létrehoz egy új példányt az Azure Adatbázis-áttelepítési szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="64c16-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="64c16-107">Ez a parancsmag a meglévő Azure Resource Group nevet veszi fel, a létrehozni szükséges Azure Adatbázis-áttelepítési szolgáltatás új példányának egyedi nevét, a példány kiépítésének régióját, a DMS Worker termékváltozat nevét, valamint annak az Azure Virtuális alhálózatnak a nevét, amelyen a szolgáltatás található.</span><span class="sxs-lookup"><span data-stu-id="64c16-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="64c16-108">Az előfizetés nevéhez nincs paraméter, mert a felhasználónak meg kell adnia az Azure bejelentkezési munkamenet alapértelmezett előfizetését, vagy végre kell hajtania a Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription másik előfizetést.</span><span class="sxs-lookup"><span data-stu-id="64c16-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="64c16-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64c16-109">EXAMPLES</span></span>

### <span data-ttu-id="64c16-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="64c16-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="64c16-111">A fenti példa bemutatja, hogy miként hozhat létre egy TestService nevű Azure Database Migration Service-példányt a közép-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="64c16-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="64c16-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64c16-112">PARAMETERS</span></span>

### <span data-ttu-id="64c16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c16-113">-DefaultProfile</span></span>
<span data-ttu-id="64c16-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64c16-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64c16-115">-Location</span><span class="sxs-lookup"><span data-stu-id="64c16-115">-Location</span></span>
<span data-ttu-id="64c16-116">A létrehozható Azure Database Migration Service-példány helye, amely megfelel egy Azure-régiónak.</span><span class="sxs-lookup"><span data-stu-id="64c16-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="64c16-117">-Name</span><span class="sxs-lookup"><span data-stu-id="64c16-117">-Name</span></span>
<span data-ttu-id="64c16-118">Adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="64c16-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="64c16-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c16-119">-ResourceGroupName</span></span>
<span data-ttu-id="64c16-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="64c16-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="64c16-121">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="64c16-121">-Sku</span></span>
<span data-ttu-id="64c16-122">Az Azure Database Migration Service példány termékváltozata.</span><span class="sxs-lookup"><span data-stu-id="64c16-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="64c16-123">A lehetséges értékek jelenleg Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="64c16-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="64c16-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="64c16-124">-VirtualSubnetId</span></span>
<span data-ttu-id="64c16-125">Az Azure Database Migration Service-példányhoz használt, megadott virtuális hálózat alatti alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="64c16-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="64c16-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64c16-126">-Confirm</span></span>
<span data-ttu-id="64c16-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64c16-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c16-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c16-128">-WhatIf</span></span>
<span data-ttu-id="64c16-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64c16-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64c16-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64c16-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c16-131">CommonParameters</span></span>
<span data-ttu-id="64c16-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c16-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c16-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c16-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64c16-134">INPUTS</span></span>

### <span data-ttu-id="64c16-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="64c16-135">None</span></span>

## <span data-ttu-id="64c16-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64c16-136">OUTPUTS</span></span>

### <span data-ttu-id="64c16-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="64c16-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="64c16-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64c16-138">NOTES</span></span>

## <span data-ttu-id="64c16-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64c16-139">RELATED LINKS</span></span>
