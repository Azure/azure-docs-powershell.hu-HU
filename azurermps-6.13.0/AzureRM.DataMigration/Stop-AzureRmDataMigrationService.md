---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 59ec77f0c6e3a2f9389931e12ecbce155fe970bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495144"
---
# <span data-ttu-id="9898e-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9898e-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="9898e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9898e-102">SYNOPSIS</span></span>
<span data-ttu-id="9898e-103">Leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotban lévő példányát.</span><span class="sxs-lookup"><span data-stu-id="9898e-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9898e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9898e-104">SYNTAX</span></span>

### <span data-ttu-id="9898e-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9898e-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9898e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9898e-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9898e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9898e-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9898e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9898e-108">DESCRIPTION</span></span>
<span data-ttu-id="9898e-109">Az Stop-AzureRmDataMigrationService parancsmag leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotú példányát.</span><span class="sxs-lookup"><span data-stu-id="9898e-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="9898e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9898e-110">EXAMPLES</span></span>

### <span data-ttu-id="9898e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9898e-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="9898e-112">A fenti példa leállítja az Azure-adatbázis áttelepítési szolgáltatásának az "TestService" nevű példányát, amely bemeneti paraméterként lett átadva a szolgáltatás neve mezőbe.</span><span class="sxs-lookup"><span data-stu-id="9898e-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="9898e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9898e-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="9898e-114">A fenti példa leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát, amely a PSDataMigrationService objektum bemeneti paraméterként lett átadva.</span><span class="sxs-lookup"><span data-stu-id="9898e-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="9898e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9898e-115">PARAMETERS</span></span>

### <span data-ttu-id="9898e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9898e-116">-DefaultProfile</span></span>
<span data-ttu-id="9898e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9898e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9898e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9898e-118">-InputObject</span></span>
<span data-ttu-id="9898e-119">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="9898e-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="9898e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9898e-120">-Name</span></span>
<span data-ttu-id="9898e-121">Az adatbázis-áttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="9898e-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9898e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9898e-122">-PassThru</span></span>
<span data-ttu-id="9898e-123">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="9898e-123">Returns an true/false.</span></span>
<span data-ttu-id="9898e-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9898e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9898e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9898e-125">-ResourceGroupName</span></span>
<span data-ttu-id="9898e-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9898e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9898e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9898e-127">-ResourceId</span></span>
<span data-ttu-id="9898e-128">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9898e-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="9898e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9898e-129">-Confirm</span></span>
<span data-ttu-id="9898e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9898e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9898e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9898e-131">-WhatIf</span></span>
<span data-ttu-id="9898e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9898e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9898e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9898e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9898e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9898e-134">CommonParameters</span></span>
<span data-ttu-id="9898e-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9898e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9898e-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9898e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9898e-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9898e-137">INPUTS</span></span>

### <span data-ttu-id="9898e-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9898e-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="9898e-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9898e-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9898e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9898e-140">System.String</span></span>

## <span data-ttu-id="9898e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9898e-141">OUTPUTS</span></span>

### <span data-ttu-id="9898e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9898e-142">System.Boolean</span></span>

## <span data-ttu-id="9898e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9898e-143">NOTES</span></span>

## <span data-ttu-id="9898e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9898e-144">RELATED LINKS</span></span>
