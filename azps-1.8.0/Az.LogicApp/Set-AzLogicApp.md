---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 254ab4f1dd126e1b671c9a1d899a9dbe8e71beca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835349"
---
# <span data-ttu-id="6e2a9-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6e2a9-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="6e2a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2a9-103">Egy logikai alkalmazást módosított egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="6e2a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e2a9-104">SYNTAX</span></span>

### <span data-ttu-id="6e2a9-105">Felhasználás (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e2a9-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e2a9-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="6e2a9-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e2a9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e2a9-107">DESCRIPTION</span></span>
<span data-ttu-id="6e2a9-108">A **set-AzLogicApp** parancsmag a Logic apps funkció használatával módosítja a logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="6e2a9-109">A logikai alkalmazások a Logic app-definícióban meghatározott műveletek vagy eseményindítók gyűjteményei.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="6e2a9-110">Ez a parancsmag egy **munkafolyamat** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="6e2a9-111">A logikai alkalmazásokat a név, a hely, a logikai app-definíció, az erőforráscsoport és a terv megadásával módosíthatja.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="6e2a9-112">A logikai app-definíciók és a paraméterek JavaScript-objektum formátumban (JSON) vannak formázva.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="6e2a9-113">A logikai alkalmazások a definíciók és a paraméterek sablonként használhatók.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="6e2a9-114">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6e2a9-115">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6e2a9-116">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6e2a9-117">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="6e2a9-118">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="6e2a9-119">Példák</span><span class="sxs-lookup"><span data-stu-id="6e2a9-119">EXAMPLES</span></span>

### <span data-ttu-id="6e2a9-120">Példa 1: logikai alkalmazás módosítása</span><span class="sxs-lookup"><span data-stu-id="6e2a9-120">Example 1: Modify a logic app</span></span>
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

<span data-ttu-id="6e2a9-121">Ez a parancs módosítja a logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="6e2a9-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e2a9-122">PARAMETERS</span></span>

### <span data-ttu-id="6e2a9-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6e2a9-123">-AppServicePlan</span></span>
<span data-ttu-id="6e2a9-124">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="6e2a9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2a9-125">-DefaultProfile</span></span>
<span data-ttu-id="6e2a9-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6e2a9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e2a9-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="6e2a9-127">-Definition</span></span>
<span data-ttu-id="6e2a9-128">Egy logikai alkalmazás definícióját adja meg objektumként vagy egy karakterláncot JavaScript-objektumként (JSON) formátumban.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="6e2a9-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="6e2a9-129">-DefinitionFilePath</span></span>
<span data-ttu-id="6e2a9-130">Egy logikai alkalmazás definícióját adja meg a JSON formátumú definíciós fájlok elérési útjának elérési útjaként.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="6e2a9-131">-Force</span><span class="sxs-lookup"><span data-stu-id="6e2a9-131">-Force</span></span>
<span data-ttu-id="6e2a9-132">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e2a9-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="6e2a9-133">-IntegrationAccountId</span></span>
<span data-ttu-id="6e2a9-134">A Logic app-integrációs fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="6e2a9-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e2a9-135">-Name</span></span>
<span data-ttu-id="6e2a9-136">A logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="6e2a9-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="6e2a9-137">-ParameterFilePath</span></span>
<span data-ttu-id="6e2a9-138">A JSON formátumú paramétert tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="6e2a9-139">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="6e2a9-139">-Parameters</span></span>
<span data-ttu-id="6e2a9-140">A Logic app Parameters Collection objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="6e2a9-141">Adjon meg egy hash-táblázatot, szótár- \< karakterláncot \> vagy szótári \< karakterláncot a WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="6e2a9-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="6e2a9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e2a9-142">-ResourceGroupName</span></span>
<span data-ttu-id="6e2a9-143">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6e2a9-144">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="6e2a9-144">-State</span></span>
<span data-ttu-id="6e2a9-145">A Logic app állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="6e2a9-146">A paraméter elfogadható értékei a következők: engedélyezve és letiltva.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="6e2a9-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="6e2a9-147">-UseConsumptionModel</span></span>
<span data-ttu-id="6e2a9-148">Jelzi, hogy a Logic app számlázása a fogyasztási modellt használja.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-148">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="6e2a9-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e2a9-149">-Confirm</span></span>
<span data-ttu-id="6e2a9-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e2a9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e2a9-151">-WhatIf</span></span>
<span data-ttu-id="6e2a9-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e2a9-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e2a9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2a9-154">CommonParameters</span></span>
<span data-ttu-id="6e2a9-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e2a9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2a9-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e2a9-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2a9-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e2a9-157">INPUTS</span></span>

### <span data-ttu-id="6e2a9-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6e2a9-158">System.String</span></span>

## <span data-ttu-id="6e2a9-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e2a9-159">OUTPUTS</span></span>

### <span data-ttu-id="6e2a9-160">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="6e2a9-160">System.Object</span></span>

## <span data-ttu-id="6e2a9-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e2a9-161">NOTES</span></span>

## <span data-ttu-id="6e2a9-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e2a9-162">RELATED LINKS</span></span>

[<span data-ttu-id="6e2a9-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6e2a9-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="6e2a9-164">Új – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6e2a9-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="6e2a9-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6e2a9-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="6e2a9-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6e2a9-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


