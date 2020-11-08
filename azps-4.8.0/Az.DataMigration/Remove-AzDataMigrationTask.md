---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184576"
---
# <span data-ttu-id="602b6-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="602b6-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="602b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="602b6-102">SYNOPSIS</span></span>
<span data-ttu-id="602b6-103">Az Azure adatbázis-áttelepítési szolgáltatás tevékenységének eltávolítása az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="602b6-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="602b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="602b6-104">SYNTAX</span></span>

### <span data-ttu-id="602b6-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="602b6-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="602b6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="602b6-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="602b6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="602b6-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="602b6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="602b6-108">DESCRIPTION</span></span>
<span data-ttu-id="602b6-109">Az Remove-AzDataMigrationTask parancsmag eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának feladatát az Azureról.</span><span class="sxs-lookup"><span data-stu-id="602b6-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="602b6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="602b6-110">EXAMPLES</span></span>

### <span data-ttu-id="602b6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="602b6-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="602b6-112">Az előző példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás TestTask nevű feladatát az Azure-ról a tevékenység neve paraméter alapján.</span><span class="sxs-lookup"><span data-stu-id="602b6-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="602b6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="602b6-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="602b6-114">Az előző példa eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának feladatát az PSProjectTask objektum által átadott adatok alapján.</span><span class="sxs-lookup"><span data-stu-id="602b6-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="602b6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="602b6-115">PARAMETERS</span></span>

### <span data-ttu-id="602b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="602b6-116">-DefaultProfile</span></span>
<span data-ttu-id="602b6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="602b6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="602b6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="602b6-118">-Force</span></span>
<span data-ttu-id="602b6-119">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="602b6-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="602b6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="602b6-120">-InputObject</span></span>
<span data-ttu-id="602b6-121">PSProjectTask objektum</span><span class="sxs-lookup"><span data-stu-id="602b6-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="602b6-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="602b6-122">-Name</span></span>
<span data-ttu-id="602b6-123">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="602b6-123">The name of the task.</span></span>

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

### <span data-ttu-id="602b6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="602b6-124">-PassThru</span></span>
<span data-ttu-id="602b6-125">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="602b6-125">Returns an true/false.</span></span>
<span data-ttu-id="602b6-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="602b6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="602b6-127">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="602b6-127">-ProjectName</span></span>
<span data-ttu-id="602b6-128">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="602b6-128">The name of the project.</span></span>

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

### <span data-ttu-id="602b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="602b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="602b6-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="602b6-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="602b6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="602b6-131">-ResourceId</span></span>
<span data-ttu-id="602b6-132">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="602b6-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="602b6-133">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="602b6-133">-ServiceName</span></span>
<span data-ttu-id="602b6-134">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="602b6-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="602b6-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="602b6-135">-Confirm</span></span>
<span data-ttu-id="602b6-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="602b6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="602b6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="602b6-137">-WhatIf</span></span>
<span data-ttu-id="602b6-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="602b6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="602b6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="602b6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="602b6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="602b6-140">CommonParameters</span></span>
<span data-ttu-id="602b6-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="602b6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="602b6-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="602b6-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="602b6-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="602b6-143">INPUTS</span></span>

### <span data-ttu-id="602b6-144">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="602b6-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="602b6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="602b6-145">System.String</span></span>

## <span data-ttu-id="602b6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="602b6-146">OUTPUTS</span></span>

### <span data-ttu-id="602b6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="602b6-147">System.Boolean</span></span>

## <span data-ttu-id="602b6-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="602b6-148">NOTES</span></span>

## <span data-ttu-id="602b6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="602b6-149">RELATED LINKS</span></span>
