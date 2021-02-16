---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208710"
---
# <span data-ttu-id="082c6-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="082c6-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="082c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="082c6-102">SYNOPSIS</span></span>
<span data-ttu-id="082c6-103">Leiratkozhat az eseményindítóról a külső szolgáltatás eseményeiről.</span><span class="sxs-lookup"><span data-stu-id="082c6-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="082c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="082c6-104">SYNTAX</span></span>

### <span data-ttu-id="082c6-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="082c6-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="082c6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="082c6-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="082c6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="082c6-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="082c6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="082c6-108">DESCRIPTION</span></span>
<span data-ttu-id="082c6-109">Ez a parancs leiratkozik az eseményindítóról a megadott külső szolgáltatásesemények számára az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="082c6-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="082c6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="082c6-110">EXAMPLES</span></span>

### <span data-ttu-id="082c6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="082c6-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="082c6-112">Ez a parancs leiratkozik a BlobEnetTrigger1 eseményindítóról a megadott eseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="082c6-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="082c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="082c6-113">PARAMETERS</span></span>

### <span data-ttu-id="082c6-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="082c6-114">-DataFactoryName</span></span>
<span data-ttu-id="082c6-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="082c6-115">The data factory name.</span></span>

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

### <span data-ttu-id="082c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082c6-116">-DefaultProfile</span></span>
<span data-ttu-id="082c6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="082c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="082c6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="082c6-118">-Force</span></span>
<span data-ttu-id="082c6-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="082c6-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="082c6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="082c6-120">-InputObject</span></span>
<span data-ttu-id="082c6-121">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="082c6-121">The trigger object.</span></span>

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

### <span data-ttu-id="082c6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="082c6-122">-Name</span></span>
<span data-ttu-id="082c6-123">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="082c6-123">The trigger name.</span></span>

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

### <span data-ttu-id="082c6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="082c6-124">-PassThru</span></span>
<span data-ttu-id="082c6-125">Ha meg van adva, a parancsmag a sikeres törlés esetén a true értéket adja vissza.</span><span class="sxs-lookup"><span data-stu-id="082c6-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="082c6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="082c6-126">-ResourceGroupName</span></span>
<span data-ttu-id="082c6-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="082c6-127">The resource group name.</span></span>

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

### <span data-ttu-id="082c6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="082c6-128">-ResourceId</span></span>
<span data-ttu-id="082c6-129">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="082c6-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="082c6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="082c6-130">-Confirm</span></span>
<span data-ttu-id="082c6-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="082c6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="082c6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="082c6-132">-WhatIf</span></span>
<span data-ttu-id="082c6-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="082c6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="082c6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="082c6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="082c6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082c6-135">CommonParameters</span></span>
<span data-ttu-id="082c6-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="082c6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082c6-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="082c6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082c6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="082c6-138">INPUTS</span></span>

### <span data-ttu-id="082c6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="082c6-139">System.String</span></span>
<span data-ttu-id="082c6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="082c6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="082c6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="082c6-141">OUTPUTS</span></span>

### <span data-ttu-id="082c6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="082c6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="082c6-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="082c6-143">NOTES</span></span>

## <span data-ttu-id="082c6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="082c6-144">RELATED LINKS</span></span>

