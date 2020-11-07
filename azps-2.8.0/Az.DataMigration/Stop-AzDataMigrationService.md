---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: b838cef6b72c783c8a9252df1e448e27bd100e36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666752"
---
# <span data-ttu-id="48b86-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="48b86-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="48b86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48b86-102">SYNOPSIS</span></span>
<span data-ttu-id="48b86-103">Leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotban lévő példányát.</span><span class="sxs-lookup"><span data-stu-id="48b86-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="48b86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48b86-104">SYNTAX</span></span>

### <span data-ttu-id="48b86-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48b86-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b86-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48b86-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b86-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48b86-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b86-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="48b86-108">DESCRIPTION</span></span>
<span data-ttu-id="48b86-109">Az Stop-AzDataMigrationService parancsmag leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotú példányát.</span><span class="sxs-lookup"><span data-stu-id="48b86-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="48b86-110">Példák</span><span class="sxs-lookup"><span data-stu-id="48b86-110">EXAMPLES</span></span>

### <span data-ttu-id="48b86-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48b86-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="48b86-112">A fenti példa leállítja az Azure-adatbázis áttelepítési szolgáltatásának az "TestService" nevű példányát, amely bemeneti paraméterként lett átadva a szolgáltatás neve mezőbe.</span><span class="sxs-lookup"><span data-stu-id="48b86-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="48b86-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="48b86-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="48b86-114">A fenti példa leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát, amely a PSDataMigrationService objektum bemeneti paraméterként lett átadva.</span><span class="sxs-lookup"><span data-stu-id="48b86-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="48b86-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48b86-115">PARAMETERS</span></span>

### <span data-ttu-id="48b86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b86-116">-DefaultProfile</span></span>
<span data-ttu-id="48b86-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48b86-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48b86-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48b86-118">-InputObject</span></span>
<span data-ttu-id="48b86-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="48b86-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="48b86-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48b86-120">-Name</span></span>
<span data-ttu-id="48b86-121">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="48b86-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="48b86-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48b86-122">-PassThru</span></span>
<span data-ttu-id="48b86-123">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="48b86-123">Returns an true/false.</span></span>
<span data-ttu-id="48b86-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="48b86-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48b86-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b86-125">-ResourceGroupName</span></span>
<span data-ttu-id="48b86-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="48b86-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="48b86-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48b86-127">-ResourceId</span></span>
<span data-ttu-id="48b86-128">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="48b86-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="48b86-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48b86-129">-Confirm</span></span>
<span data-ttu-id="48b86-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48b86-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b86-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b86-131">-WhatIf</span></span>
<span data-ttu-id="48b86-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48b86-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48b86-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48b86-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b86-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b86-134">CommonParameters</span></span>
<span data-ttu-id="48b86-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48b86-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b86-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b86-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b86-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48b86-137">INPUTS</span></span>

### <span data-ttu-id="48b86-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="48b86-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="48b86-139">System. String</span><span class="sxs-lookup"><span data-stu-id="48b86-139">System.String</span></span>

## <span data-ttu-id="48b86-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48b86-140">OUTPUTS</span></span>

### <span data-ttu-id="48b86-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48b86-141">System.Boolean</span></span>

## <span data-ttu-id="48b86-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48b86-142">NOTES</span></span>

## <span data-ttu-id="48b86-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48b86-143">RELATED LINKS</span></span>
