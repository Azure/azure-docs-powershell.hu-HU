---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154850"
---
# <span data-ttu-id="7b8fe-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="7b8fe-101">New-AzLogicApp</span></span>

## <span data-ttu-id="7b8fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8fe-103">Logikai alkalmazást hoz létre egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="7b8fe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7b8fe-104">SYNTAX</span></span>

### <span data-ttu-id="7b8fe-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b8fe-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b8fe-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b8fe-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b8fe-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7b8fe-107">DESCRIPTION</span></span>
<span data-ttu-id="7b8fe-108">A **New-Az LogicApp** parancsmag a Logic Apps funkcióval létrehoz egy logikai appot.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="7b8fe-109">A logikai appok a Logic App definíciójában definiált műveletek vagy triggerek gyűjteményei.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="7b8fe-110">Ez a parancsmag **munkafolyamat-objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="7b8fe-111">Logikai alkalmazást létrehozhat név, hely, Logic App-definíció, erőforráscsoport és terv megadásával.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="7b8fe-112">A Logic App definíciója és paraméterei a JavaScript Object Notation (JSON) alkalmazásban vannak formázva.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="7b8fe-113">A logikai appokat sablonként használhatja definíciók és paraméterek meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="7b8fe-114">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7b8fe-115">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7b8fe-116">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7b8fe-117">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="7b8fe-118">A parancssorban megadott paraméterfájlértékek elsőbbséget élveznek a sablon paraméterértékeivel a sablon paraméterobjektumában.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="7b8fe-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7b8fe-119">EXAMPLES</span></span>

### <span data-ttu-id="7b8fe-120">1. példa: Logikai alkalmazás létrehozása definíciós és paraméteres fájl elérési utak használatával</span><span class="sxs-lookup"><span data-stu-id="7b8fe-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
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

<span data-ttu-id="7b8fe-121">Ez a parancs létrehoz egy logikai alkalmazást a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="7b8fe-122">A logikai alkalmazás tartalmazza a fájl elérési útjai által megadott definíciót és paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="7b8fe-123">2. példa: Logikai alkalmazás létrehozása definíció- és paraméterobjektumok használatával</span><span class="sxs-lookup"><span data-stu-id="7b8fe-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
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

<span data-ttu-id="7b8fe-124">Ez a parancs létrehoz egy logikai alkalmazást a megadott erőforráscsoport erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="7b8fe-125">3. példa: Logikai alkalmazás létrehozása az erőforráscsoport megadására használt folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="7b8fe-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
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

<span data-ttu-id="7b8fe-126">Ez a parancs az Erőforráscsoport11 nevű erőforráscsoportot a Get-AzResourceGroup parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="7b8fe-127">A parancs a folyamat műveleti operátorával átadja az erőforráscsoportot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7b8fe-128">Az aktuális parancsmag létrehoz egy logikai alkalmazást az erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="7b8fe-129">A logikai alkalmazás tartalmazza a fájl elérési útjai által megadott definíciót és paramétereket.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="7b8fe-130">4. példa: Logikai app létrehozása meglévő logikai app alapján</span><span class="sxs-lookup"><span data-stu-id="7b8fe-130">Example 4: Create a logic app based on an existing logic app</span></span>
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

<span data-ttu-id="7b8fe-131">Az első parancs a LogicApp03 nevű logikai appot a Get-AzLogicApp parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="7b8fe-132">A parancs a logikai alkalmazást a $Workflow tárolja.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="7b8fe-133">A második parancs létrehoz egy új logikai appot, amely a megadott helyen tárolt logikai app definícióját és paramétereit $Workflow.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="7b8fe-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b8fe-134">PARAMETERS</span></span>

### <span data-ttu-id="7b8fe-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8fe-135">-DefaultProfile</span></span>
<span data-ttu-id="7b8fe-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7b8fe-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b8fe-137">-Definition</span><span class="sxs-lookup"><span data-stu-id="7b8fe-137">-Definition</span></span>
<span data-ttu-id="7b8fe-138">A logikai alkalmazás definícióját adja meg objektumként vagy karakterláncként JavaScript Object Notation (JSON) formátumban.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="7b8fe-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="7b8fe-139">-DefinitionFilePath</span></span>
<span data-ttu-id="7b8fe-140">Egy logikai app definícióját adja meg egy JSON formátumú definíciófájl elérési útjaként.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="7b8fe-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="7b8fe-141">-IntegrationAccountId</span></span>
<span data-ttu-id="7b8fe-142">A logikai alkalmazás integrációs fiókazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="7b8fe-143">-Location</span><span class="sxs-lookup"><span data-stu-id="7b8fe-143">-Location</span></span>
<span data-ttu-id="7b8fe-144">A logikai alkalmazás helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="7b8fe-145">Adja meg az Azure-adatközpont helyét, például Nyugat-Egyesült Államok vagy Délkelet-Ázsia.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="7b8fe-146">A logikai alkalmazásokat bármilyen helyen el lehet helyezése.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="7b8fe-147">-Name</span><span class="sxs-lookup"><span data-stu-id="7b8fe-147">-Name</span></span>
<span data-ttu-id="7b8fe-148">A logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="7b8fe-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="7b8fe-149">-ParameterFilePath</span></span>
<span data-ttu-id="7b8fe-150">Egy JSON formátumú paraméterfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="7b8fe-151">-Parameters</span><span class="sxs-lookup"><span data-stu-id="7b8fe-151">-Parameters</span></span>
<span data-ttu-id="7b8fe-152">A Logic app paramétergyűjtemény-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="7b8fe-153">Adjon meg egy kivonattáblát, szótárat \<string\> vagy \<string, WorkflowParameter\> szótárat.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="7b8fe-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b8fe-154">-ResourceGroupName</span></span>
<span data-ttu-id="7b8fe-155">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7b8fe-156">-State</span><span class="sxs-lookup"><span data-stu-id="7b8fe-156">-State</span></span>
<span data-ttu-id="7b8fe-157">A logikai alkalmazás állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="7b8fe-158">A paraméter elfogadható értékei: Engedélyezve és Letiltva.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="7b8fe-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b8fe-159">-Confirm</span></span>
<span data-ttu-id="7b8fe-160">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b8fe-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b8fe-161">-WhatIf</span></span>
<span data-ttu-id="7b8fe-162">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b8fe-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b8fe-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8fe-164">CommonParameters</span></span>
<span data-ttu-id="7b8fe-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8fe-166">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b8fe-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8fe-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b8fe-167">INPUTS</span></span>

### <span data-ttu-id="7b8fe-168">System.String</span><span class="sxs-lookup"><span data-stu-id="7b8fe-168">System.String</span></span>

## <span data-ttu-id="7b8fe-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b8fe-169">OUTPUTS</span></span>

### <span data-ttu-id="7b8fe-170">System.Object</span><span class="sxs-lookup"><span data-stu-id="7b8fe-170">System.Object</span></span>

## <span data-ttu-id="7b8fe-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7b8fe-171">NOTES</span></span>

## <span data-ttu-id="7b8fe-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b8fe-172">RELATED LINKS</span></span>

[<span data-ttu-id="7b8fe-173">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="7b8fe-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="7b8fe-174">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="7b8fe-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="7b8fe-175">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="7b8fe-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="7b8fe-176">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="7b8fe-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


