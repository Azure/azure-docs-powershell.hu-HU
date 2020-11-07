---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 67194bfc9a7ce1971817c7f80e7a5ee61caf6db0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671022"
---
# <span data-ttu-id="c6ee4-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c6ee4-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="c6ee4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ee4-103">Elindítja az Azure adatbázis áttelepítési szolgáltatásának példányát egy leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="c6ee4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6ee4-104">SYNTAX</span></span>

### <span data-ttu-id="c6ee4-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6ee4-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6ee4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6ee4-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6ee4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6ee4-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6ee4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6ee4-108">DESCRIPTION</span></span>
<span data-ttu-id="c6ee4-109">A Start-AzDataMigrationService parancsmag az Azure-adatbázis áttelepítési szolgáltatásának egy példányát leállított állapotban indítja el.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="c6ee4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c6ee4-110">EXAMPLES</span></span>

### <span data-ttu-id="c6ee4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6ee4-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="c6ee4-112">A fenti példa elindítja az Azure adatbázis-áttelepítési szolgáltatás példányát egy teszt</span><span class="sxs-lookup"><span data-stu-id="c6ee4-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="c6ee4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c6ee4-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="c6ee4-114">A fenti példa egy Azure adatbázis-áttelepítési szolgáltatás példányát indítja el bemeneti paraméterként átadott PSDataMigrationService alapján.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="c6ee4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6ee4-115">PARAMETERS</span></span>

### <span data-ttu-id="c6ee4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ee4-116">-DefaultProfile</span></span>
<span data-ttu-id="c6ee4-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6ee4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6ee4-118">-InputObject</span></span>
<span data-ttu-id="c6ee4-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="c6ee4-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="c6ee4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6ee4-120">-Name</span></span>
<span data-ttu-id="c6ee4-121">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="c6ee4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6ee4-122">-PassThru</span></span>
<span data-ttu-id="c6ee4-123">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-123">Returns an true/false.</span></span>
<span data-ttu-id="c6ee4-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6ee4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6ee4-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6ee4-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6ee4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6ee4-127">-ResourceId</span></span>
<span data-ttu-id="c6ee4-128">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="c6ee4-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6ee4-129">-Confirm</span></span>
<span data-ttu-id="c6ee4-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6ee4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6ee4-131">-WhatIf</span></span>
<span data-ttu-id="c6ee4-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6ee4-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6ee4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6ee4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ee4-134">CommonParameters</span></span>
<span data-ttu-id="c6ee4-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6ee4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ee4-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6ee4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ee4-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6ee4-137">INPUTS</span></span>

### <span data-ttu-id="c6ee4-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="c6ee4-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="c6ee4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6ee4-139">System.String</span></span>

## <span data-ttu-id="c6ee4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6ee4-140">OUTPUTS</span></span>

### <span data-ttu-id="c6ee4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6ee4-141">System.Boolean</span></span>

## <span data-ttu-id="c6ee4-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6ee4-142">NOTES</span></span>

## <span data-ttu-id="c6ee4-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6ee4-143">RELATED LINKS</span></span>
