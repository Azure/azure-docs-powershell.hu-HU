---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: 4aa135adf8db8cc1044eba761b33f570abd0396b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672246"
---
# <span data-ttu-id="46082-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="46082-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="46082-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46082-102">SYNOPSIS</span></span>
<span data-ttu-id="46082-103">Egy logikai app futásának műveletét kapja.</span><span class="sxs-lookup"><span data-stu-id="46082-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46082-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46082-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46082-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46082-105">DESCRIPTION</span></span>
<span data-ttu-id="46082-106">A **Get-AzureRmLogicAppRunAction** parancsmag egy logikai app futtatását követően kapja meg a műveletsort.</span><span class="sxs-lookup"><span data-stu-id="46082-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="46082-107">Ez a parancsmag **WorkflowRunAction** -objektumokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="46082-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="46082-108">Adja meg a logikai alkalmazást, az erőforrás csoportot és a futtatást.</span><span class="sxs-lookup"><span data-stu-id="46082-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="46082-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="46082-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="46082-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="46082-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="46082-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="46082-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="46082-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="46082-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="46082-113">Példák</span><span class="sxs-lookup"><span data-stu-id="46082-113">EXAMPLES</span></span>

### <span data-ttu-id="46082-114">Példa 1: művelet beszerzése logikai alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="46082-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="46082-115">Ez a parancs a LogicApp05 nevű LogicAppRun56 nevű logikai app konkrét logikával kapcsolatos műveletét kapja.</span><span class="sxs-lookup"><span data-stu-id="46082-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="46082-116">2. példa: a logikai alkalmazások által futtatott összes művelet beolvasása</span><span class="sxs-lookup"><span data-stu-id="46082-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="46082-117">Ez a parancs a LogicApp05 nevű logikai app Run nevű LogicAppRun56 minden logikai app-műveletet beolvassa.</span><span class="sxs-lookup"><span data-stu-id="46082-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="46082-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46082-118">PARAMETERS</span></span>

### <span data-ttu-id="46082-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="46082-119">-ActionName</span></span>
<span data-ttu-id="46082-120">Egy logikai alkalmazásban futtatott művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46082-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="46082-121">Ez a parancsmag a paraméter által megadott műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="46082-121">This cmdlet gets the action that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46082-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46082-122">-DefaultProfile</span></span>
<span data-ttu-id="46082-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="46082-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46082-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46082-124">-Name</span></span>
<span data-ttu-id="46082-125">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez ez a parancsmag a műveleteket kapja.</span><span class="sxs-lookup"><span data-stu-id="46082-125">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46082-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46082-126">-ResourceGroupName</span></span>
<span data-ttu-id="46082-127">Annak a csoportnak a nevét adja meg, amelyben ez a parancsmag egy művelethez jut.</span><span class="sxs-lookup"><span data-stu-id="46082-127">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46082-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="46082-128">-RunName</span></span>
<span data-ttu-id="46082-129">A logikai alkalmazás futtatásának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46082-129">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="46082-130">Ez a parancsmag a paraméter által megadott futtatási műveletre ad lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="46082-130">This cmdlet gets an action for the run that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46082-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46082-131">CommonParameters</span></span>
<span data-ttu-id="46082-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46082-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46082-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46082-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46082-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46082-134">INPUTS</span></span>

### <span data-ttu-id="46082-135">System. String</span><span class="sxs-lookup"><span data-stu-id="46082-135">System.String</span></span>

## <span data-ttu-id="46082-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46082-136">OUTPUTS</span></span>

### <span data-ttu-id="46082-137">Microsoft. Azure. Management. Logic. models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="46082-137">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="46082-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46082-138">NOTES</span></span>

## <span data-ttu-id="46082-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46082-139">RELATED LINKS</span></span>

[<span data-ttu-id="46082-140">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="46082-140">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="46082-141">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="46082-141">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


