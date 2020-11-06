---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503767"
---
# <span data-ttu-id="ef7d3-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="ef7d3-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="ef7d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7d3-103">Az Azure adatbázis-áttelepítési szolgáltatás projekt eltávolítása az Azure-ról</span><span class="sxs-lookup"><span data-stu-id="ef7d3-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef7d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef7d3-104">SYNTAX</span></span>

### <span data-ttu-id="ef7d3-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef7d3-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ef7d3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef7d3-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ef7d3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef7d3-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ef7d3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef7d3-108">DESCRIPTION</span></span>
<span data-ttu-id="ef7d3-109">A Remove-AzureRmDataMigrationProject parancsmag az Azure adatbázis-áttelepítési szolgáltatás projektjét távolítja el az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="ef7d3-110">A DeleteRunningTask paraméter ellátása eltávolítja a projekthez társított összes Azure adatbázis-áttelepítési szolgáltatási feladatot.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="ef7d3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ef7d3-111">EXAMPLES</span></span>

### <span data-ttu-id="ef7d3-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef7d3-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="ef7d3-113">A fenti példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás myDMProject nevű projektjét az Azure-tól az Azure-ról a név beviteli paraméter alapján.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="ef7d3-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ef7d3-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="ef7d3-115">A fenti példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás projektjét a PSProject objektumon alapuló bemeneti paraméterként.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="ef7d3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef7d3-116">PARAMETERS</span></span>

### <span data-ttu-id="ef7d3-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef7d3-117">-Confirm</span></span>
<span data-ttu-id="ef7d3-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7d3-119">-DefaultProfile</span></span>
<span data-ttu-id="ef7d3-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef7d3-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="ef7d3-121">-DeleteRunningTask</span></span>
<span data-ttu-id="ef7d3-122">Bármely futó tevékenység törlése</span><span class="sxs-lookup"><span data-stu-id="ef7d3-122">Delete any running task</span></span>

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

### <span data-ttu-id="ef7d3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ef7d3-123">-Force</span></span>
<span data-ttu-id="ef7d3-124">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="ef7d3-124">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ef7d3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef7d3-125">-InputObject</span></span>
<span data-ttu-id="ef7d3-126">PSProject objektum</span><span class="sxs-lookup"><span data-stu-id="ef7d3-126">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7d3-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef7d3-127">-Name</span></span>
<span data-ttu-id="ef7d3-128">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7d3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef7d3-129">-PassThru</span></span>
<span data-ttu-id="ef7d3-130">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-130">Returns an true/false.</span></span>
<span data-ttu-id="ef7d3-131">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef7d3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7d3-132">-ResourceGroupName</span></span>
<span data-ttu-id="ef7d3-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef7d3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef7d3-134">-ResourceId</span></span>
<span data-ttu-id="ef7d3-135">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="ef7d3-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="ef7d3-136">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="ef7d3-136">-ServiceName</span></span>
<span data-ttu-id="ef7d3-137">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-137">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="ef7d3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7d3-138">-WhatIf</span></span>
<span data-ttu-id="ef7d3-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef7d3-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef7d3-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="ef7d3-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef7d3-141">INPUTS</span></span>

### <span data-ttu-id="ef7d3-142">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="ef7d3-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="ef7d3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ef7d3-143">System.String</span></span>


## <span data-ttu-id="ef7d3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef7d3-144">OUTPUTS</span></span>

### <span data-ttu-id="ef7d3-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef7d3-145">System.Boolean</span></span>


## <span data-ttu-id="ef7d3-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef7d3-146">NOTES</span></span>

## <span data-ttu-id="ef7d3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef7d3-147">RELATED LINKS</span></span>

