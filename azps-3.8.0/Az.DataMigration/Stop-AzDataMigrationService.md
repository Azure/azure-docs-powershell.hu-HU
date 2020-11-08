---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014552"
---
# <span data-ttu-id="8cbdf-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8cbdf-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="8cbdf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cbdf-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbdf-103">Leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotban lévő példányát.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="8cbdf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cbdf-104">SYNTAX</span></span>

### <span data-ttu-id="8cbdf-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8cbdf-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cbdf-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cbdf-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cbdf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cbdf-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cbdf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cbdf-108">DESCRIPTION</span></span>
<span data-ttu-id="8cbdf-109">Az Stop-AzDataMigrationService parancsmag leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotú példányát.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="8cbdf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8cbdf-110">EXAMPLES</span></span>

### <span data-ttu-id="8cbdf-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8cbdf-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="8cbdf-112">A fenti példa leállítja az Azure-adatbázis áttelepítési szolgáltatásának az "TestService" nevű példányát, amely bemeneti paraméterként lett átadva a szolgáltatás neve mezőbe.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="8cbdf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8cbdf-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="8cbdf-114">A fenti példa leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát, amely a PSDataMigrationService objektum bemeneti paraméterként lett átadva.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="8cbdf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cbdf-115">PARAMETERS</span></span>

### <span data-ttu-id="8cbdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbdf-116">-DefaultProfile</span></span>
<span data-ttu-id="8cbdf-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cbdf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cbdf-118">-InputObject</span></span>
<span data-ttu-id="8cbdf-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="8cbdf-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="8cbdf-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8cbdf-120">-Name</span></span>
<span data-ttu-id="8cbdf-121">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="8cbdf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cbdf-122">-PassThru</span></span>
<span data-ttu-id="8cbdf-123">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-123">Returns an true/false.</span></span>
<span data-ttu-id="8cbdf-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cbdf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbdf-125">-ResourceGroupName</span></span>
<span data-ttu-id="8cbdf-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="8cbdf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbdf-127">-ResourceId</span></span>
<span data-ttu-id="8cbdf-128">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="8cbdf-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8cbdf-129">-Confirm</span></span>
<span data-ttu-id="8cbdf-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cbdf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cbdf-131">-WhatIf</span></span>
<span data-ttu-id="8cbdf-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cbdf-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8cbdf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cbdf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbdf-134">CommonParameters</span></span>
<span data-ttu-id="8cbdf-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cbdf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbdf-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbdf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbdf-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cbdf-137">INPUTS</span></span>

### <span data-ttu-id="8cbdf-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8cbdf-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="8cbdf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8cbdf-139">System.String</span></span>

## <span data-ttu-id="8cbdf-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cbdf-140">OUTPUTS</span></span>

### <span data-ttu-id="8cbdf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8cbdf-141">System.Boolean</span></span>

## <span data-ttu-id="8cbdf-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cbdf-142">NOTES</span></span>

## <span data-ttu-id="8cbdf-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cbdf-143">RELATED LINKS</span></span>
