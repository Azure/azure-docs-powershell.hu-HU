---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183725"
---
# <span data-ttu-id="ed03e-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed03e-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="ed03e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed03e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed03e-103">A DSC csomópont-konfigurációk metaadatait kapja az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="ed03e-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="ed03e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed03e-104">SYNTAX</span></span>

### <span data-ttu-id="ed03e-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed03e-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed03e-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ed03e-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed03e-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ed03e-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed03e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed03e-108">DESCRIPTION</span></span>
<span data-ttu-id="ed03e-109">A **Get-AzAutomationDscNodeConfiguration** parancsmag metaadatokat kap az APS-nek a kívánt állapot-konfiguráció (DSC) csomópont-konfigurációjában az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="ed03e-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="ed03e-110">Az automatizálás a DSC-csomópontok konfigurációját a Managed Object Format (MOF) konfigurációs dokumentumként tárolja.</span><span class="sxs-lookup"><span data-stu-id="ed03e-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="ed03e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ed03e-111">EXAMPLES</span></span>

### <span data-ttu-id="ed03e-112">1. példa: az összes DSC csomópont-konfiguráció beolvasása</span><span class="sxs-lookup"><span data-stu-id="ed03e-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="ed03e-113">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC csomópont-konfigurációjának metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ed03e-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="ed03e-114">2. példa: az összes DSC csomópont-konfiguráció beolvasása DSC-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="ed03e-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="ed03e-115">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC csomópont-konfigurációjának metaadatait kapja meg, hogy az ContosoConfiguration nevű DSC-konfigurációt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ed03e-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="ed03e-116">Példa 3: DSC csomópont-konfiguráció beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="ed03e-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="ed03e-117">Ez a parancs a DSC csomópontok konfigurációjának metaadatait a Contoso17 nevű automatizálási fiók ContosoConfiguration. webszerver segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ed03e-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ed03e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed03e-118">PARAMETERS</span></span>

### <span data-ttu-id="ed03e-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed03e-119">-AutomationAccountName</span></span>
<span data-ttu-id="ed03e-120">Megadja annak az automatizálási fióknak a nevét, amely tartalmazza azokat a DSC csomópont-konfigurációkat, amelyekhez a parancsmag metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="ed03e-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="ed03e-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ed03e-121">-ConfigurationName</span></span>
<span data-ttu-id="ed03e-122">Annak a DSC-konfigurációnak a nevét adja meg, amelyhez ez a parancsmag a Node Configuration metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="ed03e-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed03e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed03e-123">-DefaultProfile</span></span>
<span data-ttu-id="ed03e-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ed03e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed03e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ed03e-125">-Name</span></span>
<span data-ttu-id="ed03e-126">Annak a DSC-csomópontnak a neve, amelyhez a parancsmag metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="ed03e-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed03e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed03e-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed03e-128">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed03e-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ed03e-129">Ez a parancsmag a DSC csomópontok konfigurációjának metaadatait adja meg abban az erőforráscsoport-konfigurációban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="ed03e-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed03e-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="ed03e-130">-RollupStatus</span></span>
<span data-ttu-id="ed03e-131">A parancsmag által beolvasott DSC csomópont-konfigurációk összesítő állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ed03e-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="ed03e-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ed03e-132">Valid values are:</span></span> 
- <span data-ttu-id="ed03e-133">rossz</span><span class="sxs-lookup"><span data-stu-id="ed03e-133">Bad</span></span> 
- <span data-ttu-id="ed03e-134">jó</span><span class="sxs-lookup"><span data-stu-id="ed03e-134">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed03e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed03e-135">CommonParameters</span></span>
<span data-ttu-id="ed03e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed03e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed03e-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed03e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed03e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed03e-138">INPUTS</span></span>

### <span data-ttu-id="ed03e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ed03e-139">System.String</span></span>

## <span data-ttu-id="ed03e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed03e-140">OUTPUTS</span></span>

### <span data-ttu-id="ed03e-141">Microsoft. Azure. Command. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="ed03e-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="ed03e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed03e-142">NOTES</span></span>

## <span data-ttu-id="ed03e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed03e-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed03e-144">Importálás – AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed03e-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


