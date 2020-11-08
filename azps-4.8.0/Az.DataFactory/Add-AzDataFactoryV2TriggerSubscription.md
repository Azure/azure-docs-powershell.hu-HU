---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182848"
---
# <span data-ttu-id="5a075-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="5a075-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="5a075-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a075-102">SYNOPSIS</span></span>
<span data-ttu-id="5a075-103">Iratkozzon fel az eseményindítót külső szolgáltatási eseményekre.</span><span class="sxs-lookup"><span data-stu-id="5a075-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="5a075-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a075-104">SYNTAX</span></span>

### <span data-ttu-id="5a075-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a075-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a075-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a075-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a075-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a075-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a075-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a075-108">DESCRIPTION</span></span>
<span data-ttu-id="5a075-109">Ez a parancs Előfizeti az esemény eseményindítóját a megadott külső szolgáltatási eseményekre az eseményindító Defintion.</span><span class="sxs-lookup"><span data-stu-id="5a075-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="5a075-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5a075-110">EXAMPLES</span></span>

### <span data-ttu-id="5a075-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5a075-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="5a075-112">Ez a parancs Előfizeti a BlobEnetTrigger1 az indító Defintion megadott eseményekre.</span><span class="sxs-lookup"><span data-stu-id="5a075-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="5a075-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a075-113">PARAMETERS</span></span>

### <span data-ttu-id="5a075-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5a075-114">-DataFactoryName</span></span>
<span data-ttu-id="5a075-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="5a075-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a075-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a075-116">-DefaultProfile</span></span>
<span data-ttu-id="5a075-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a075-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a075-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a075-118">-InputObject</span></span>
<span data-ttu-id="5a075-119">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="5a075-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a075-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a075-120">-Name</span></span>
<span data-ttu-id="5a075-121">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="5a075-121">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a075-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a075-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a075-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a075-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a075-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a075-124">-ResourceId</span></span>
<span data-ttu-id="5a075-125">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="5a075-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a075-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5a075-126">-Confirm</span></span>
<span data-ttu-id="5a075-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a075-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a075-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a075-128">-WhatIf</span></span>
<span data-ttu-id="5a075-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5a075-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a075-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a075-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a075-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a075-131">CommonParameters</span></span>
<span data-ttu-id="5a075-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a075-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a075-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a075-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a075-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a075-134">INPUTS</span></span>

### <span data-ttu-id="5a075-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5a075-135">System.String</span></span>
<span data-ttu-id="5a075-136">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5a075-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5a075-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a075-137">OUTPUTS</span></span>

### <span data-ttu-id="5a075-138">Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="5a075-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="5a075-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a075-139">NOTES</span></span>

## <span data-ttu-id="5a075-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a075-140">RELATED LINKS</span></span>

