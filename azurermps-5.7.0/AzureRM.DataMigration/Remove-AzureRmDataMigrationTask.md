---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498967"
---
# <span data-ttu-id="ad34a-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="ad34a-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="ad34a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad34a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad34a-103">Az Azure adatbázis-áttelepítési szolgáltatás tevékenységének eltávolítása az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="ad34a-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad34a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad34a-104">SYNTAX</span></span>

### <span data-ttu-id="ad34a-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad34a-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ad34a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad34a-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ad34a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad34a-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ad34a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad34a-108">DESCRIPTION</span></span>
<span data-ttu-id="ad34a-109">Az Remove-AzureRmDataMigrationTask parancsmag eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának feladatát az Azureról.</span><span class="sxs-lookup"><span data-stu-id="ad34a-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="ad34a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ad34a-110">EXAMPLES</span></span>

### <span data-ttu-id="ad34a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad34a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="ad34a-112">Az előző példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás TestTask nevű feladatát az Azure-ról a tevékenység neve paraméter alapján.</span><span class="sxs-lookup"><span data-stu-id="ad34a-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="ad34a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ad34a-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="ad34a-114">Az előző példa eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának feladatát az PSProjectTask objektum által átadott adatok alapján.</span><span class="sxs-lookup"><span data-stu-id="ad34a-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="ad34a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad34a-115">PARAMETERS</span></span>

### <span data-ttu-id="ad34a-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad34a-116">-Confirm</span></span>
<span data-ttu-id="ad34a-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad34a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad34a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad34a-118">-DefaultProfile</span></span>
<span data-ttu-id="ad34a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad34a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad34a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ad34a-120">-Force</span></span>
<span data-ttu-id="ad34a-121">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="ad34a-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ad34a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad34a-122">-InputObject</span></span>
<span data-ttu-id="ad34a-123">PSProjectTask objektum</span><span class="sxs-lookup"><span data-stu-id="ad34a-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad34a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad34a-124">-Name</span></span>
<span data-ttu-id="ad34a-125">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="ad34a-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad34a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad34a-126">-PassThru</span></span>
<span data-ttu-id="ad34a-127">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ad34a-127">Returns an true/false.</span></span>
<span data-ttu-id="ad34a-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ad34a-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ad34a-129">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="ad34a-129">-ProjectName</span></span>
<span data-ttu-id="ad34a-130">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="ad34a-130">The name of the project.</span></span>

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

### <span data-ttu-id="ad34a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad34a-131">-ResourceGroupName</span></span>
<span data-ttu-id="ad34a-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad34a-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad34a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad34a-133">-ResourceId</span></span>
<span data-ttu-id="ad34a-134">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="ad34a-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="ad34a-135">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="ad34a-135">-ServiceName</span></span>
<span data-ttu-id="ad34a-136">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="ad34a-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="ad34a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad34a-137">-WhatIf</span></span>
<span data-ttu-id="ad34a-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad34a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad34a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad34a-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="ad34a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad34a-140">INPUTS</span></span>

### <span data-ttu-id="ad34a-141">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="ad34a-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="ad34a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ad34a-142">System.String</span></span>


## <span data-ttu-id="ad34a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad34a-143">OUTPUTS</span></span>

### <span data-ttu-id="ad34a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad34a-144">System.Boolean</span></span>


## <span data-ttu-id="ad34a-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad34a-145">NOTES</span></span>

## <span data-ttu-id="ad34a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad34a-146">RELATED LINKS</span></span>


