---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 175667480977e55cc93486f252a8f84080c64b5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147602"
---
# <span data-ttu-id="7f2d0-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="7f2d0-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="7f2d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f2d0-102">SYNOPSIS</span></span>

<span data-ttu-id="7f2d0-103">Egy logikai appból futtat egy műveletet.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="7f2d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f2d0-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f2d0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f2d0-105">DESCRIPTION</span></span>

<span data-ttu-id="7f2d0-106">A **Get-Az LogicAppRunAction parancsmag** egy logikai app futtatásával kapja meg a műveletet.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="7f2d0-107">Ez a parancsmag **egy WorkflowRunAction objektumot ad** vissza.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="7f2d0-108">Adja meg a logikai alkalmazást, az erőforráscsoportot, és futtassa.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="7f2d0-109">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7f2d0-110">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7f2d0-111">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7f2d0-112">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7f2d0-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f2d0-113">EXAMPLES</span></span>

### <span data-ttu-id="7f2d0-114">1. példa: Művelet lekérte egy logic app futtatásával</span><span class="sxs-lookup"><span data-stu-id="7f2d0-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
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

<span data-ttu-id="7f2d0-115">Ez a parancs a 0858592518423369718380498702CU26 azonosítóval futtatott logic appból kap egy adott Logic App-műveletet.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="7f2d0-116">2. példa: Az összes művelet lekérte a Logic App futtatását</span><span class="sxs-lookup"><span data-stu-id="7f2d0-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="7f2d0-117">Ez a parancs a LogicApp05 nevű logikai app 08585925184423369718380498702CU26 azonosítóját futtatva kapja meg az összes logikai alkalmazásműveletet.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="7f2d0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f2d0-118">PARAMETERS</span></span>

### <span data-ttu-id="7f2d0-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="7f2d0-119">-ActionName</span></span>

<span data-ttu-id="7f2d0-120">Egy logikai appban futtatott művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="7f2d0-121">Ez a parancsmag a paraméter által megadott műveletet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f2d0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2d0-122">-DefaultProfile</span></span>

<span data-ttu-id="7f2d0-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f2d0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f2d0-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="7f2d0-124">-FollowNextPageLink</span></span>

<span data-ttu-id="7f2d0-125">Azt jelzi, hogy a parancsmagnak a következő laphivatkozásokat kell követnie.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="7f2d0-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="7f2d0-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="7f2d0-127">Azt adja meg, hogy a FollowNextPageLink használata esetén hányszor kell követni a következő laphivatkozásokat.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="7f2d0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7f2d0-128">-Name</span></span>

<span data-ttu-id="7f2d0-129">Annak a logikai alkalmazásnak a nevét adja meg, amelyhez a parancsmag műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="7f2d0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f2d0-130">-ResourceGroupName</span></span>

<span data-ttu-id="7f2d0-131">Annak az erőforráscsoportnak a nevét adja meg, amelyben a parancsmag műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="7f2d0-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="7f2d0-132">-RunName</span></span>

<span data-ttu-id="7f2d0-133">Logikai alkalmazás futtatásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="7f2d0-134">Ez a parancsmag egy műveletet kap a paraméter által megadott futtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f2d0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2d0-135">CommonParameters</span></span>

<span data-ttu-id="7f2d0-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2d0-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f2d0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2d0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f2d0-138">INPUTS</span></span>

### <span data-ttu-id="7f2d0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7f2d0-139">System.String</span></span>

## <span data-ttu-id="7f2d0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f2d0-140">OUTPUTS</span></span>

### <span data-ttu-id="7f2d0-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="7f2d0-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="7f2d0-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f2d0-142">NOTES</span></span>

## <span data-ttu-id="7f2d0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f2d0-143">RELATED LINKS</span></span>

[<span data-ttu-id="7f2d0-144">Get-AzRunAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="7f2d0-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="7f2d0-145">Stop-AzRunAppRun</span><span class="sxs-lookup"><span data-stu-id="7f2d0-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
