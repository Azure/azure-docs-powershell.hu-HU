---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505527"
---
# <span data-ttu-id="26db0-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="26db0-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="26db0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26db0-102">SYNOPSIS</span></span>
<span data-ttu-id="26db0-103">Leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotban lévő példányát.</span><span class="sxs-lookup"><span data-stu-id="26db0-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26db0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26db0-104">SYNTAX</span></span>

### <span data-ttu-id="26db0-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="26db0-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="26db0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26db0-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="26db0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26db0-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="26db0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="26db0-108">DESCRIPTION</span></span>
<span data-ttu-id="26db0-109">Az Stop-AzureRmDataMigrationService parancsmag leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy futó állapotú példányát.</span><span class="sxs-lookup"><span data-stu-id="26db0-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="26db0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="26db0-110">EXAMPLES</span></span>

### <span data-ttu-id="26db0-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="26db0-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="26db0-112">A fenti példa leállítja az Azure-adatbázis áttelepítési szolgáltatásának az "TestService" nevű példányát, amely bemeneti paraméterként lett átadva a szolgáltatás neve mezőbe.</span><span class="sxs-lookup"><span data-stu-id="26db0-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="26db0-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="26db0-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="26db0-114">A fenti példa leállítja az Azure-adatbázis áttelepítési szolgáltatásának egy példányát, amely a PSDataMigrationService objektum bemeneti paraméterként lett átadva.</span><span class="sxs-lookup"><span data-stu-id="26db0-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="26db0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26db0-115">PARAMETERS</span></span>

### <span data-ttu-id="26db0-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26db0-116">-Confirm</span></span>
<span data-ttu-id="26db0-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26db0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26db0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26db0-118">-DefaultProfile</span></span>
<span data-ttu-id="26db0-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26db0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26db0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26db0-120">-InputObject</span></span>
<span data-ttu-id="26db0-121">PSDataMigrationService objektum</span><span class="sxs-lookup"><span data-stu-id="26db0-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="26db0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26db0-122">-Name</span></span>
<span data-ttu-id="26db0-123">Az adatáttelepítési szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="26db0-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="26db0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26db0-124">-PassThru</span></span>
<span data-ttu-id="26db0-125">Igaz/hamis értéket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="26db0-125">Returns an true/false.</span></span>
<span data-ttu-id="26db0-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="26db0-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26db0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26db0-127">-ResourceGroupName</span></span>
<span data-ttu-id="26db0-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="26db0-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="26db0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26db0-129">-ResourceId</span></span>
<span data-ttu-id="26db0-130">DataMigrationService erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="26db0-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="26db0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26db0-131">-WhatIf</span></span>
<span data-ttu-id="26db0-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26db0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26db0-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26db0-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="26db0-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26db0-134">INPUTS</span></span>

### <span data-ttu-id="26db0-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="26db0-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="26db0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="26db0-136">System.String</span></span>


## <span data-ttu-id="26db0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26db0-137">OUTPUTS</span></span>

### <span data-ttu-id="26db0-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26db0-138">System.Boolean</span></span>


## <span data-ttu-id="26db0-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26db0-139">NOTES</span></span>

## <span data-ttu-id="26db0-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26db0-140">RELATED LINKS</span></span>

