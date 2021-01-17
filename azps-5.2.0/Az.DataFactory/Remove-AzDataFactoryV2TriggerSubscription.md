---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365719"
---
# <span data-ttu-id="03174-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="03174-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="03174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03174-102">SYNOPSIS</span></span>
<span data-ttu-id="03174-103">Leiratkozhat az eseményindítóról a külső szolgáltatásesemények számára.</span><span class="sxs-lookup"><span data-stu-id="03174-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="03174-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03174-104">SYNTAX</span></span>

### <span data-ttu-id="03174-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03174-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03174-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03174-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03174-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03174-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03174-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03174-108">DESCRIPTION</span></span>
<span data-ttu-id="03174-109">Ez a parancs leiratkozik az eseményindítóról a megadott külső szolgáltatásesemények számára az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="03174-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="03174-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03174-110">EXAMPLES</span></span>

### <span data-ttu-id="03174-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="03174-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="03174-112">Ez a parancs leiratkozik a BlobEnetTrigger1 eseményindítóról a megadott eseményre az eseményindító definiálásból.</span><span class="sxs-lookup"><span data-stu-id="03174-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="03174-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03174-113">PARAMETERS</span></span>

### <span data-ttu-id="03174-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="03174-114">-DataFactoryName</span></span>
<span data-ttu-id="03174-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="03174-115">The data factory name.</span></span>

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

### <span data-ttu-id="03174-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03174-116">-DefaultProfile</span></span>
<span data-ttu-id="03174-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03174-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03174-118">-Force</span><span class="sxs-lookup"><span data-stu-id="03174-118">-Force</span></span>
<span data-ttu-id="03174-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03174-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="03174-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03174-120">-InputObject</span></span>
<span data-ttu-id="03174-121">Az eseményindító objektum.</span><span class="sxs-lookup"><span data-stu-id="03174-121">The trigger object.</span></span>

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

### <span data-ttu-id="03174-122">-Name</span><span class="sxs-lookup"><span data-stu-id="03174-122">-Name</span></span>
<span data-ttu-id="03174-123">Az eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="03174-123">The trigger name.</span></span>

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

### <span data-ttu-id="03174-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03174-124">-PassThru</span></span>
<span data-ttu-id="03174-125">Ha meg van adva, a parancsmag a sikeres törlés esetén a true értéket adja vissza.</span><span class="sxs-lookup"><span data-stu-id="03174-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="03174-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03174-126">-ResourceGroupName</span></span>
<span data-ttu-id="03174-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03174-127">The resource group name.</span></span>

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

### <span data-ttu-id="03174-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03174-128">-ResourceId</span></span>
<span data-ttu-id="03174-129">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="03174-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="03174-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03174-130">-Confirm</span></span>
<span data-ttu-id="03174-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03174-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03174-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03174-132">-WhatIf</span></span>
<span data-ttu-id="03174-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03174-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03174-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03174-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03174-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03174-135">CommonParameters</span></span>
<span data-ttu-id="03174-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03174-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03174-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03174-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03174-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03174-138">INPUTS</span></span>

### <span data-ttu-id="03174-139">System.String</span><span class="sxs-lookup"><span data-stu-id="03174-139">System.String</span></span>
<span data-ttu-id="03174-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="03174-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="03174-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03174-141">OUTPUTS</span></span>

### <span data-ttu-id="03174-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="03174-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="03174-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03174-143">NOTES</span></span>

## <span data-ttu-id="03174-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03174-144">RELATED LINKS</span></span>

