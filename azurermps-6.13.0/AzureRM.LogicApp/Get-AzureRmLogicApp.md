---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 740ef9b21a2e2caa839880ff2c5e9dadc042351a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503616"
---
# <span data-ttu-id="dcee8-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dcee8-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="dcee8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dcee8-102">SYNOPSIS</span></span>
<span data-ttu-id="dcee8-103">Logikai alkalmazást kap egy erőforrás-csoportból.</span><span class="sxs-lookup"><span data-stu-id="dcee8-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcee8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dcee8-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcee8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dcee8-105">DESCRIPTION</span></span>
<span data-ttu-id="dcee8-106">A **Get-AzureRmLogicApp** parancsmag logikai alkalmazást kap.</span><span class="sxs-lookup"><span data-stu-id="dcee8-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="dcee8-107">Ez a parancsmag egy **munkafolyamat** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dcee8-107">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="dcee8-108">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="dcee8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dcee8-109">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="dcee8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dcee8-110">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="dcee8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dcee8-111">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="dcee8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dcee8-112">Példák</span><span class="sxs-lookup"><span data-stu-id="dcee8-112">EXAMPLES</span></span>

### <span data-ttu-id="dcee8-113">Példa 1: logikai alkalmazás beszerzése egy erőforrás-csoportból</span><span class="sxs-lookup"><span data-stu-id="dcee8-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="dcee8-114">Ez a parancs egy logikai alkalmazást kap a ResourceGroup11 nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="dcee8-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="dcee8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dcee8-115">PARAMETERS</span></span>

### <span data-ttu-id="dcee8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcee8-116">-DefaultProfile</span></span>
<span data-ttu-id="dcee8-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dcee8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcee8-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dcee8-118">-Name</span></span>
<span data-ttu-id="dcee8-119">Annak a logikai alkalmazásnak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="dcee8-119">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dcee8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcee8-120">-ResourceGroupName</span></span>
<span data-ttu-id="dcee8-121">Annak a csoportnak a nevét adja meg, amelyben a parancsmag logikai alkalmazást kap.</span><span class="sxs-lookup"><span data-stu-id="dcee8-121">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="dcee8-122">-Verzió</span><span class="sxs-lookup"><span data-stu-id="dcee8-122">-Version</span></span>
<span data-ttu-id="dcee8-123">A logikai alkalmazás verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dcee8-123">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="dcee8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcee8-124">CommonParameters</span></span>
<span data-ttu-id="dcee8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dcee8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcee8-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcee8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcee8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcee8-127">INPUTS</span></span>

### <span data-ttu-id="dcee8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dcee8-128">System.String</span></span>

## <span data-ttu-id="dcee8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcee8-129">OUTPUTS</span></span>

### <span data-ttu-id="dcee8-130">Microsoft. Azure. Management. Logic. models. workflow</span><span class="sxs-lookup"><span data-stu-id="dcee8-130">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="dcee8-131">Microsoft. Azure. Management. Logic. models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="dcee8-131">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="dcee8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dcee8-132">NOTES</span></span>

## <span data-ttu-id="dcee8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcee8-133">RELATED LINKS</span></span>

[<span data-ttu-id="dcee8-134">Új – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dcee8-134">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="dcee8-135">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dcee8-135">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="dcee8-136">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dcee8-136">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="dcee8-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dcee8-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


