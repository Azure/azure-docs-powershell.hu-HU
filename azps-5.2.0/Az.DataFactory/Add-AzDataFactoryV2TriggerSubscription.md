---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328393"
---
# <span data-ttu-id="8f4f6-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f4f6-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="8f4f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4f6-103">Előfizeti az eseményindítót a külső szolgáltatás eseményeire.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="8f4f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f4f6-104">SYNTAX</span></span>

### <span data-ttu-id="8f4f6-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f4f6-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f4f6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8f4f6-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f4f6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f4f6-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f4f6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f4f6-108">DESCRIPTION</span></span>
<span data-ttu-id="8f4f6-109">Ez a parancs előfizeti az eseményindítót a megadott külső szolgáltatáseseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="8f4f6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f4f6-110">EXAMPLES</span></span>

### <span data-ttu-id="8f4f6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8f4f6-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="8f4f6-112">Ez a parancs előfizeti a BlobEnetTrigger1 eseményindítót a megadott eseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="8f4f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f4f6-113">PARAMETERS</span></span>

### <span data-ttu-id="8f4f6-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8f4f6-114">-DataFactoryName</span></span>
<span data-ttu-id="8f4f6-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-115">The data factory name.</span></span>

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

### <span data-ttu-id="8f4f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4f6-116">-DefaultProfile</span></span>
<span data-ttu-id="8f4f6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f4f6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f4f6-118">-InputObject</span></span>
<span data-ttu-id="8f4f6-119">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-119">The trigger object.</span></span>

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

### <span data-ttu-id="8f4f6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8f4f6-120">-Name</span></span>
<span data-ttu-id="8f4f6-121">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-121">The trigger name.</span></span>

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

### <span data-ttu-id="8f4f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f4f6-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-123">The resource group name.</span></span>

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

### <span data-ttu-id="8f4f6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f4f6-124">-ResourceId</span></span>
<span data-ttu-id="8f4f6-125">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8f4f6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f4f6-126">-Confirm</span></span>
<span data-ttu-id="8f4f6-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f4f6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f4f6-128">-WhatIf</span></span>
<span data-ttu-id="8f4f6-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f4f6-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f4f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4f6-131">CommonParameters</span></span>
<span data-ttu-id="8f4f6-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4f6-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f4f6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4f6-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f4f6-134">INPUTS</span></span>

### <span data-ttu-id="8f4f6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4f6-135">System.String</span></span>
<span data-ttu-id="8f4f6-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8f4f6-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8f4f6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f4f6-137">OUTPUTS</span></span>

### <span data-ttu-id="8f4f6-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8f4f6-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="8f4f6-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f4f6-139">NOTES</span></span>

## <span data-ttu-id="8f4f6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f4f6-140">RELATED LINKS</span></span>

