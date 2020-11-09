---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298301"
---
# <span data-ttu-id="82ad4-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="82ad4-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="82ad4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="82ad4-103">Lemondhatja az eseményindítót külső szolgáltatási eseményekre.</span><span class="sxs-lookup"><span data-stu-id="82ad4-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="82ad4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82ad4-104">SYNTAX</span></span>

### <span data-ttu-id="82ad4-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82ad4-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82ad4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="82ad4-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ad4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="82ad4-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ad4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="82ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="82ad4-109">Ez a parancs lemondja, hogy az eseményindító Defintion a megadott külső szolgáltatási eseményekre az eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="82ad4-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="82ad4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="82ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="82ad4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="82ad4-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="82ad4-112">Ez a parancs lemondja a BlobEnetTrigger1 triggert az indító Defintion megadott eseményekre.</span><span class="sxs-lookup"><span data-stu-id="82ad4-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="82ad4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82ad4-113">PARAMETERS</span></span>

### <span data-ttu-id="82ad4-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="82ad4-114">-DataFactoryName</span></span>
<span data-ttu-id="82ad4-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="82ad4-115">The data factory name.</span></span>

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

### <span data-ttu-id="82ad4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ad4-116">-DefaultProfile</span></span>
<span data-ttu-id="82ad4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82ad4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82ad4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="82ad4-118">-Force</span></span>
<span data-ttu-id="82ad4-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82ad4-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="82ad4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82ad4-120">-InputObject</span></span>
<span data-ttu-id="82ad4-121">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="82ad4-121">The trigger object.</span></span>

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

### <span data-ttu-id="82ad4-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82ad4-122">-Name</span></span>
<span data-ttu-id="82ad4-123">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="82ad4-123">The trigger name.</span></span>

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

### <span data-ttu-id="82ad4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82ad4-124">-PassThru</span></span>
<span data-ttu-id="82ad4-125">Ha meg van adva, a parancsmag visszatérési értéke sikeres lesz a sikeres törléshez.</span><span class="sxs-lookup"><span data-stu-id="82ad4-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="82ad4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ad4-126">-ResourceGroupName</span></span>
<span data-ttu-id="82ad4-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="82ad4-127">The resource group name.</span></span>

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

### <span data-ttu-id="82ad4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82ad4-128">-ResourceId</span></span>
<span data-ttu-id="82ad4-129">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="82ad4-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="82ad4-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="82ad4-130">-Confirm</span></span>
<span data-ttu-id="82ad4-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82ad4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ad4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ad4-132">-WhatIf</span></span>
<span data-ttu-id="82ad4-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="82ad4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ad4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82ad4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ad4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ad4-135">CommonParameters</span></span>
<span data-ttu-id="82ad4-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82ad4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ad4-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ad4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ad4-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ad4-138">INPUTS</span></span>

### <span data-ttu-id="82ad4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="82ad4-139">System.String</span></span>
<span data-ttu-id="82ad4-140">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="82ad4-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="82ad4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ad4-141">OUTPUTS</span></span>

### <span data-ttu-id="82ad4-142">Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="82ad4-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="82ad4-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82ad4-143">NOTES</span></span>

## <span data-ttu-id="82ad4-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82ad4-144">RELATED LINKS</span></span>

