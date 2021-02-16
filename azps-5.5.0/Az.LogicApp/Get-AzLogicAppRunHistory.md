---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 855cab84e4ab9de2cd7afae2a25dbc867a192e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154851"
---
# <span data-ttu-id="78ddd-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="78ddd-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="78ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78ddd-102">SYNOPSIS</span></span>

<span data-ttu-id="78ddd-103">Egy logikai alkalmazás futtatásának előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="78ddd-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="78ddd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78ddd-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78ddd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78ddd-105">DESCRIPTION</span></span>

<span data-ttu-id="78ddd-106">A **Get-AzRunHistory parancsmag** egy logikai alkalmazás futtatásának előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="78ddd-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="78ddd-107">Ez a parancsmag **WorkflowRun-objektumok gyűjteményét adja** vissza.</span><span class="sxs-lookup"><span data-stu-id="78ddd-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="78ddd-108">Adja meg a logikai alkalmazást és az erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="78ddd-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="78ddd-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="78ddd-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="78ddd-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="78ddd-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="78ddd-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="78ddd-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="78ddd-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="78ddd-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="78ddd-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78ddd-113">EXAMPLES</span></span>

### <span data-ttu-id="78ddd-114">1. példa: Logikai alkalmazás futtatásának előzményeinek lekérte</span><span class="sxs-lookup"><span data-stu-id="78ddd-114">Example 1: Get the run history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="78ddd-115">Ez a parancs a LogicApp03 nevű logikai app futtatásának előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="78ddd-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="78ddd-116">2. példa: Logikai alkalmazás futtatása</span><span class="sxs-lookup"><span data-stu-id="78ddd-116">Example 2: Get a logic app run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="78ddd-117">Ez a parancs egy logic appot futtat a LogicApp03 nevű logikai appban.</span><span class="sxs-lookup"><span data-stu-id="78ddd-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="78ddd-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="78ddd-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="78ddd-119">Ez a parancs a LogicApp03 nevű logikai app teljes futtatáselőzményét lekérte a NextPageLink parancs futtatásával.</span><span class="sxs-lookup"><span data-stu-id="78ddd-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="78ddd-120">4. példa</span><span class="sxs-lookup"><span data-stu-id="78ddd-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="78ddd-121">Ez a parancs a LogicApp03 nevű logikai app futtatásának első két lapját kapja meg a NextPageLink parancs futtatásával, és az eredmény méretét két oldalra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="78ddd-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="78ddd-122">Minden lap 30 találatot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="78ddd-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="78ddd-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78ddd-123">PARAMETERS</span></span>

### <span data-ttu-id="78ddd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ddd-124">-DefaultProfile</span></span>

<span data-ttu-id="78ddd-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="78ddd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78ddd-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="78ddd-126">-FollowNextPageLink</span></span>

<span data-ttu-id="78ddd-127">Azt jelzi, hogy a parancsmagnak a következő laphivatkozásokat kell követnie.</span><span class="sxs-lookup"><span data-stu-id="78ddd-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78ddd-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="78ddd-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="78ddd-129">Azt adja meg, hogy a FollowNextPageLink használata esetén hányszor kell követni a következő laphivatkozásokat.</span><span class="sxs-lookup"><span data-stu-id="78ddd-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78ddd-130">-Name</span><span class="sxs-lookup"><span data-stu-id="78ddd-130">-Name</span></span>

<span data-ttu-id="78ddd-131">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez ez a parancsmag futtatja az előzményeket.</span><span class="sxs-lookup"><span data-stu-id="78ddd-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="78ddd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ddd-132">-ResourceGroupName</span></span>

<span data-ttu-id="78ddd-133">A logikai alkalmazást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78ddd-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="78ddd-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="78ddd-134">-RunName</span></span>

<span data-ttu-id="78ddd-135">Egy logikai alkalmazás futtatásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78ddd-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="78ddd-136">Ez a parancsmag a parancsmag által megadott munkafolyamatot futtatja.</span><span class="sxs-lookup"><span data-stu-id="78ddd-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="78ddd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ddd-137">CommonParameters</span></span>

<span data-ttu-id="78ddd-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ddd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ddd-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78ddd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ddd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78ddd-140">INPUTS</span></span>

### <span data-ttu-id="78ddd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="78ddd-141">System.String</span></span>

## <span data-ttu-id="78ddd-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78ddd-142">OUTPUTS</span></span>

### <span data-ttu-id="78ddd-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="78ddd-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="78ddd-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78ddd-144">NOTES</span></span>

## <span data-ttu-id="78ddd-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78ddd-145">RELATED LINKS</span></span>

[<span data-ttu-id="78ddd-146">Get-AzRunRunAction</span><span class="sxs-lookup"><span data-stu-id="78ddd-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="78ddd-147">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="78ddd-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="78ddd-148">Stop-AzRunAppRun</span><span class="sxs-lookup"><span data-stu-id="78ddd-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
