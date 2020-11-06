---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Start-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: a8440ddc7249068486f94c30e28e1b1be2e2413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505400"
---
# <span data-ttu-id="f4583-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f4583-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="f4583-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4583-102">SYNOPSIS</span></span>
<span data-ttu-id="f4583-103">Elindítja az Azure adatbázis áttelepítési szolgáltatásának példányát egy leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="f4583-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4583-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4583-104">SYNTAX</span></span>

### <span data-ttu-id="f4583-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4583-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4583-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4583-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4583-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4583-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4583-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4583-108">DESCRIPTION</span></span>
<span data-ttu-id="f4583-109">A Start-AzureRmDataMigrationService parancsmag az Azure-adatbázis áttelepítési szolgáltatásának egy példányát leállított állapotban indítja el.</span><span class="sxs-lookup"><span data-stu-id="f4583-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="f4583-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f4583-110">EXAMPLES</span></span>

### <span data-ttu-id="f4583-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4583-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="f4583-112">A fenti példa elindítja az Azure adatbázis-áttelepítési szolgáltatás példányát egy teszt</span><span class="sxs-lookup"><span data-stu-id="f4583-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="f4583-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f4583-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="f4583-114">A fenti példa egy Azure adatbázis-áttelepítési szolgáltatás példányát indítja el bemeneti paraméterként átadott PSDataMigrationService alapján.</span><span class="sxs-lookup"><span data-stu-id="f4583-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="f4583-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4583-115">PARAMETERS</span></span>

### <span data-ttu-id="f4583-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4583-116">-DefaultProfile</span></span>
<span data-ttu-id="f4583-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4583-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4583-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4583-118">-InputObject</span></span>
<span data-ttu-id="f4583-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="f4583-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="f4583-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4583-120">-Name</span></span>
<span data-ttu-id="f4583-121">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="f4583-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="f4583-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4583-122">-PassThru</span></span>
<span data-ttu-id="f4583-123">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="f4583-123">Returns an true/false.</span></span>
<span data-ttu-id="f4583-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="f4583-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4583-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4583-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4583-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4583-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4583-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4583-127">-ResourceId</span></span>
<span data-ttu-id="f4583-128">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f4583-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="f4583-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4583-129">-Confirm</span></span>
<span data-ttu-id="f4583-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4583-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4583-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4583-131">-WhatIf</span></span>
<span data-ttu-id="f4583-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4583-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4583-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4583-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4583-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4583-134">CommonParameters</span></span>
<span data-ttu-id="f4583-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4583-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4583-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4583-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4583-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4583-137">INPUTS</span></span>

### <span data-ttu-id="f4583-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f4583-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="f4583-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4583-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f4583-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f4583-140">System.String</span></span>

## <span data-ttu-id="f4583-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4583-141">OUTPUTS</span></span>

### <span data-ttu-id="f4583-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4583-142">System.Boolean</span></span>

## <span data-ttu-id="f4583-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4583-143">NOTES</span></span>

## <span data-ttu-id="f4583-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4583-144">RELATED LINKS</span></span>
