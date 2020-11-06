---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: 677e89dd0def314744e507c6e61c745f39a081bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502944"
---
# <span data-ttu-id="eac83-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="eac83-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="eac83-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eac83-102">SYNOPSIS</span></span>
<span data-ttu-id="eac83-103">Eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="eac83-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eac83-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eac83-104">SYNTAX</span></span>

### <span data-ttu-id="eac83-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eac83-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac83-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac83-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac83-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac83-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac83-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eac83-108">DESCRIPTION</span></span>
<span data-ttu-id="eac83-109">A Remove-AzureRmDataMigrationService parancsmag eltávolítja az Azure-adatbázis áttelepítési szolgáltatásának példányát az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="eac83-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="eac83-110">A DeleteRunningTask paraméter ellátása eltávolítja az összes, az Azure adatbázis áttelepítési szolgáltatási feladatát, amely az eltávolítandó szolgáltatáshoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="eac83-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="eac83-111">Példák</span><span class="sxs-lookup"><span data-stu-id="eac83-111">EXAMPLES</span></span>

### <span data-ttu-id="eac83-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eac83-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="eac83-113">A fenti példa eltávolítja az Azure adatbázis-áttelepítési szolgáltatás TestService nevű példányát, amely egy MyResourceGroup nevű Azure Resource csoportban található.</span><span class="sxs-lookup"><span data-stu-id="eac83-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="eac83-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eac83-114">PARAMETERS</span></span>

### <span data-ttu-id="eac83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac83-115">-DefaultProfile</span></span>
<span data-ttu-id="eac83-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eac83-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eac83-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="eac83-117">-DeleteRunningTask</span></span>
<span data-ttu-id="eac83-118">Bármely futó tevékenység törlése</span><span class="sxs-lookup"><span data-stu-id="eac83-118">Delete any running task</span></span>

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

### <span data-ttu-id="eac83-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eac83-119">-Force</span></span>
<span data-ttu-id="eac83-120">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="eac83-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="eac83-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eac83-121">-InputObject</span></span>
<span data-ttu-id="eac83-122">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="eac83-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="eac83-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eac83-123">-Name</span></span>
<span data-ttu-id="eac83-124">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="eac83-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="eac83-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eac83-125">-PassThru</span></span>
<span data-ttu-id="eac83-126">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="eac83-126">Returns an true/false.</span></span>
<span data-ttu-id="eac83-127">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="eac83-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eac83-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac83-128">-ResourceGroupName</span></span>
<span data-ttu-id="eac83-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eac83-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="eac83-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eac83-130">-ResourceId</span></span>
<span data-ttu-id="eac83-131">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="eac83-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="eac83-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eac83-132">-Confirm</span></span>
<span data-ttu-id="eac83-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eac83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac83-134">-WhatIf</span></span>
<span data-ttu-id="eac83-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eac83-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac83-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eac83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac83-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac83-137">CommonParameters</span></span>
<span data-ttu-id="eac83-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eac83-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac83-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eac83-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac83-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eac83-140">INPUTS</span></span>

### <span data-ttu-id="eac83-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="eac83-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="eac83-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eac83-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="eac83-143">System. String</span><span class="sxs-lookup"><span data-stu-id="eac83-143">System.String</span></span>

## <span data-ttu-id="eac83-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eac83-144">OUTPUTS</span></span>

### <span data-ttu-id="eac83-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eac83-145">System.Boolean</span></span>

## <span data-ttu-id="eac83-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eac83-146">NOTES</span></span>

## <span data-ttu-id="eac83-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eac83-147">RELATED LINKS</span></span>
