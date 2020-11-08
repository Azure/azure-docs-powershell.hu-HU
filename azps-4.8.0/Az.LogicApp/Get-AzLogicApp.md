---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: ca0871dae696425c7f19ac1924aa0b725d0dac6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181686"
---
# <span data-ttu-id="9ad37-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ad37-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="9ad37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ad37-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad37-103">Logikai alkalmazást kap egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="9ad37-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="9ad37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ad37-104">SYNTAX</span></span>

### <span data-ttu-id="9ad37-105">ListWorkflows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ad37-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad37-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="9ad37-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad37-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ad37-107">DESCRIPTION</span></span>
<span data-ttu-id="9ad37-108">A **Get-AzLogicApp** parancsmag logikai alkalmazást kap.</span><span class="sxs-lookup"><span data-stu-id="9ad37-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="9ad37-109">Ez a parancsmag egy **munkafolyamat** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="9ad37-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="9ad37-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="9ad37-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9ad37-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="9ad37-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9ad37-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="9ad37-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9ad37-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="9ad37-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9ad37-114">Példák</span><span class="sxs-lookup"><span data-stu-id="9ad37-114">EXAMPLES</span></span>

### <span data-ttu-id="9ad37-115">Példa 1: logikai alkalmazás beszerzése egy erőforrás-csoportból</span><span class="sxs-lookup"><span data-stu-id="9ad37-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="9ad37-116">Ez a parancs egy logikai alkalmazást kap a ResourceGroup11 nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="9ad37-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="9ad37-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ad37-117">PARAMETERS</span></span>

### <span data-ttu-id="9ad37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad37-118">-DefaultProfile</span></span>
<span data-ttu-id="9ad37-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9ad37-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ad37-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ad37-120">-Name</span></span>
<span data-ttu-id="9ad37-121">Annak a logikai alkalmazásnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="9ad37-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad37-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ad37-123">Annak a csoportnak a nevét adja meg, amelyben a parancsmag logikai alkalmazást kap.</span><span class="sxs-lookup"><span data-stu-id="9ad37-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad37-124">-Verzió</span><span class="sxs-lookup"><span data-stu-id="9ad37-124">-Version</span></span>
<span data-ttu-id="9ad37-125">A logikai alkalmazás verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ad37-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad37-126">CommonParameters</span></span>
<span data-ttu-id="9ad37-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ad37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad37-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad37-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad37-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ad37-129">INPUTS</span></span>

### <span data-ttu-id="9ad37-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad37-130">System.String</span></span>

## <span data-ttu-id="9ad37-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ad37-131">OUTPUTS</span></span>

### <span data-ttu-id="9ad37-132">Microsoft. Azure. Management. Logic. models. workflow</span><span class="sxs-lookup"><span data-stu-id="9ad37-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="9ad37-133">Microsoft. Azure. Management. Logic. models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="9ad37-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="9ad37-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ad37-134">NOTES</span></span>

## <span data-ttu-id="9ad37-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ad37-135">RELATED LINKS</span></span>

[<span data-ttu-id="9ad37-136">Új – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ad37-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="9ad37-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ad37-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="9ad37-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ad37-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="9ad37-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ad37-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


