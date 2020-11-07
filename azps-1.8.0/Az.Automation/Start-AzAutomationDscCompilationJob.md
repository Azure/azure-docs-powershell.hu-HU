---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 53a0527570e9168038bb1636c476e09e5bda6d66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671493"
---
# <span data-ttu-id="f7936-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f7936-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="f7936-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7936-102">SYNOPSIS</span></span>
<span data-ttu-id="f7936-103">A DSC-konfiguráció fordítása automatizálással.</span><span class="sxs-lookup"><span data-stu-id="f7936-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="f7936-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7936-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7936-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7936-105">DESCRIPTION</span></span>
<span data-ttu-id="f7936-106">A **Start-AzAutomationDscCompilationJob** PARANCSMAG egy APS-alapú, az Azure automatizáláshoz szükséges konfigurációt fordítja le.</span><span class="sxs-lookup"><span data-stu-id="f7936-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="f7936-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f7936-107">EXAMPLES</span></span>

### <span data-ttu-id="f7936-108">Példa 1: Azure DSC-konfiguráció összeállítása automatizálással</span><span class="sxs-lookup"><span data-stu-id="f7936-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f7936-109">Az első parancs létrehozza a paraméterek szótárát, és a $Params változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="f7936-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="f7936-110">A második parancs a Config01 nevű DSC-konfigurációt fordítja le.</span><span class="sxs-lookup"><span data-stu-id="f7936-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="f7936-111">A parancs a DSC konfiguráció paramétereinek $Params értékeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f7936-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="f7936-112">2. példa: az Azure DSC-konfiguráció fordítása automatizálással az új csomópont-konfiguráció-összeállítási verzióval</span><span class="sxs-lookup"><span data-stu-id="f7936-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="f7936-113">Az első példához hasonlóan az első parancs létrehozza a paraméterek szótárát, és a $Params változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="f7936-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="f7936-114">A második parancs a Config01 nevű DSC-konfigurációt fordítja le.</span><span class="sxs-lookup"><span data-stu-id="f7936-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="f7936-115">A parancs a DSC konfiguráció paramétereinek $Params értékeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f7936-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="f7936-116">A korábbi meglévő csomópont-konfigurációt nem bírálja felül, ha új csomópont-konfigurációt hoz létre a név Config01 [<2>]. <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="f7936-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="f7936-117">A verziószám a már meglévő verziószám alapján növekszik.</span><span class="sxs-lookup"><span data-stu-id="f7936-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="f7936-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7936-118">PARAMETERS</span></span>

### <span data-ttu-id="f7936-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f7936-119">-AutomationAccountName</span></span>
<span data-ttu-id="f7936-120">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f7936-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="f7936-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="f7936-121">-ConfigurationData</span></span>
<span data-ttu-id="f7936-122">A DSC konfigurációhoz használt konfigurációs adatokat tartalmazó szótárt adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7936-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

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

### <span data-ttu-id="f7936-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f7936-123">-ConfigurationName</span></span>
<span data-ttu-id="f7936-124">Itt adhatja meg annak a DSC-konfigurációnak a nevét, amelyet a parancsmag lefordít.</span><span class="sxs-lookup"><span data-stu-id="f7936-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="f7936-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7936-125">-DefaultProfile</span></span>
<span data-ttu-id="f7936-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f7936-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7936-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="f7936-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="f7936-128">Létrehoz egy új csomópont-konfiguráció-összeállítási verziót.</span><span class="sxs-lookup"><span data-stu-id="f7936-128">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="f7936-129">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="f7936-129">-Parameters</span></span>
<span data-ttu-id="f7936-130">A parancsmag által a DSC-konfiguráció összeállításához használt paraméterek szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7936-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

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

### <span data-ttu-id="f7936-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7936-131">-ResourceGroupName</span></span>
<span data-ttu-id="f7936-132">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="f7936-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="f7936-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7936-133">-Confirm</span></span>
<span data-ttu-id="f7936-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7936-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7936-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7936-135">-WhatIf</span></span>
<span data-ttu-id="f7936-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7936-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7936-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7936-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7936-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7936-138">CommonParameters</span></span>
<span data-ttu-id="f7936-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7936-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7936-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7936-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7936-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7936-141">INPUTS</span></span>

### <span data-ttu-id="f7936-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f7936-142">System.String</span></span>

## <span data-ttu-id="f7936-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7936-143">OUTPUTS</span></span>

### <span data-ttu-id="f7936-144">Microsoft. Azure. Command. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f7936-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f7936-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7936-145">NOTES</span></span>

## <span data-ttu-id="f7936-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7936-146">RELATED LINKS</span></span>

[<span data-ttu-id="f7936-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f7936-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="f7936-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="f7936-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


