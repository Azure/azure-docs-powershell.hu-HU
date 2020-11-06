---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 5aada0f82b8d2a11486e3dde2f4b806f735979e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502943"
---
# <span data-ttu-id="e8df4-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e8df4-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="e8df4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8df4-102">SYNOPSIS</span></span>
<span data-ttu-id="e8df4-103">Az Azure adatbázis-áttelepítési szolgáltatás projekt eltávolítása az Azure-ról</span><span class="sxs-lookup"><span data-stu-id="e8df4-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8df4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8df4-104">SYNTAX</span></span>

### <span data-ttu-id="e8df4-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8df4-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8df4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8df4-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8df4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8df4-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8df4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8df4-108">DESCRIPTION</span></span>
<span data-ttu-id="e8df4-109">A Remove-AzureRmDataMigrationProject parancsmag az Azure adatbázis-áttelepítési szolgáltatás projektjét távolítja el az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="e8df4-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="e8df4-110">A DeleteRunningTask paraméter ellátása eltávolítja a projekthez társított összes Azure adatbázis-áttelepítési szolgáltatási feladatot.</span><span class="sxs-lookup"><span data-stu-id="e8df4-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="e8df4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e8df4-111">EXAMPLES</span></span>

### <span data-ttu-id="e8df4-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8df4-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="e8df4-113">A fenti példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás myDMProject nevű projektjét az Azure-tól az Azure-ról a név beviteli paraméter alapján.</span><span class="sxs-lookup"><span data-stu-id="e8df4-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="e8df4-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e8df4-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="e8df4-115">A fenti példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás projektjét a PSProject objektumon alapuló bemeneti paraméterként.</span><span class="sxs-lookup"><span data-stu-id="e8df4-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="e8df4-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8df4-116">PARAMETERS</span></span>

### <span data-ttu-id="e8df4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8df4-117">-DefaultProfile</span></span>
<span data-ttu-id="e8df4-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8df4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8df4-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="e8df4-119">-DeleteRunningTask</span></span>
<span data-ttu-id="e8df4-120">Bármely futó tevékenység törlése</span><span class="sxs-lookup"><span data-stu-id="e8df4-120">Delete any running task</span></span>

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

### <span data-ttu-id="e8df4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e8df4-121">-Force</span></span>
<span data-ttu-id="e8df4-122">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="e8df4-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e8df4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8df4-123">-InputObject</span></span>
<span data-ttu-id="e8df4-124">PSProject objektum</span><span class="sxs-lookup"><span data-stu-id="e8df4-124">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8df4-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8df4-125">-Name</span></span>
<span data-ttu-id="e8df4-126">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="e8df4-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8df4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8df4-127">-PassThru</span></span>
<span data-ttu-id="e8df4-128">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="e8df4-128">Returns an true/false.</span></span>
<span data-ttu-id="e8df4-129">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e8df4-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8df4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8df4-130">-ResourceGroupName</span></span>
<span data-ttu-id="e8df4-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e8df4-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8df4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8df4-132">-ResourceId</span></span>
<span data-ttu-id="e8df4-133">Projekt-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="e8df4-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="e8df4-134">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="e8df4-134">-ServiceName</span></span>
<span data-ttu-id="e8df4-135">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="e8df4-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e8df4-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8df4-136">-Confirm</span></span>
<span data-ttu-id="e8df4-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8df4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8df4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8df4-138">-WhatIf</span></span>
<span data-ttu-id="e8df4-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8df4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8df4-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8df4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8df4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8df4-141">CommonParameters</span></span>
<span data-ttu-id="e8df4-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8df4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8df4-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8df4-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8df4-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8df4-144">INPUTS</span></span>

### <span data-ttu-id="e8df4-145">Microsoft. Azure. Command. DataMigration. models. PSProject</span><span class="sxs-lookup"><span data-stu-id="e8df4-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="e8df4-146">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8df4-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e8df4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e8df4-147">System.String</span></span>

## <span data-ttu-id="e8df4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8df4-148">OUTPUTS</span></span>

### <span data-ttu-id="e8df4-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8df4-149">System.Boolean</span></span>

## <span data-ttu-id="e8df4-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8df4-150">NOTES</span></span>

## <span data-ttu-id="e8df4-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8df4-151">RELATED LINKS</span></span>
