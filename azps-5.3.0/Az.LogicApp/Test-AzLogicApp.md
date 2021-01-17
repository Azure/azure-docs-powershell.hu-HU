---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386117"
---
# <span data-ttu-id="9cdc4-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9cdc4-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="9cdc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cdc4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdc4-103">Logikai alkalmazásdefiníciót ellenőriz.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="9cdc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9cdc4-104">SYNTAX</span></span>

### <span data-ttu-id="9cdc4-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cdc4-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cdc4-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cdc4-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cdc4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9cdc4-107">DESCRIPTION</span></span>
<span data-ttu-id="9cdc4-108">A **Test-AzCmApp** parancsmag egy logikai appdefiníciót ellenőriz egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="9cdc4-109">Adja meg a logikai alkalmazás nevét, az erőforráscsoport nevét, a helyet, az állapotot, az integrációs fiókazonosítót vagy a paramétereket.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="9cdc4-110">Ez a modul támogatja a dinamikus paramétereket.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9cdc4-111">Ha dinamikus paramétert használ, írja be a parancsba.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9cdc4-112">A dinamikus paraméterek nevének felfedezéséhez írjon be egy kötőjelet (-) a parancsmag neve után, majd a Tab billentyű többszöri lenyomása után lépkedhet a rendelkezésre álló paraméterek között.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9cdc4-113">Ha kihagy egy kötelező sablonparamétert, a parancsmag rákérdez az értékre.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9cdc4-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9cdc4-114">EXAMPLES</span></span>

### <span data-ttu-id="9cdc4-115">1. példa: Logikai alkalmazás érvényesítése fájl elérési utak használatával</span><span class="sxs-lookup"><span data-stu-id="9cdc4-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="9cdc4-116">Ez a parancs ellenőrzi a LogicApp01 nevű logikai appot a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="9cdc4-117">A parancs megadja a definíció és a paraméter elérési útját.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="9cdc4-118">2. példa: Logikai alkalmazás érvényesítése objektumok használatával</span><span class="sxs-lookup"><span data-stu-id="9cdc4-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="9cdc4-119">Ez a parancs ellenőrzi a LogicApp01 nevű logikai appot a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="9cdc4-120">A parancs definíciót és paraméterobjektumokat ad meg.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="9cdc4-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="9cdc4-121">Example 3</span></span>

<span data-ttu-id="9cdc4-122">Logikai alkalmazásdefiníciót ellenőriz.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-122">Validates a logic app definition.</span></span> <span data-ttu-id="9cdc4-123">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="9cdc4-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="9cdc4-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cdc4-124">PARAMETERS</span></span>

### <span data-ttu-id="9cdc4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdc4-125">-DefaultProfile</span></span>
<span data-ttu-id="9cdc4-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9cdc4-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cdc4-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="9cdc4-127">-Definition</span></span>
<span data-ttu-id="9cdc4-128">A logikai app definícióját adja meg objektumként vagy karakterláncként JavaScript objektum-notation (JSON) formátumban.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="9cdc4-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="9cdc4-129">-DefinitionFilePath</span></span>
<span data-ttu-id="9cdc4-130">A logikai alkalmazás definícióját adja meg egy JSON formátumú definíciós fájl elérési útjaként.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="9cdc4-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="9cdc4-131">-IntegrationAccountId</span></span>
<span data-ttu-id="9cdc4-132">A logikai alkalmazás integrációs fiókazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="9cdc4-133">-Location</span><span class="sxs-lookup"><span data-stu-id="9cdc4-133">-Location</span></span>
<span data-ttu-id="9cdc4-134">A logikai alkalmazás helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="9cdc4-135">Adja meg az Azure-adatközpont helyét, például Nyugat-Egyesült Államok vagy Délkelet-Ázsia.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="9cdc4-136">A logikai alkalmazásokat bármilyen helyen el lehet helyezése.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="9cdc4-137">-Name</span><span class="sxs-lookup"><span data-stu-id="9cdc4-137">-Name</span></span>
<span data-ttu-id="9cdc4-138">A logikai alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="9cdc4-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="9cdc4-139">-ParameterFilePath</span></span>
<span data-ttu-id="9cdc4-140">Egy JSON formátumú paraméterfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="9cdc4-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="9cdc4-141">-Parameters</span></span>
<span data-ttu-id="9cdc4-142">A logikai alkalmazás paramétergyűjtemény-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="9cdc4-143">Adjon meg egy kivonattáblát, szótárat \<string\> vagy \<string, WorkflowParameter\> szótárat.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="9cdc4-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cdc4-144">-ResourceGroupName</span></span>
<span data-ttu-id="9cdc4-145">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9cdc4-146">-State</span><span class="sxs-lookup"><span data-stu-id="9cdc4-146">-State</span></span>
<span data-ttu-id="9cdc4-147">A logikai alkalmazás állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="9cdc4-148">A paraméter elfogadható értékei: Engedélyezve és Letiltva.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="9cdc4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdc4-149">CommonParameters</span></span>
<span data-ttu-id="9cdc4-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cdc4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdc4-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cdc4-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdc4-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cdc4-152">INPUTS</span></span>

### <span data-ttu-id="9cdc4-153">System.String</span><span class="sxs-lookup"><span data-stu-id="9cdc4-153">System.String</span></span>

## <span data-ttu-id="9cdc4-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cdc4-154">OUTPUTS</span></span>

### <span data-ttu-id="9cdc4-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="9cdc4-155">System.Void</span></span>

## <span data-ttu-id="9cdc4-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9cdc4-156">NOTES</span></span>

## <span data-ttu-id="9cdc4-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cdc4-157">RELATED LINKS</span></span>

[<span data-ttu-id="9cdc4-158">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="9cdc4-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="9cdc4-159">New-AzApp</span><span class="sxs-lookup"><span data-stu-id="9cdc4-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="9cdc4-160">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="9cdc4-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="9cdc4-161">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="9cdc4-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="9cdc4-162">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="9cdc4-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


