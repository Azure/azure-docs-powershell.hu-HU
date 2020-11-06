---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492284"
---
# <span data-ttu-id="b03b2-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b03b2-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="b03b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b03b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b03b2-103">Elindítja az Azure adatbázis áttelepítési szolgáltatásának példányát egy leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="b03b2-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b03b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b03b2-104">SYNTAX</span></span>

### <span data-ttu-id="b03b2-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b03b2-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b03b2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03b2-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b03b2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03b2-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b03b2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b03b2-108">DESCRIPTION</span></span>
<span data-ttu-id="b03b2-109">A Start-AzureRmDataMigrationService parancsmag az Azure-adatbázis áttelepítési szolgáltatásának egy példányát leállított állapotban indítja el.</span><span class="sxs-lookup"><span data-stu-id="b03b2-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="b03b2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b03b2-110">EXAMPLES</span></span>

### <span data-ttu-id="b03b2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b03b2-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="b03b2-112">A fenti példa elindítja az Azure adatbázis-áttelepítési szolgáltatás példányát egy teszt</span><span class="sxs-lookup"><span data-stu-id="b03b2-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="b03b2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b03b2-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="b03b2-114">A fenti példa egy Azure adatbázis-áttelepítési szolgáltatás példányát indítja el bemeneti paraméterként átadott PSDataMigrationService alapján.</span><span class="sxs-lookup"><span data-stu-id="b03b2-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="b03b2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b03b2-115">PARAMETERS</span></span>

### <span data-ttu-id="b03b2-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b03b2-116">-Confirm</span></span>
<span data-ttu-id="b03b2-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b03b2-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03b2-118">-DefaultProfile</span></span>
<span data-ttu-id="b03b2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b03b2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b03b2-120">-InputObject</span></span>
<span data-ttu-id="b03b2-121">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="b03b2-121">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b03b2-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b03b2-122">-Name</span></span>
<span data-ttu-id="b03b2-123">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="b03b2-123">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b03b2-124">-PassThru</span></span>
<span data-ttu-id="b03b2-125">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="b03b2-125">Returns an true/false.</span></span>
<span data-ttu-id="b03b2-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b03b2-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="b03b2-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b03b2-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b03b2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b03b2-129">-ResourceId</span></span>
<span data-ttu-id="b03b2-130">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b03b2-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b03b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03b2-131">-WhatIf</span></span>
<span data-ttu-id="b03b2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b03b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03b2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b03b2-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="b03b2-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b03b2-134">INPUTS</span></span>

### <span data-ttu-id="b03b2-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b03b2-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="b03b2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b03b2-136">System.String</span></span>


## <span data-ttu-id="b03b2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b03b2-137">OUTPUTS</span></span>

### <span data-ttu-id="b03b2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b03b2-138">System.Boolean</span></span>


## <span data-ttu-id="b03b2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b03b2-139">NOTES</span></span>

## <span data-ttu-id="b03b2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b03b2-140">RELATED LINKS</span></span>


