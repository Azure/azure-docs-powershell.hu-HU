---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: ca0871dae696425c7f19ac1924aa0b725d0dac6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152442"
---
# <span data-ttu-id="d67ce-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d67ce-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="d67ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d67ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d67ce-103">Logikai alkalmazást kap egy erőforráscsoporttól.</span><span class="sxs-lookup"><span data-stu-id="d67ce-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="d67ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d67ce-104">SYNTAX</span></span>

### <span data-ttu-id="d67ce-105">ListWorkflows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d67ce-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d67ce-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="d67ce-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d67ce-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d67ce-107">DESCRIPTION</span></span>
<span data-ttu-id="d67ce-108">A **Get-Az LogicApp** parancsmag kap egy logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d67ce-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="d67ce-109">Ez a parancsmag **munkafolyamat-objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="d67ce-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="d67ce-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d67ce-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d67ce-111">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="d67ce-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d67ce-112">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="d67ce-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d67ce-113">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="d67ce-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d67ce-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d67ce-114">EXAMPLES</span></span>

### <span data-ttu-id="d67ce-115">1. példa: Logikai alkalmazás lekérte egy erőforráscsoportból</span><span class="sxs-lookup"><span data-stu-id="d67ce-115">Example 1: Get a logic app from a resource group</span></span>
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

<span data-ttu-id="d67ce-116">Ez a parancs az ResourceGroup11 nevű erőforráscsoportból kap egy logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d67ce-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d67ce-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d67ce-117">PARAMETERS</span></span>

### <span data-ttu-id="d67ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67ce-118">-DefaultProfile</span></span>
<span data-ttu-id="d67ce-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d67ce-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d67ce-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d67ce-120">-Name</span></span>
<span data-ttu-id="d67ce-121">Annak a logikai alkalmazásnak a neve, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="d67ce-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d67ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="d67ce-123">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag logikai alkalmazást kap.</span><span class="sxs-lookup"><span data-stu-id="d67ce-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="d67ce-124">-Verzió</span><span class="sxs-lookup"><span data-stu-id="d67ce-124">-Version</span></span>
<span data-ttu-id="d67ce-125">Egy logikai alkalmazás verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d67ce-125">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="d67ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67ce-126">CommonParameters</span></span>
<span data-ttu-id="d67ce-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67ce-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d67ce-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67ce-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d67ce-129">INPUTS</span></span>

### <span data-ttu-id="d67ce-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d67ce-130">System.String</span></span>

## <span data-ttu-id="d67ce-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d67ce-131">OUTPUTS</span></span>

### <span data-ttu-id="d67ce-132">Microsoft.Azure.Management.Logic.Models.Workflow</span><span class="sxs-lookup"><span data-stu-id="d67ce-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="d67ce-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="d67ce-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="d67ce-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d67ce-134">NOTES</span></span>

## <span data-ttu-id="d67ce-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d67ce-135">RELATED LINKS</span></span>

[<span data-ttu-id="d67ce-136">New-AzApp</span><span class="sxs-lookup"><span data-stu-id="d67ce-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="d67ce-137">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="d67ce-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="d67ce-138">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="d67ce-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="d67ce-139">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="d67ce-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


