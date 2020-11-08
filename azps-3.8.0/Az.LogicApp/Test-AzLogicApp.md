---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: e13f4af6f998b069168dfffca3dedc7ba385841e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002868"
---
# <span data-ttu-id="fd21c-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fd21c-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="fd21c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd21c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd21c-103">Egy logikai alkalmazás definíciójának érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="fd21c-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="fd21c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd21c-104">SYNTAX</span></span>

### <span data-ttu-id="fd21c-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd21c-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd21c-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd21c-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd21c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd21c-107">DESCRIPTION</span></span>
<span data-ttu-id="fd21c-108">A **teszt-AzLogicApp** parancsmag egy erőforráscsoport logikai app-definícióját ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="fd21c-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="fd21c-109">Adja meg a logikai app nevét, az erőforrás-csoport nevét, a helyet, az állapotot, az integrációs fiók AZONOSÍTÓját vagy a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="fd21c-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="fd21c-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="fd21c-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fd21c-111">Ha dinamikus paramétert szeretne használni, írja be azt a parancsba.</span><span class="sxs-lookup"><span data-stu-id="fd21c-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fd21c-112">A dinamikus paraméterek nevének feltárásához írjon be egy kötőjelet (-) a parancsmag neve után, majd nyomja le többször a TAB billentyűt a rendelkezésre álló paraméterek közötti váltáshoz.</span><span class="sxs-lookup"><span data-stu-id="fd21c-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fd21c-113">Ha kihagyja a szükséges sablon paramétert, a parancsmag kéri az érték megadását.</span><span class="sxs-lookup"><span data-stu-id="fd21c-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fd21c-114">Példák</span><span class="sxs-lookup"><span data-stu-id="fd21c-114">EXAMPLES</span></span>

### <span data-ttu-id="fd21c-115">1. példa: a logikai alkalmazások érvényesítése fájlelérési utak használatával</span><span class="sxs-lookup"><span data-stu-id="fd21c-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="fd21c-116">Ez a parancs ellenőrzi a megadott erőforráscsoport LogicApp01 nevű logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="fd21c-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="fd21c-117">A parancs a definíciós és a paraméteres fájlok elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="fd21c-118">2. példa: logikai app érvényesítése objektumok használatával</span><span class="sxs-lookup"><span data-stu-id="fd21c-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="fd21c-119">Ez a parancs ellenőrzi a megadott erőforráscsoport LogicApp01 nevű logikai alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="fd21c-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="fd21c-120">A parancs a definíciós és a paraméteres objektumokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="fd21c-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd21c-121">PARAMETERS</span></span>

### <span data-ttu-id="fd21c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd21c-122">-DefaultProfile</span></span>
<span data-ttu-id="fd21c-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd21c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd21c-124">-Definition</span><span class="sxs-lookup"><span data-stu-id="fd21c-124">-Definition</span></span>
<span data-ttu-id="fd21c-125">Egy logikai alkalmazás definícióját adja meg objektumként vagy egy karakterláncot JavaScript-objektumként (JSON) formátumban.</span><span class="sxs-lookup"><span data-stu-id="fd21c-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd21c-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="fd21c-126">-DefinitionFilePath</span></span>
<span data-ttu-id="fd21c-127">A logikai alkalmazás definícióját adja meg a JSON formátumú definíciós fájlok elérési útjának elérési útjaként.</span><span class="sxs-lookup"><span data-stu-id="fd21c-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd21c-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="fd21c-128">-IntegrationAccountId</span></span>
<span data-ttu-id="fd21c-129">A Logic app-integrációs fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-129">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="fd21c-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="fd21c-130">-Location</span></span>
<span data-ttu-id="fd21c-131">A Logic app helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="fd21c-132">Adjon meg egy Azure Data Center helyet, például Nyugat-amerikai vagy Délkelet-ázsiai.</span><span class="sxs-lookup"><span data-stu-id="fd21c-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="fd21c-133">A logikai alkalmazást tetszőleges helyre helyezheti.</span><span class="sxs-lookup"><span data-stu-id="fd21c-133">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="fd21c-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd21c-134">-Name</span></span>
<span data-ttu-id="fd21c-135">A Logic app nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-135">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="fd21c-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="fd21c-136">-ParameterFilePath</span></span>
<span data-ttu-id="fd21c-137">A JSON formátumú paramétert tartalmazó fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-137">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="fd21c-138">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="fd21c-138">-Parameters</span></span>
<span data-ttu-id="fd21c-139">A Logic app Parameters Collection objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="fd21c-140">Adjon meg egy hash-táblázatot, szótár- \< karakterláncot \> vagy szótári \< karakterláncot a WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="fd21c-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="fd21c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd21c-141">-ResourceGroupName</span></span>
<span data-ttu-id="fd21c-142">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fd21c-143">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="fd21c-143">-State</span></span>
<span data-ttu-id="fd21c-144">A Logic app állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="fd21c-145">A paraméter elfogadható értékei a következők: engedélyezve és letiltva.</span><span class="sxs-lookup"><span data-stu-id="fd21c-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="fd21c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd21c-146">CommonParameters</span></span>
<span data-ttu-id="fd21c-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd21c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd21c-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd21c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd21c-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd21c-149">INPUTS</span></span>

### <span data-ttu-id="fd21c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="fd21c-150">System.String</span></span>

## <span data-ttu-id="fd21c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd21c-151">OUTPUTS</span></span>

### <span data-ttu-id="fd21c-152">System. Void</span><span class="sxs-lookup"><span data-stu-id="fd21c-152">System.Void</span></span>

## <span data-ttu-id="fd21c-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd21c-153">NOTES</span></span>

## <span data-ttu-id="fd21c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd21c-154">RELATED LINKS</span></span>

[<span data-ttu-id="fd21c-155">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fd21c-155">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="fd21c-156">Új – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fd21c-156">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="fd21c-157">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fd21c-157">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="fd21c-158">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fd21c-158">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="fd21c-159">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fd21c-159">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


