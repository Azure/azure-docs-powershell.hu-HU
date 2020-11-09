---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297599"
---
# <span data-ttu-id="52db7-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="52db7-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="52db7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52db7-102">SYNOPSIS</span></span>
<span data-ttu-id="52db7-103">Eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="52db7-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="52db7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52db7-104">SYNTAX</span></span>

### <span data-ttu-id="52db7-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52db7-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52db7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52db7-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52db7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52db7-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52db7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="52db7-108">DESCRIPTION</span></span>
<span data-ttu-id="52db7-109">A Remove-AzDataMigrationService parancsmag eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának példányát az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="52db7-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="52db7-110">A DeleteRunningTask paraméter ellátása eltávolítja az összes, az Azure adatbázis áttelepítési szolgáltatási feladatát, amely az eltávolítandó szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="52db7-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="52db7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="52db7-111">EXAMPLES</span></span>

### <span data-ttu-id="52db7-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="52db7-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="52db7-113">A fenti példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás TestService nevű példányát, amely egy MyResourceGroup nevű Azure Resource csoportban található.</span><span class="sxs-lookup"><span data-stu-id="52db7-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="52db7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52db7-114">PARAMETERS</span></span>

### <span data-ttu-id="52db7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52db7-115">-DefaultProfile</span></span>
<span data-ttu-id="52db7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52db7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52db7-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="52db7-117">-DeleteRunningTask</span></span>
<span data-ttu-id="52db7-118">Bármely futó tevékenység törlése</span><span class="sxs-lookup"><span data-stu-id="52db7-118">Delete any running task</span></span>

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

### <span data-ttu-id="52db7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="52db7-119">-Force</span></span>
<span data-ttu-id="52db7-120">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="52db7-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="52db7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52db7-121">-InputObject</span></span>
<span data-ttu-id="52db7-122">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="52db7-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52db7-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52db7-123">-Name</span></span>
<span data-ttu-id="52db7-124">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="52db7-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52db7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52db7-125">-PassThru</span></span>
<span data-ttu-id="52db7-126">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="52db7-126">Returns an true/false.</span></span>
<span data-ttu-id="52db7-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="52db7-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52db7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52db7-128">-ResourceGroupName</span></span>
<span data-ttu-id="52db7-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52db7-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="52db7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52db7-130">-ResourceId</span></span>
<span data-ttu-id="52db7-131">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="52db7-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="52db7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52db7-132">-Confirm</span></span>
<span data-ttu-id="52db7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52db7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52db7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52db7-134">-WhatIf</span></span>
<span data-ttu-id="52db7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52db7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52db7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52db7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52db7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52db7-137">CommonParameters</span></span>
<span data-ttu-id="52db7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52db7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52db7-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52db7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52db7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52db7-140">INPUTS</span></span>

### <span data-ttu-id="52db7-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="52db7-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="52db7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="52db7-142">System.String</span></span>

## <span data-ttu-id="52db7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52db7-143">OUTPUTS</span></span>

### <span data-ttu-id="52db7-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52db7-144">System.Boolean</span></span>

## <span data-ttu-id="52db7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52db7-145">NOTES</span></span>

## <span data-ttu-id="52db7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52db7-146">RELATED LINKS</span></span>
