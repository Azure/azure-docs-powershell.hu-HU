---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499867"
---
# <span data-ttu-id="4d863-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="4d863-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="4d863-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d863-102">SYNOPSIS</span></span>
<span data-ttu-id="4d863-103">Eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="4d863-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d863-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d863-104">SYNTAX</span></span>

### <span data-ttu-id="4d863-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d863-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4d863-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d863-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4d863-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d863-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4d863-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d863-108">DESCRIPTION</span></span>
<span data-ttu-id="4d863-109">A Remove-AzureRmDataMigrationService parancsmag eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának példányát az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="4d863-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="4d863-110">A DeleteRunningTask paraméter ellátása eltávolítja az összes, az Azure adatbázis áttelepítési szolgáltatási feladatát, amely az eltávolítandó szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="4d863-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="4d863-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4d863-111">EXAMPLES</span></span>

### <span data-ttu-id="4d863-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4d863-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="4d863-113">A fenti példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás TestService nevű példányát, amely egy MyResourceGroup nevű Azure Resource csoportban található.</span><span class="sxs-lookup"><span data-stu-id="4d863-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="4d863-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d863-114">PARAMETERS</span></span>

### <span data-ttu-id="4d863-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d863-115">-Confirm</span></span>
<span data-ttu-id="4d863-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d863-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d863-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d863-117">-DefaultProfile</span></span>
<span data-ttu-id="4d863-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d863-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d863-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="4d863-119">-DeleteRunningTask</span></span>
<span data-ttu-id="4d863-120">Bármely futó tevékenység törlése</span><span class="sxs-lookup"><span data-stu-id="4d863-120">Delete any running task</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d863-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4d863-121">-Force</span></span>
<span data-ttu-id="4d863-122">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="4d863-122">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d863-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d863-123">-InputObject</span></span>
<span data-ttu-id="4d863-124">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="4d863-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d863-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d863-125">-Name</span></span>
<span data-ttu-id="4d863-126">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="4d863-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d863-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d863-127">-PassThru</span></span>
<span data-ttu-id="4d863-128">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="4d863-128">Returns an true/false.</span></span>
<span data-ttu-id="4d863-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4d863-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d863-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d863-130">-ResourceGroupName</span></span>
<span data-ttu-id="4d863-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d863-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d863-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d863-132">-ResourceId</span></span>
<span data-ttu-id="4d863-133">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4d863-133">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d863-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d863-134">-WhatIf</span></span>
<span data-ttu-id="4d863-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d863-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d863-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d863-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="4d863-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d863-137">INPUTS</span></span>

### <span data-ttu-id="4d863-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="4d863-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="4d863-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4d863-139">System.String</span></span>


## <span data-ttu-id="4d863-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d863-140">OUTPUTS</span></span>

### <span data-ttu-id="4d863-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d863-141">System.Boolean</span></span>


## <span data-ttu-id="4d863-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d863-142">NOTES</span></span>

## <span data-ttu-id="4d863-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d863-143">RELATED LINKS</span></span>


