---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672863"
---
# <span data-ttu-id="7ed9f-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="7ed9f-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="7ed9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ed9f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed9f-103">Egy futó államban futó Azure adatbázis-áttelepítési szolgáltatási feladat leállítása.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ed9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ed9f-104">SYNTAX</span></span>

### <span data-ttu-id="7ed9f-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ed9f-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7ed9f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed9f-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7ed9f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed9f-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7ed9f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ed9f-108">DESCRIPTION</span></span>
<span data-ttu-id="7ed9f-109">Stop-AzureRmDataMigrationTask parancsmag az adatbázis-áttelepítési tevékenységet futási állapotba állítja.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="7ed9f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7ed9f-110">EXAMPLES</span></span>

### <span data-ttu-id="7ed9f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ed9f-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="7ed9f-112">A fenti példa leállítja az Azure adatbázis áttelepítési szolgáltatásának a myDMSTask nevű feladatot, amely a Project myDMSProject és az Azure Database Migration Service instance nevű TestService</span><span class="sxs-lookup"><span data-stu-id="7ed9f-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="7ed9f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7ed9f-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="7ed9f-114">A fenti példa leállítja az Azure Database áttelepítési szolgáltatás tevékenységének bemeneti paraméterként PSProjectTask objektumként való átadását.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="7ed9f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ed9f-115">PARAMETERS</span></span>

### <span data-ttu-id="7ed9f-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ed9f-116">-Confirm</span></span>
<span data-ttu-id="7ed9f-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed9f-118">-DefaultProfile</span></span>
<span data-ttu-id="7ed9f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ed9f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ed9f-120">-InputObject</span></span>
<span data-ttu-id="7ed9f-121">PSProjectTask objektum</span><span class="sxs-lookup"><span data-stu-id="7ed9f-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="7ed9f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ed9f-122">-Name</span></span>
<span data-ttu-id="7ed9f-123">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-123">The name of the task.</span></span>

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

### <span data-ttu-id="7ed9f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ed9f-124">-PassThru</span></span>
<span data-ttu-id="7ed9f-125">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-125">Returns an true/false.</span></span>
<span data-ttu-id="7ed9f-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7ed9f-127">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="7ed9f-127">-ProjectName</span></span>
<span data-ttu-id="7ed9f-128">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-128">The name of the project.</span></span>

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

### <span data-ttu-id="7ed9f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed9f-129">-ResourceGroupName</span></span>
<span data-ttu-id="7ed9f-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-130">The name of the resource group .</span></span>

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

### <span data-ttu-id="7ed9f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ed9f-131">-ResourceId</span></span>
<span data-ttu-id="7ed9f-132">ProjectTask erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-132">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="7ed9f-133">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="7ed9f-133">-ServiceName</span></span>
<span data-ttu-id="7ed9f-134">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-134">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="7ed9f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed9f-135">-WhatIf</span></span>
<span data-ttu-id="7ed9f-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed9f-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ed9f-137">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="7ed9f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ed9f-138">INPUTS</span></span>

### <span data-ttu-id="7ed9f-139">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="7ed9f-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="7ed9f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7ed9f-140">System.String</span></span>


## <span data-ttu-id="7ed9f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ed9f-141">OUTPUTS</span></span>

### <span data-ttu-id="7ed9f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ed9f-142">System.Boolean</span></span>


## <span data-ttu-id="7ed9f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ed9f-143">NOTES</span></span>

## <span data-ttu-id="7ed9f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ed9f-144">RELATED LINKS</span></span>

