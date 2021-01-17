---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 989a898605488fc7cfaa828bfd8c5b9b61378a27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338706"
---
# <span data-ttu-id="80eb7-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80eb7-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="80eb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="80eb7-103">Információkat kap az adatüzemben található eseményindítókról.</span><span class="sxs-lookup"><span data-stu-id="80eb7-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="80eb7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80eb7-104">SYNTAX</span></span>

### <span data-ttu-id="80eb7-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80eb7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80eb7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="80eb7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80eb7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="80eb7-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80eb7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80eb7-108">DESCRIPTION</span></span>
<span data-ttu-id="80eb7-109">A **Get-AzDataFactoryV2Trigger** parancsmag információkat kap az adatüzemű eseményindítókról.</span><span class="sxs-lookup"><span data-stu-id="80eb7-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="80eb7-110">Ha megadja egy eseményindító nevét, a parancsmag információt kap az eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="80eb7-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="80eb7-111">Ha nem ad meg nevet, a parancsmag információt kap az adatüzemben található összes eseményindítóról.</span><span class="sxs-lookup"><span data-stu-id="80eb7-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="80eb7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80eb7-112">EXAMPLES</span></span>

### <span data-ttu-id="80eb7-113">1. példa: Információ lekérte egy adott eseményindítóról</span><span class="sxs-lookup"><span data-stu-id="80eb7-113">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="80eb7-114">A "WikiADF" adatüzemben létrehozott összes eseményindító listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="80eb7-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="80eb7-115">2. példa: Információ az összes eseményindítóról</span><span class="sxs-lookup"><span data-stu-id="80eb7-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="80eb7-116">Egyetlen "ScheduledTrigger" eseményindítót kap a "WikiADF" adat factoryban.</span><span class="sxs-lookup"><span data-stu-id="80eb7-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="80eb7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80eb7-117">PARAMETERS</span></span>

### <span data-ttu-id="80eb7-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="80eb7-118">-DataFactory</span></span>
<span data-ttu-id="80eb7-119">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="80eb7-119">The data factory object.</span></span>

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

### <span data-ttu-id="80eb7-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="80eb7-120">-DataFactoryName</span></span>
<span data-ttu-id="80eb7-121">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="80eb7-121">The data factory name.</span></span>

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

### <span data-ttu-id="80eb7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80eb7-122">-DefaultProfile</span></span>
<span data-ttu-id="80eb7-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80eb7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80eb7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="80eb7-124">-Name</span></span>
<span data-ttu-id="80eb7-125">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="80eb7-125">The trigger name.</span></span>

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

### <span data-ttu-id="80eb7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80eb7-126">-ResourceGroupName</span></span>
<span data-ttu-id="80eb7-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="80eb7-127">The resource group name.</span></span>

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

### <span data-ttu-id="80eb7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80eb7-128">-ResourceId</span></span>
<span data-ttu-id="80eb7-129">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="80eb7-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="80eb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80eb7-130">CommonParameters</span></span>
<span data-ttu-id="80eb7-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80eb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80eb7-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80eb7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80eb7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80eb7-133">INPUTS</span></span>

### <span data-ttu-id="80eb7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="80eb7-134">System.String</span></span>

### <span data-ttu-id="80eb7-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="80eb7-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="80eb7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80eb7-136">OUTPUTS</span></span>

### <span data-ttu-id="80eb7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="80eb7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="80eb7-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80eb7-138">NOTES</span></span>

## <span data-ttu-id="80eb7-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80eb7-139">RELATED LINKS</span></span>

[<span data-ttu-id="80eb7-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80eb7-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="80eb7-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80eb7-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="80eb7-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80eb7-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="80eb7-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80eb7-143">Remove-AzDataFactoryV2Trigger</span></span>]()
