---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: ffa84b2c5ec4ccfdc48cae4e68cbe562034f7e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679187"
---
# <span data-ttu-id="d8301-101">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d8301-101">Start-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="d8301-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8301-102">SYNOPSIS</span></span>
<span data-ttu-id="d8301-103">A DSC-konfiguráció fordítása automatizálással.</span><span class="sxs-lookup"><span data-stu-id="d8301-103">Compiles a DSC configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8301-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8301-104">SYNTAX</span></span>

```
Start-AzureRmAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8301-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8301-105">DESCRIPTION</span></span>
<span data-ttu-id="d8301-106">A **Start-AzureRmAutomationDscCompilationJob** PARANCSMAG egy APS-alapú, az Azure automatizáláshoz szükséges konfigurációt fordítja le.</span><span class="sxs-lookup"><span data-stu-id="d8301-106">The **Start-AzureRmAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="d8301-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d8301-107">EXAMPLES</span></span>

### <span data-ttu-id="d8301-108">Példa 1: Azure DSC-konfiguráció összeállítása automatizálással</span><span class="sxs-lookup"><span data-stu-id="d8301-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d8301-109">Az első parancs létrehozza a paraméterek szótárát, és a $Params változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d8301-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="d8301-110">A második parancs a Config01 nevű DSC-konfigurációt fordítja le.</span><span class="sxs-lookup"><span data-stu-id="d8301-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="d8301-111">A parancs a DSC konfiguráció paramétereinek $Params értékeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d8301-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="d8301-112">2. példa: az Azure DSC-konfiguráció fordítása automatizálással az új csomópont-konfiguráció-összeállítási verzióval</span><span class="sxs-lookup"><span data-stu-id="d8301-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="d8301-113">Az első példához hasonlóan az első parancs létrehozza a paraméterek szótárát, és a $Params változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="d8301-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="d8301-114">A második parancs a Config01 nevű DSC-konfigurációt fordítja le.</span><span class="sxs-lookup"><span data-stu-id="d8301-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="d8301-115">A parancs a DSC konfiguráció paramétereinek $Params értékeit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d8301-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="d8301-116">A korábbi meglévő csomópont-konfigurációt nem bírálja felül, ha új csomópont-konfigurációt hoz létre a név Config01 [<2>]. <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="d8301-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="d8301-117">A verziószám a már meglévő verziószám alapján növekszik.</span><span class="sxs-lookup"><span data-stu-id="d8301-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="d8301-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8301-118">PARAMETERS</span></span>

### <span data-ttu-id="d8301-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8301-119">-AutomationAccountName</span></span>
<span data-ttu-id="d8301-120">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d8301-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="d8301-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="d8301-121">-ConfigurationData</span></span>
<span data-ttu-id="d8301-122">A DSC konfigurációhoz használt konfigurációs adatokat tartalmazó szótárt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8301-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

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

### <span data-ttu-id="d8301-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d8301-123">-ConfigurationName</span></span>
<span data-ttu-id="d8301-124">Itt adhatja meg annak a DSC-konfigurációnak a nevét, amelyet a parancsmag lefordít.</span><span class="sxs-lookup"><span data-stu-id="d8301-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="d8301-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8301-125">-DefaultProfile</span></span>
<span data-ttu-id="d8301-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8301-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8301-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="d8301-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="d8301-128">Létrehoz egy új csomópont-konfiguráció-összeállítási verziót.</span><span class="sxs-lookup"><span data-stu-id="d8301-128">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="d8301-129">-Paraméterek</span><span class="sxs-lookup"><span data-stu-id="d8301-129">-Parameters</span></span>
<span data-ttu-id="d8301-130">A parancsmag által a DSC-konfiguráció összeállításához használt paraméterek szótárát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8301-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

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

### <span data-ttu-id="d8301-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8301-131">-ResourceGroupName</span></span>
<span data-ttu-id="d8301-132">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="d8301-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="d8301-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8301-133">-Confirm</span></span>
<span data-ttu-id="d8301-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8301-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8301-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8301-135">-WhatIf</span></span>
<span data-ttu-id="d8301-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8301-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8301-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8301-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8301-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8301-138">CommonParameters</span></span>
<span data-ttu-id="d8301-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8301-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8301-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8301-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8301-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8301-141">INPUTS</span></span>

### <span data-ttu-id="d8301-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d8301-142">System.String</span></span>

## <span data-ttu-id="d8301-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8301-143">OUTPUTS</span></span>

### <span data-ttu-id="d8301-144">Microsoft. Azure. Command. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="d8301-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="d8301-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8301-145">NOTES</span></span>

## <span data-ttu-id="d8301-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8301-146">RELATED LINKS</span></span>

[<span data-ttu-id="d8301-147">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d8301-147">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="d8301-148">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d8301-148">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)


