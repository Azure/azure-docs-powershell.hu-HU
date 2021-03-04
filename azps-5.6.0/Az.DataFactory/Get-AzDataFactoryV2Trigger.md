---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 5940d362b3c06ede714568daa2ecce8bd829581d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930178"
---
# <span data-ttu-id="7fcf9-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7fcf9-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="7fcf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcf9-103">Információkat kap az adatüzemben található eseményindítókról.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="7fcf9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fcf9-104">SYNTAX</span></span>

### <span data-ttu-id="7fcf9-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7fcf9-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fcf9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7fcf9-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fcf9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7fcf9-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fcf9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fcf9-108">DESCRIPTION</span></span>
<span data-ttu-id="7fcf9-109">A **Get-AzDataFactoryV2Trigger** parancsmag információkat kap az adatüzemű eseményindítókról.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="7fcf9-110">Ha megadja egy eseményindító nevét, a parancsmag információt kap az eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="7fcf9-111">Ha nem ad meg nevet, a parancsmag információt kap az adatüzemben található összes eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="7fcf9-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fcf9-112">EXAMPLES</span></span>

### <span data-ttu-id="7fcf9-113">1. példa: Információ az összes eseményindítóról</span><span class="sxs-lookup"><span data-stu-id="7fcf9-113">Example 1: Get information about all triggers</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="7fcf9-114">A "WikiADF" adatüzemben létrehozott összes eseményindító listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="7fcf9-115">2. példa: Információ lekérte egy adott eseményindítóról</span><span class="sxs-lookup"><span data-stu-id="7fcf9-115">Example 2: Get information about a specific trigger</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="7fcf9-116">Egyetlen "ScheduledTrigger" eseményindítót kap a "WikiADF" adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="7fcf9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fcf9-117">PARAMETERS</span></span>

### <span data-ttu-id="7fcf9-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7fcf9-118">-DataFactory</span></span>
<span data-ttu-id="7fcf9-119">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcf9-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7fcf9-120">-DataFactoryName</span></span>
<span data-ttu-id="7fcf9-121">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-121">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcf9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcf9-122">-DefaultProfile</span></span>
<span data-ttu-id="7fcf9-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fcf9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7fcf9-124">-Name</span></span>
<span data-ttu-id="7fcf9-125">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcf9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fcf9-126">-ResourceGroupName</span></span>
<span data-ttu-id="7fcf9-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcf9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fcf9-128">-ResourceId</span></span>
<span data-ttu-id="7fcf9-129">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcf9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcf9-130">CommonParameters</span></span>
<span data-ttu-id="7fcf9-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fcf9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcf9-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fcf9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcf9-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fcf9-133">INPUTS</span></span>

### <span data-ttu-id="7fcf9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7fcf9-134">System.String</span></span>

### <span data-ttu-id="7fcf9-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7fcf9-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7fcf9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fcf9-136">OUTPUTS</span></span>

### <span data-ttu-id="7fcf9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7fcf9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="7fcf9-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fcf9-138">NOTES</span></span>

## <span data-ttu-id="7fcf9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fcf9-139">RELATED LINKS</span></span>

[<span data-ttu-id="7fcf9-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7fcf9-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7fcf9-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7fcf9-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7fcf9-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7fcf9-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7fcf9-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7fcf9-143">Remove-AzDataFactoryV2Trigger</span></span>]()
