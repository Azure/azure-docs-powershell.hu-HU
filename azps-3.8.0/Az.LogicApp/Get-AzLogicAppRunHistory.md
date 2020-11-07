---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 2d9425f21845123c003568204675b0d56a8bcd02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845969"
---
# <span data-ttu-id="ace65-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="ace65-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="ace65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ace65-102">SYNOPSIS</span></span>
<span data-ttu-id="ace65-103">Egy logikai alkalmazás futtatási előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="ace65-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="ace65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ace65-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace65-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ace65-105">DESCRIPTION</span></span>
<span data-ttu-id="ace65-106">A **Get-AzLogicAppRunHistory** parancsmag a logikai alkalmazások futási előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="ace65-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="ace65-107">Ez a parancsmag a **WorkflowRun** -objektumok gyűjteményét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="ace65-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="ace65-108">Adja meg a logikai alkalmazást és az erőforrás csoportot.</span><span class="sxs-lookup"><span data-stu-id="ace65-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="ace65-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="ace65-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ace65-110">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="ace65-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ace65-111">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="ace65-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ace65-112">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="ace65-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ace65-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ace65-113">EXAMPLES</span></span>

### <span data-ttu-id="ace65-114">Példa 1: egy logikai app futtatási előzményeinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="ace65-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="ace65-115">Ez a parancs a LogicApp03 nevű logikai app futtatási előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ace65-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="ace65-116">2. példa: a logikai alkalmazások futtatásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="ace65-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="ace65-117">Ez a parancs a LogicApp03 nevű logikai alkalmazáshoz egy adott logikai app futtatását kapja.</span><span class="sxs-lookup"><span data-stu-id="ace65-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="ace65-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ace65-118">PARAMETERS</span></span>

### <span data-ttu-id="ace65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace65-119">-DefaultProfile</span></span>
<span data-ttu-id="ace65-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ace65-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ace65-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ace65-121">-Name</span></span>
<span data-ttu-id="ace65-122">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez ez a parancsmag futtatja az előzményeket.</span><span class="sxs-lookup"><span data-stu-id="ace65-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="ace65-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace65-123">-ResourceGroupName</span></span>
<span data-ttu-id="ace65-124">A logikai alkalmazást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ace65-124">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="ace65-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="ace65-125">-RunName</span></span>
<span data-ttu-id="ace65-126">Egy logikai alkalmazás futtatási nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ace65-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="ace65-127">Ez a parancsmag a munkafolyamatot futtatja, hogy ez a parancsmag határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ace65-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="ace65-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace65-128">CommonParameters</span></span>
<span data-ttu-id="ace65-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ace65-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace65-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace65-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace65-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ace65-131">INPUTS</span></span>

### <span data-ttu-id="ace65-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ace65-132">System.String</span></span>

## <span data-ttu-id="ace65-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ace65-133">OUTPUTS</span></span>

### <span data-ttu-id="ace65-134">Microsoft. Azure. Management. Logic. models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="ace65-134">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="ace65-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ace65-135">NOTES</span></span>

## <span data-ttu-id="ace65-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ace65-136">RELATED LINKS</span></span>

[<span data-ttu-id="ace65-137">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="ace65-137">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="ace65-138">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ace65-138">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="ace65-139">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="ace65-139">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


