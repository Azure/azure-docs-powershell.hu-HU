---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
ms.openlocfilehash: f8e6204be07b9094b1fb4f2cb4c5cafa2a609f0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504400"
---
# <span data-ttu-id="59dfc-101">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="59dfc-101">Get-AzureRmLogicAppRunHistory</span></span>

## <span data-ttu-id="59dfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="59dfc-103">Egy logikai alkalmazás futtatási előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="59dfc-103">Gets the run history of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59dfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59dfc-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59dfc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="59dfc-106">A **Get-AzureRmLogicAppRunHistory** parancsmag a logikai alkalmazások futási előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="59dfc-106">The **Get-AzureRmLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="59dfc-107">Ez a parancsmag a **WorkflowRun** -objektumok gyűjteményét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="59dfc-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="59dfc-108">Adja meg a logikai alkalmazást és az erőforrás csoportot.</span><span class="sxs-lookup"><span data-stu-id="59dfc-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="59dfc-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="59dfc-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="59dfc-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="59dfc-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="59dfc-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="59dfc-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="59dfc-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="59dfc-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="59dfc-113">Példák</span><span class="sxs-lookup"><span data-stu-id="59dfc-113">EXAMPLES</span></span>

### <span data-ttu-id="59dfc-114">Példa 1: egy logikai app futtatási előzményeinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="59dfc-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="59dfc-115">Ez a parancs a LogicApp03 nevű logikai app futtatási előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59dfc-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="59dfc-116">2. példa: a logikai alkalmazások futtatásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="59dfc-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="59dfc-117">Ez a parancs a LogicApp03 nevű logikai alkalmazáshoz egy adott logikai app futtatását kapja.</span><span class="sxs-lookup"><span data-stu-id="59dfc-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="59dfc-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59dfc-118">PARAMETERS</span></span>

### <span data-ttu-id="59dfc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59dfc-119">-DefaultProfile</span></span>
<span data-ttu-id="59dfc-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="59dfc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59dfc-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59dfc-121">-Name</span></span>
<span data-ttu-id="59dfc-122">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez ez a parancsmag futtatja az előzményeket.</span><span class="sxs-lookup"><span data-stu-id="59dfc-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59dfc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59dfc-123">-ResourceGroupName</span></span>
<span data-ttu-id="59dfc-124">A logikai alkalmazást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59dfc-124">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="59dfc-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="59dfc-125">-RunName</span></span>
<span data-ttu-id="59dfc-126">Egy logikai alkalmazás futtatási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59dfc-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="59dfc-127">Ez a parancsmag a munkafolyamatot futtatja, hogy ez a parancsmag határozza meg.</span><span class="sxs-lookup"><span data-stu-id="59dfc-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59dfc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59dfc-128">CommonParameters</span></span>
<span data-ttu-id="59dfc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59dfc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59dfc-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59dfc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59dfc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59dfc-131">INPUTS</span></span>

### <span data-ttu-id="59dfc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="59dfc-132">System.String</span></span>

## <span data-ttu-id="59dfc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59dfc-133">OUTPUTS</span></span>

### <span data-ttu-id="59dfc-134">Microsoft. Azure. Management. Logic. models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="59dfc-134">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="59dfc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59dfc-135">NOTES</span></span>

## <span data-ttu-id="59dfc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59dfc-136">RELATED LINKS</span></span>

[<span data-ttu-id="59dfc-137">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="59dfc-137">Get-AzureRmLogicAppRunAction</span></span>](./Get-AzureRmLogicAppRunAction.md)

[<span data-ttu-id="59dfc-138">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="59dfc-138">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

[<span data-ttu-id="59dfc-139">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="59dfc-139">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


