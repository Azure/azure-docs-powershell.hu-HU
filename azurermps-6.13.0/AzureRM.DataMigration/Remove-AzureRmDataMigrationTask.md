---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: 295ac647bcbe04e26e761e4fdf8fe2bd30282218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504436"
---
# <span data-ttu-id="3474d-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="3474d-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="3474d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3474d-102">SYNOPSIS</span></span>
<span data-ttu-id="3474d-103">Az Azure adatbázis-áttelepítési szolgáltatás tevékenységének eltávolítása az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="3474d-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3474d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3474d-104">SYNTAX</span></span>

### <span data-ttu-id="3474d-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3474d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3474d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3474d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3474d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3474d-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3474d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3474d-108">DESCRIPTION</span></span>
<span data-ttu-id="3474d-109">Az Remove-AzureRmDataMigrationTask parancsmag eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának feladatát az Azureról.</span><span class="sxs-lookup"><span data-stu-id="3474d-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="3474d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3474d-110">EXAMPLES</span></span>

### <span data-ttu-id="3474d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3474d-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="3474d-112">Az előző példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás TestTask nevű feladatát az Azure-ról a tevékenység neve paraméter alapján.</span><span class="sxs-lookup"><span data-stu-id="3474d-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="3474d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3474d-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="3474d-114">Az előző példa eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának feladatát az PSProjectTask objektum által átadott adatok alapján.</span><span class="sxs-lookup"><span data-stu-id="3474d-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="3474d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3474d-115">PARAMETERS</span></span>

### <span data-ttu-id="3474d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3474d-116">-DefaultProfile</span></span>
<span data-ttu-id="3474d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3474d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3474d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3474d-118">-Force</span></span>
<span data-ttu-id="3474d-119">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="3474d-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3474d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3474d-120">-InputObject</span></span>
<span data-ttu-id="3474d-121">PSProjectTask objektum</span><span class="sxs-lookup"><span data-stu-id="3474d-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3474d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3474d-122">-Name</span></span>
<span data-ttu-id="3474d-123">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="3474d-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3474d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3474d-124">-PassThru</span></span>
<span data-ttu-id="3474d-125">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3474d-125">Returns an true/false.</span></span>
<span data-ttu-id="3474d-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3474d-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3474d-127">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="3474d-127">-ProjectName</span></span>
<span data-ttu-id="3474d-128">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="3474d-128">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3474d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3474d-129">-ResourceGroupName</span></span>
<span data-ttu-id="3474d-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3474d-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3474d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3474d-131">-ResourceId</span></span>
<span data-ttu-id="3474d-132">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="3474d-132">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3474d-133">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="3474d-133">-ServiceName</span></span>
<span data-ttu-id="3474d-134">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="3474d-134">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3474d-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3474d-135">-Confirm</span></span>
<span data-ttu-id="3474d-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3474d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3474d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3474d-137">-WhatIf</span></span>
<span data-ttu-id="3474d-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3474d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3474d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3474d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3474d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3474d-140">CommonParameters</span></span>
<span data-ttu-id="3474d-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3474d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3474d-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3474d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3474d-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3474d-143">INPUTS</span></span>

### <span data-ttu-id="3474d-144">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="3474d-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="3474d-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3474d-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="3474d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3474d-146">System.String</span></span>

## <span data-ttu-id="3474d-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3474d-147">OUTPUTS</span></span>

### <span data-ttu-id="3474d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3474d-148">System.Boolean</span></span>

## <span data-ttu-id="3474d-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3474d-149">NOTES</span></span>

## <span data-ttu-id="3474d-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3474d-150">RELATED LINKS</span></span>
