---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014550"
---
# <span data-ttu-id="38dd8-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="38dd8-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="38dd8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="38dd8-103">Egy futó államban futó Azure adatbázis-áttelepítési szolgáltatási feladat leállítása.</span><span class="sxs-lookup"><span data-stu-id="38dd8-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="38dd8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38dd8-104">SYNTAX</span></span>

### <span data-ttu-id="38dd8-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38dd8-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38dd8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38dd8-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38dd8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38dd8-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38dd8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="38dd8-108">DESCRIPTION</span></span>
<span data-ttu-id="38dd8-109">Stop-AzDataMigrationTask parancsmag az adatbázis-áttelepítési tevékenységet futási állapotba állítja.</span><span class="sxs-lookup"><span data-stu-id="38dd8-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="38dd8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="38dd8-110">EXAMPLES</span></span>

### <span data-ttu-id="38dd8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="38dd8-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="38dd8-112">A fenti példa leállítja az Azure adatbázis áttelepítési szolgáltatásának a myDMSTask nevű feladatot, amely a Project myDMSProject és az Azure Database Migration Service instance nevű TestService</span><span class="sxs-lookup"><span data-stu-id="38dd8-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="38dd8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="38dd8-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="38dd8-114">A fenti példa leállítja az Azure Database áttelepítési szolgáltatás tevékenységének bemeneti paraméterként PSProjectTask objektumként való átadását.</span><span class="sxs-lookup"><span data-stu-id="38dd8-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="38dd8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38dd8-115">PARAMETERS</span></span>

### <span data-ttu-id="38dd8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38dd8-116">-DefaultProfile</span></span>
<span data-ttu-id="38dd8-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38dd8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38dd8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38dd8-118">-InputObject</span></span>
<span data-ttu-id="38dd8-119">PSProjectTask objektum</span><span class="sxs-lookup"><span data-stu-id="38dd8-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="38dd8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38dd8-120">-Name</span></span>
<span data-ttu-id="38dd8-121">A tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="38dd8-121">The name of the task.</span></span>

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

### <span data-ttu-id="38dd8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38dd8-122">-PassThru</span></span>
<span data-ttu-id="38dd8-123">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="38dd8-123">Returns an true/false.</span></span>
<span data-ttu-id="38dd8-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="38dd8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="38dd8-125">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="38dd8-125">-ProjectName</span></span>
<span data-ttu-id="38dd8-126">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="38dd8-126">The name of the project.</span></span>

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

### <span data-ttu-id="38dd8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38dd8-127">-ResourceGroupName</span></span>
<span data-ttu-id="38dd8-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="38dd8-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="38dd8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38dd8-129">-ResourceId</span></span>
<span data-ttu-id="38dd8-130">ProjectTask erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="38dd8-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="38dd8-131">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="38dd8-131">-ServiceName</span></span>
<span data-ttu-id="38dd8-132">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="38dd8-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="38dd8-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38dd8-133">-Confirm</span></span>
<span data-ttu-id="38dd8-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38dd8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38dd8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38dd8-135">-WhatIf</span></span>
<span data-ttu-id="38dd8-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38dd8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38dd8-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38dd8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38dd8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38dd8-138">CommonParameters</span></span>
<span data-ttu-id="38dd8-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38dd8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38dd8-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38dd8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38dd8-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38dd8-141">INPUTS</span></span>

### <span data-ttu-id="38dd8-142">Microsoft. Azure. Command. DataMigration. models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="38dd8-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="38dd8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="38dd8-143">System.String</span></span>

## <span data-ttu-id="38dd8-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38dd8-144">OUTPUTS</span></span>

### <span data-ttu-id="38dd8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38dd8-145">System.Boolean</span></span>

## <span data-ttu-id="38dd8-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38dd8-146">NOTES</span></span>

## <span data-ttu-id="38dd8-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38dd8-147">RELATED LINKS</span></span>
