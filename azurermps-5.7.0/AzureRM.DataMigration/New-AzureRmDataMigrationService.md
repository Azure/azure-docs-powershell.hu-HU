---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680167"
---
# <span data-ttu-id="db54b-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="db54b-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="db54b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db54b-102">SYNOPSIS</span></span>
<span data-ttu-id="db54b-103">Az Azure-adatbázis áttelepítési szolgáltatásának új példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="db54b-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db54b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db54b-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="db54b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db54b-105">DESCRIPTION</span></span>
<span data-ttu-id="db54b-106">Az New-AzureRmDataMigrationService parancsmag az Azure adatbázis-áttelepítési szolgáltatás új példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="db54b-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="db54b-107">Ez a parancsmag a meglévő Azure Resource Group nevet veszi fel, az Azure-adatbázis áttelepítési szolgáltatásának új példányának egyedi nevét, a példány kiépítési területét, a DMS-munkatárs SKU nevét, valamint annak az Azure virtuális alhálózatnak a nevét, amelyen a szolgáltatás található.</span><span class="sxs-lookup"><span data-stu-id="db54b-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="db54b-108">Nincs paraméter az előfizetés nevéhez, mert várhatóan a felhasználó megadhatja az Azure bejelentkezési munkamenet alapértelmezett előfizetését, vagy végrehajtja a Get-AzureRmSubscription – SubscriptionName "MySubscription" | Select-AzureRmSubscription másik előfizetést szeretne kiválasztani.</span><span class="sxs-lookup"><span data-stu-id="db54b-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription –SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="db54b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="db54b-109">EXAMPLES</span></span>

### <span data-ttu-id="db54b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db54b-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="db54b-111">A fenti példa azt szemlélteti, hogy miként hozhat létre új példányt az Azure Database áttelepítési szolgáltatás TestService nevű, Közép-amerikai régiójában.</span><span class="sxs-lookup"><span data-stu-id="db54b-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>


## <span data-ttu-id="db54b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db54b-112">PARAMETERS</span></span>

### <span data-ttu-id="db54b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db54b-113">-DefaultProfile</span></span>
<span data-ttu-id="db54b-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db54b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db54b-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="db54b-115">-Location</span></span>
<span data-ttu-id="db54b-116">Annak a helynek a helye, amely az Azure-adatbázis áttelepítési példányát hozza létre, amely egy Azure-régiónak felel meg.</span><span class="sxs-lookup"><span data-stu-id="db54b-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db54b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db54b-117">-ResourceGroupName</span></span>
<span data-ttu-id="db54b-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="db54b-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db54b-119">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="db54b-119">-ServiceName</span></span>
<span data-ttu-id="db54b-120">Az Azure adatbázis-áttelepítési szolgáltatás példányának neve.</span><span class="sxs-lookup"><span data-stu-id="db54b-120">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db54b-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="db54b-121">-Sku</span></span>
<span data-ttu-id="db54b-122">Az Azure adatbázis-áttelepítési szolgáltatás példányának SKU-je.</span><span class="sxs-lookup"><span data-stu-id="db54b-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="db54b-123">A lehetséges értékek jelenleg az Basic_1vCore, a Basic_2vCores, a GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="db54b-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db54b-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="db54b-124">-VirtualSubnetId</span></span>
<span data-ttu-id="db54b-125">Annak az alhálózatnak a neve, amely az Azure adatbázis-áttelepítési szolgáltatás példányához használható megadott virtuális hálózatban van.</span><span class="sxs-lookup"><span data-stu-id="db54b-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="db54b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db54b-126">OUTPUTS</span></span>

### <span data-ttu-id="db54b-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="db54b-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>


## <span data-ttu-id="db54b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db54b-128">NOTES</span></span>

## <span data-ttu-id="db54b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db54b-129">RELATED LINKS</span></span>

