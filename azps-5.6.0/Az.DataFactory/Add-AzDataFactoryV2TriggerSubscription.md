---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c74eb60e698cff0d95a4361235c9282f1405dce0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939618"
---
# <span data-ttu-id="7de1f-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="7de1f-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="7de1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7de1f-102">SYNOPSIS</span></span>
<span data-ttu-id="7de1f-103">Előfizeti az eseményindítót a külső szolgáltatás eseményeire.</span><span class="sxs-lookup"><span data-stu-id="7de1f-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="7de1f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7de1f-104">SYNTAX</span></span>

### <span data-ttu-id="7de1f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7de1f-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7de1f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7de1f-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de1f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7de1f-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de1f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7de1f-108">DESCRIPTION</span></span>
<span data-ttu-id="7de1f-109">Ez a parancs előfizeti az eseményindítót a megadott külső szolgáltatáseseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="7de1f-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="7de1f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7de1f-110">EXAMPLES</span></span>

### <span data-ttu-id="7de1f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7de1f-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="7de1f-112">Ez a parancs előfizeti a BlobEnetTrigger1 eseményindítót a megadott eseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="7de1f-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="7de1f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7de1f-113">PARAMETERS</span></span>

### <span data-ttu-id="7de1f-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7de1f-114">-DataFactoryName</span></span>
<span data-ttu-id="7de1f-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="7de1f-115">The data factory name.</span></span>

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

### <span data-ttu-id="7de1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de1f-116">-DefaultProfile</span></span>
<span data-ttu-id="7de1f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7de1f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7de1f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7de1f-118">-InputObject</span></span>
<span data-ttu-id="7de1f-119">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="7de1f-119">The trigger object.</span></span>

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

### <span data-ttu-id="7de1f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7de1f-120">-Name</span></span>
<span data-ttu-id="7de1f-121">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="7de1f-121">The trigger name.</span></span>

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

### <span data-ttu-id="7de1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="7de1f-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7de1f-123">The resource group name.</span></span>

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

### <span data-ttu-id="7de1f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7de1f-124">-ResourceId</span></span>
<span data-ttu-id="7de1f-125">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="7de1f-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7de1f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7de1f-126">-Confirm</span></span>
<span data-ttu-id="7de1f-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7de1f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de1f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de1f-128">-WhatIf</span></span>
<span data-ttu-id="7de1f-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7de1f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de1f-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7de1f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de1f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de1f-131">CommonParameters</span></span>
<span data-ttu-id="7de1f-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de1f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de1f-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de1f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de1f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7de1f-134">INPUTS</span></span>

### <span data-ttu-id="7de1f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7de1f-135">System.String</span></span>
<span data-ttu-id="7de1f-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7de1f-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="7de1f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7de1f-137">OUTPUTS</span></span>

### <span data-ttu-id="7de1f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7de1f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="7de1f-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7de1f-139">NOTES</span></span>

## <span data-ttu-id="7de1f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7de1f-140">RELATED LINKS</span></span>

