---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195851"
---
# <span data-ttu-id="49a92-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="49a92-101">New-AzLogicApp</span></span>

## <span data-ttu-id="49a92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49a92-102">SYNOPSIS</span></span>
<span data-ttu-id="49a92-103">Logikai alkalmazást hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="49a92-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="49a92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49a92-104">SYNTAX</span></span>

### <span data-ttu-id="49a92-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="49a92-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a92-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="49a92-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49a92-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="49a92-107">DESCRIPTION</span></span>
<span data-ttu-id="49a92-108">A **New-AzLogicApp** parancsmag a Logic apps funkció segítségével hoz létre logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="49a92-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="49a92-109">A logikai alkalmazások a Logic app-definícióban meghatározott műveletek vagy eseményindítók gyűjteményei.</span><span class="sxs-lookup"><span data-stu-id="49a92-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="49a92-110">Ez a parancsmag egy **munkafolyamat** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="49a92-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="49a92-111">Logikai alkalmazást úgy hozhat létre, hogy megadhatja a nevet, a helyet, a logikai app definícióját, az erőforráscsoportot és a csomagot.</span><span class="sxs-lookup"><span data-stu-id="49a92-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="49a92-112">A logikai app-definíciók és a paraméterek JavaScript-objektum formátumban (JSON) vannak formázva.</span><span class="sxs-lookup"><span data-stu-id="49a92-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="49a92-113">A logikai alkalmazások a definíciók és a paraméterek sablonként használhatók.</span><span class="sxs-lookup"><span data-stu-id="49a92-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="49a92-114">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="49a92-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="49a92-115">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="49a92-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="49a92-116">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="49a92-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="49a92-117">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="49a92-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="49a92-118">A parancssorban megadott sablon paraméterben megadott értékek elsőbbséget élveznek a Template paraméteres objektumban lévő sablon paraméter értékeivel.</span><span class="sxs-lookup"><span data-stu-id="49a92-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="49a92-119">Példák</span><span class="sxs-lookup"><span data-stu-id="49a92-119">EXAMPLES</span></span>

### <span data-ttu-id="49a92-120">Példa 1: logikai alkalmazás létrehozása a definíciós és a paraméteres fájlelérési utak segítségével</span><span class="sxs-lookup"><span data-stu-id="49a92-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="49a92-121">A parancs a megadott erőforráscsoport logikai alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="49a92-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="49a92-122">A Logic app a fájlok elérési útján megadott definíciókat és paramétereket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="49a92-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="49a92-123">2. példa: logikai alkalmazás létrehozása a definíciós és a paraméteres objektumokkal</span><span class="sxs-lookup"><span data-stu-id="49a92-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="49a92-124">A parancs a megadott erőforráscsoport-erőforráscsoport logikai alkalmazást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="49a92-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="49a92-125">3. példa: logikai alkalmazás létrehozása a pipeline segítségével az erőforráscsoport megadásához</span><span class="sxs-lookup"><span data-stu-id="49a92-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="49a92-126">Ez a parancs a ResourceGroup11 nevű erőforráscsoportot az Get-AzResourceGroup parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="49a92-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="49a92-127">A parancs a csővezeték-kezelő segítségével átadja az adott erőforráscsoportot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="49a92-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="49a92-128">Az aktuális parancsmag létrehoz egy logikai alkalmazást az adott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="49a92-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="49a92-129">A Logic app a fájlok elérési útján megadott definíciókat és paramétereket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="49a92-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="49a92-130">Példa 4: logikai alkalmazás létrehozása meglévő logikai alkalmazás alapján</span><span class="sxs-lookup"><span data-stu-id="49a92-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="49a92-131">Az első parancs az Get-AzLogicApp parancsmag használatával kapja meg a LogicApp03 nevű logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="49a92-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="49a92-132">A parancs a logikai alkalmazást a $Workflow változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="49a92-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="49a92-133">A második parancs létrehoz egy új logikai alkalmazást, amely a $Workflowban tárolt logikai alkalmazás definícióját és paramétereit használja.</span><span class="sxs-lookup"><span data-stu-id="49a92-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="49a92-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49a92-134">PARAMETERS</span></span>

### <span data-ttu-id="49a92-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a92-135">-DefaultProfile</span></span>
<span data-ttu-id="49a92-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49a92-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49a92-137">-Definition</span><span class="sxs-lookup"><span data-stu-id="49a92-137">-Definition</span></span>
<span data-ttu-id="49a92-138">A logikai alkalmazás definícióját adja meg objektumként vagy egy karakterláncot JavaScript-objektumként (JSON) formátumban.</span><span class="sxs-lookup"><span data-stu-id="49a92-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a92-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="49a92-139">-DefinitionFilePath</span></span>
<span data-ttu-id="49a92-140">Egy logikai alkalmazás definícióját adja meg a JSON formátumú definíciós fájlok elérési útjának elérési útjaként.</span><span class="sxs-lookup"><span data-stu-id="49a92-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a92-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="49a92-141">-IntegrationAccountId</span></span>
<span data-ttu-id="49a92-142">A Logic app-integrációs fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a92-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="49a92-143">-Hely</span><span class="sxs-lookup"><span data-stu-id="49a92-143">-Location</span></span>
<span data-ttu-id="49a92-144">A Logic app helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a92-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="49a92-145">Adjon meg egy Azure Data Center helyet, például Nyugat-amerikai vagy Délkelet-ázsiai.</span><span class="sxs-lookup"><span data-stu-id="49a92-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="49a92-146">A logikai alkalmazást tetszőleges helyre helyezheti.</span><span class="sxs-lookup"><span data-stu-id="49a92-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="49a92-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49a92-147">-Name</span></span>
<span data-ttu-id="49a92-148">A Logic app nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a92-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="49a92-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="49a92-149">-ParameterFilePath</span></span>
<span data-ttu-id="49a92-150">A JSON formátumú paramétert tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a92-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="49a92-151">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="49a92-151">-Parameters</span></span>
<span data-ttu-id="49a92-152">A Logic app Parameters Collection objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a92-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="49a92-153">Adjon meg egy kivonatoló táblázatot, szótárt \<string\> vagy szótárat \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="49a92-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="49a92-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a92-154">-ResourceGroupName</span></span>
<span data-ttu-id="49a92-155">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a92-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="49a92-156">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="49a92-156">-State</span></span>
<span data-ttu-id="49a92-157">A Logic app állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a92-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="49a92-158">A paraméter elfogadható értékei a következők: engedélyezve és letiltva.</span><span class="sxs-lookup"><span data-stu-id="49a92-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="49a92-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49a92-159">-Confirm</span></span>
<span data-ttu-id="49a92-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49a92-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a92-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a92-161">-WhatIf</span></span>
<span data-ttu-id="49a92-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49a92-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a92-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49a92-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a92-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a92-164">CommonParameters</span></span>
<span data-ttu-id="49a92-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49a92-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a92-166">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a92-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a92-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a92-167">INPUTS</span></span>

### <span data-ttu-id="49a92-168">System. String</span><span class="sxs-lookup"><span data-stu-id="49a92-168">System.String</span></span>

## <span data-ttu-id="49a92-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a92-169">OUTPUTS</span></span>

### <span data-ttu-id="49a92-170">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="49a92-170">System.Object</span></span>

## <span data-ttu-id="49a92-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49a92-171">NOTES</span></span>

## <span data-ttu-id="49a92-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49a92-172">RELATED LINKS</span></span>

[<span data-ttu-id="49a92-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="49a92-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="49a92-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="49a92-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="49a92-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="49a92-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="49a92-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="49a92-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

