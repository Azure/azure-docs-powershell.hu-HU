---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168410"
---
# <span data-ttu-id="91ca5-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="91ca5-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="91ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="91ca5-103">Metaadatokat kap a DSC-csomópontok automatizálási konfigurációihoz.</span><span class="sxs-lookup"><span data-stu-id="91ca5-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="91ca5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91ca5-104">SYNTAX</span></span>

### <span data-ttu-id="91ca5-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91ca5-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91ca5-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="91ca5-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91ca5-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="91ca5-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91ca5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91ca5-108">DESCRIPTION</span></span>
<span data-ttu-id="91ca5-109">A **Get-AzAutomationDscNodeConfiguration** parancsmag metaadatokat kap az APS kívánt állapotkonfigurációs (DSC) csomópont-konfigurációihoz az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="91ca5-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="91ca5-110">Az automatizálás a DSC-csomópont konfigurációját Felügyelt objektumformátum (MOF) konfigurációs dokumentumként tárolja.</span><span class="sxs-lookup"><span data-stu-id="91ca5-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="91ca5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91ca5-111">EXAMPLES</span></span>

### <span data-ttu-id="91ca5-112">1. példa: Az összes DSC-csomópont konfigurálása</span><span class="sxs-lookup"><span data-stu-id="91ca5-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="91ca5-113">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók DSC-csomópont-konfigurációihoz.</span><span class="sxs-lookup"><span data-stu-id="91ca5-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="91ca5-114">2. példa: A DSC-konfigurációk összes DSC-csomópontjának konfigurálása</span><span class="sxs-lookup"><span data-stu-id="91ca5-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="91ca5-115">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes olyan DSC-konfigurálásához, amelynél a ContosoConfiguration nevű DSC-konfiguráció létre van hozva.</span><span class="sxs-lookup"><span data-stu-id="91ca5-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="91ca5-116">3. példa: DSC-csomópont konfigurációjának beállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="91ca5-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="91ca5-117">Ez a parancs metaadatokat kap egy ContosoConfiguration.webserver nevű DSC-csomópont-konfigurációhoz a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="91ca5-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="91ca5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91ca5-118">PARAMETERS</span></span>

### <span data-ttu-id="91ca5-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="91ca5-119">-AutomationAccountName</span></span>
<span data-ttu-id="91ca5-120">Annak az automatizálási fióknak a nevét adja meg, amely tartalmazza azokat a DSC-csomópont-konfigurációkat, amelyekhez a parancsmag metaadatokat kap.</span><span class="sxs-lookup"><span data-stu-id="91ca5-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="91ca5-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="91ca5-121">-ConfigurationName</span></span>
<span data-ttu-id="91ca5-122">Megadja annak a DSC-konfigurációnak a nevét, amelynek a parancsmagja csomópontkonfigurációs metaadatokat kap.</span><span class="sxs-lookup"><span data-stu-id="91ca5-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="91ca5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ca5-123">-DefaultProfile</span></span>
<span data-ttu-id="91ca5-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="91ca5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91ca5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="91ca5-125">-Name</span></span>
<span data-ttu-id="91ca5-126">Annak a DSC-csomópont-konfigurációnak a neve, amelyhez a parancsmag metaadatokat kap.</span><span class="sxs-lookup"><span data-stu-id="91ca5-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="91ca5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ca5-127">-ResourceGroupName</span></span>
<span data-ttu-id="91ca5-128">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91ca5-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="91ca5-129">Ez a parancsmag metaadatokat kap a DSC-csomópontok konfigurációihoz a paraméter által megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="91ca5-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="91ca5-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="91ca5-130">-RollupStatus</span></span>
<span data-ttu-id="91ca5-131">A parancsmag által lekért DSC-csomópontkonfigurációk összegző állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91ca5-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="91ca5-132">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="91ca5-132">Valid values are:</span></span> 
- <span data-ttu-id="91ca5-133">rossz</span><span class="sxs-lookup"><span data-stu-id="91ca5-133">Bad</span></span> 
- <span data-ttu-id="91ca5-134">jó</span><span class="sxs-lookup"><span data-stu-id="91ca5-134">Good</span></span>

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

### <span data-ttu-id="91ca5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ca5-135">CommonParameters</span></span>
<span data-ttu-id="91ca5-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ca5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ca5-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ca5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ca5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91ca5-138">INPUTS</span></span>

### <span data-ttu-id="91ca5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="91ca5-139">System.String</span></span>

## <span data-ttu-id="91ca5-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91ca5-140">OUTPUTS</span></span>

### <span data-ttu-id="91ca5-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="91ca5-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="91ca5-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91ca5-142">NOTES</span></span>

## <span data-ttu-id="91ca5-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91ca5-143">RELATED LINKS</span></span>

[<span data-ttu-id="91ca5-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="91ca5-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


