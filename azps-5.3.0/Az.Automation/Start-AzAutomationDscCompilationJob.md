---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478469"
---
# <span data-ttu-id="dc6ef-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dc6ef-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="dc6ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc6ef-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6ef-103">DSC-konfigurációt ad össze az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="dc6ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dc6ef-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc6ef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dc6ef-105">DESCRIPTION</span></span>
<span data-ttu-id="dc6ef-106">A **Start-AzAutomationDscCompilation Parancsmag az** APS kívánt állapotkonfigurációs (DSC) konfigurációját állítja össze az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="dc6ef-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dc6ef-107">EXAMPLES</span></span>

### <span data-ttu-id="dc6ef-108">1. példa: Azure DSC-konfiguráció fordítása az Automatizálásban</span><span class="sxs-lookup"><span data-stu-id="dc6ef-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dc6ef-109">Az első parancs létrehozza a paraméterek szótárát, és tárolja őket a $Params változóban.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="dc6ef-110">A második parancs lefordítja a Config01 nevű DSC-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="dc6ef-111">A parancs a DSC konfigurációs $Params értékeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="dc6ef-112">2. példa: Azure DSC-konfiguráció összeállítása az Automatizálásban egy új csomópontkonfigurációs buildverzióval.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="dc6ef-113">Az első példához hasonlóan az első parancs létrehoz egy szótárat a paraméterekből, és tárolja őket a $Params változóban.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="dc6ef-114">A második parancs lefordítja a Config01 nevű DSC-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="dc6ef-115">A parancs a DSC konfigurációs $Params értékeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="dc6ef-116">Nem bírálja felül a korábbi csomópontkonfigurációt egy új, Config01[<2>] nevű csomópontkonfiguráció <NodeName> létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="dc6ef-117">A verziószám a már meglévő verziószám alapján nő.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="dc6ef-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc6ef-118">PARAMETERS</span></span>

### <span data-ttu-id="dc6ef-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc6ef-119">-AutomationAccountName</span></span>
<span data-ttu-id="dc6ef-120">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ef-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="dc6ef-121">-ConfigurationData</span></span>
<span data-ttu-id="dc6ef-122">A DSC-konfiguráció konfigurációs adatainak szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ef-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="dc6ef-123">-ConfigurationName</span></span>
<span data-ttu-id="dc6ef-124">A parancsmag által lefordított DSC-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6ef-125">-DefaultProfile</span></span>
<span data-ttu-id="dc6ef-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dc6ef-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc6ef-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="dc6ef-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="dc6ef-128">Létrehozza a csomópont konfigurációjának új verzióját.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ef-129">-Parameters</span><span class="sxs-lookup"><span data-stu-id="dc6ef-129">-Parameters</span></span>
<span data-ttu-id="dc6ef-130">A parancsmag által a DSC-konfiguráció lefordítása során használt paraméterek szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc6ef-131">-ResourceGroupName</span></span>
<span data-ttu-id="dc6ef-132">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag konfigurációt fordít.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ef-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc6ef-133">-Confirm</span></span>
<span data-ttu-id="dc6ef-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ef-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc6ef-135">-WhatIf</span></span>
<span data-ttu-id="dc6ef-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc6ef-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6ef-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6ef-138">CommonParameters</span></span>
<span data-ttu-id="dc6ef-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6ef-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6ef-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc6ef-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6ef-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc6ef-141">INPUTS</span></span>

### <span data-ttu-id="dc6ef-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dc6ef-142">System.String</span></span>

## <span data-ttu-id="dc6ef-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc6ef-143">OUTPUTS</span></span>

### <span data-ttu-id="dc6ef-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="dc6ef-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="dc6ef-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dc6ef-145">NOTES</span></span>

## <span data-ttu-id="dc6ef-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc6ef-146">RELATED LINKS</span></span>

[<span data-ttu-id="dc6ef-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dc6ef-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="dc6ef-148">Get-AzAutomationDscCompilationOutput</span><span class="sxs-lookup"><span data-stu-id="dc6ef-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


