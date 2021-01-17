---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368365"
---
# <span data-ttu-id="49300-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="49300-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="49300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49300-102">SYNOPSIS</span></span>
<span data-ttu-id="49300-103">Módosít egy logikai alkalmazást egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="49300-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="49300-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49300-104">SYNTAX</span></span>

### <span data-ttu-id="49300-105">Felhasználás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49300-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49300-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="49300-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49300-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49300-107">DESCRIPTION</span></span>
<span data-ttu-id="49300-108">A **Set-Az EgészAlkalmazás** parancsmag a Logic Apps funkcióval módosítja a logikai appokat.</span><span class="sxs-lookup"><span data-stu-id="49300-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="49300-109">A logikai appok a Logic App definíciójában definiált műveletek vagy triggerek gyűjteményei.</span><span class="sxs-lookup"><span data-stu-id="49300-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="49300-110">Ez a parancsmag **munkafolyamat-objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="49300-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="49300-111">A logikai appokat név, hely, Logic App-definíció, erőforráscsoport és terv megadásával módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="49300-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="49300-112">A Logic App definíciója és paraméterei a JavaScript Object Notation (JSON) alkalmazásban vannak formázva.</span><span class="sxs-lookup"><span data-stu-id="49300-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="49300-113">A logikai appokat sablonként használhatja definíciók és paraméterek meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="49300-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="49300-114">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="49300-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="49300-115">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="49300-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="49300-116">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="49300-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="49300-117">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="49300-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="49300-118">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterértékeivel a sablon paraméterobjektumában.</span><span class="sxs-lookup"><span data-stu-id="49300-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="49300-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49300-119">EXAMPLES</span></span>

### <span data-ttu-id="49300-120">1. példa: Logikai alkalmazás módosítása</span><span class="sxs-lookup"><span data-stu-id="49300-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="49300-121">Ez a parancs módosít egy logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="49300-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="49300-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49300-122">PARAMETERS</span></span>

### <span data-ttu-id="49300-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="49300-123">-AppServicePlan</span></span>
<span data-ttu-id="49300-124">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49300-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49300-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49300-125">-DefaultProfile</span></span>
<span data-ttu-id="49300-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49300-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49300-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="49300-127">-Definition</span></span>
<span data-ttu-id="49300-128">A logikai app definícióját adja meg objektumként vagy karakterláncként JavaScript objektum-notation (JSON) formátumban.</span><span class="sxs-lookup"><span data-stu-id="49300-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49300-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="49300-129">-DefinitionFilePath</span></span>
<span data-ttu-id="49300-130">Egy logikai app definícióját adja meg egy JSON formátumú definíciós fájl elérési útjaként.</span><span class="sxs-lookup"><span data-stu-id="49300-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="49300-131">-Force</span><span class="sxs-lookup"><span data-stu-id="49300-131">-Force</span></span>
<span data-ttu-id="49300-132">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="49300-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49300-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="49300-133">-IntegrationAccountId</span></span>
<span data-ttu-id="49300-134">A logikai alkalmazás integrációs fiókazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49300-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="49300-135">-Name</span><span class="sxs-lookup"><span data-stu-id="49300-135">-Name</span></span>
<span data-ttu-id="49300-136">Egy logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49300-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="49300-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="49300-137">-ParameterFilePath</span></span>
<span data-ttu-id="49300-138">Egy JSON formátumú paraméterfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49300-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="49300-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="49300-139">-Parameters</span></span>
<span data-ttu-id="49300-140">A Logic app paramétergyűjtemény-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49300-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="49300-141">Adjon meg egy kivonattáblát, szótárat \<string\> vagy \<string, WorkflowParameter\> szótárat.</span><span class="sxs-lookup"><span data-stu-id="49300-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49300-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49300-142">-ResourceGroupName</span></span>
<span data-ttu-id="49300-143">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49300-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="49300-144">-State</span><span class="sxs-lookup"><span data-stu-id="49300-144">-State</span></span>
<span data-ttu-id="49300-145">A logikai alkalmazás állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="49300-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="49300-146">A paraméter elfogadható értékei: Engedélyezve és Letiltva.</span><span class="sxs-lookup"><span data-stu-id="49300-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49300-147">-UseConstionModel</span><span class="sxs-lookup"><span data-stu-id="49300-147">-UseConsumptionModel</span></span>
<span data-ttu-id="49300-148">Azt jelzi, hogy a logic app számlázása a felhasználásalapú modellt használja.</span><span class="sxs-lookup"><span data-stu-id="49300-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49300-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49300-149">-Confirm</span></span>
<span data-ttu-id="49300-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="49300-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49300-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49300-151">-WhatIf</span></span>
<span data-ttu-id="49300-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="49300-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49300-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49300-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49300-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49300-154">CommonParameters</span></span>
<span data-ttu-id="49300-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49300-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49300-156">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49300-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49300-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49300-157">INPUTS</span></span>

### <span data-ttu-id="49300-158">System.String</span><span class="sxs-lookup"><span data-stu-id="49300-158">System.String</span></span>

## <span data-ttu-id="49300-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49300-159">OUTPUTS</span></span>

### <span data-ttu-id="49300-160">System.Object</span><span class="sxs-lookup"><span data-stu-id="49300-160">System.Object</span></span>

## <span data-ttu-id="49300-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49300-161">NOTES</span></span>

## <span data-ttu-id="49300-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49300-162">RELATED LINKS</span></span>

[<span data-ttu-id="49300-163">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="49300-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="49300-164">New-AzApp</span><span class="sxs-lookup"><span data-stu-id="49300-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="49300-165">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="49300-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="49300-166">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="49300-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


