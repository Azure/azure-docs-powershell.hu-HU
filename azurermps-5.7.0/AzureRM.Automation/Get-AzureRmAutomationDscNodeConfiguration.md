---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: b0fbea9b12fb8fbb76d0f5e8fd34efba4949acb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680826"
---
# <span data-ttu-id="d5f65-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5f65-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="d5f65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5f65-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f65-103">A DSC csomópont-konfigurációk metaadatait kapja az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="d5f65-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5f65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5f65-104">SYNTAX</span></span>

### <span data-ttu-id="d5f65-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5f65-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f65-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d5f65-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f65-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d5f65-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5f65-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5f65-108">DESCRIPTION</span></span>
<span data-ttu-id="d5f65-109">A **Get-AzureRmAutomationDscNodeConfiguration** parancsmag metaadatokat kap az APS-nek a kívánt állapot-konfiguráció (DSC) csomópont-konfigurációjában az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="d5f65-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="d5f65-110">Az automatizálás a DSC-csomópontok konfigurációját a Managed Object Format (MOF) konfigurációs dokumentumként tárolja.</span><span class="sxs-lookup"><span data-stu-id="d5f65-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="d5f65-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d5f65-111">EXAMPLES</span></span>

### <span data-ttu-id="d5f65-112">1. példa: az összes DSC csomópont-konfiguráció beolvasása</span><span class="sxs-lookup"><span data-stu-id="d5f65-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d5f65-113">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC csomópont-konfigurációjának metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="d5f65-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d5f65-114">2. példa: az összes DSC csomópont-konfiguráció beolvasása DSC-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d5f65-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="d5f65-115">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC csomópont-konfigurációjának metaadatait kapja meg, hogy az ContosoConfiguration nevű DSC-konfigurációt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d5f65-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="d5f65-116">Példa 3: DSC csomópont-konfiguráció beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="d5f65-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="d5f65-117">Ez a parancs a DSC csomópontok konfigurációjának metaadatait a Contoso17 nevű automatizálási fiók ContosoConfiguration. webszerver segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5f65-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d5f65-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5f65-118">PARAMETERS</span></span>

### <span data-ttu-id="d5f65-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d5f65-119">-AutomationAccountName</span></span>
<span data-ttu-id="d5f65-120">Megadja annak az automatizálási fióknak a nevét, amely tartalmazza azokat a DSC csomópont-konfigurációkat, amelyekhez a parancsmag metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="d5f65-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f65-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d5f65-121">-ConfigurationName</span></span>
<span data-ttu-id="d5f65-122">Annak a DSC-konfigurációnak a nevét adja meg, amelyhez ez a parancsmag a Node Configuration metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="d5f65-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f65-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f65-123">-DefaultProfile</span></span>
<span data-ttu-id="d5f65-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d5f65-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f65-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5f65-125">-Name</span></span>
<span data-ttu-id="d5f65-126">Annak a DSC-csomópontnak a neve, amelyhez a parancsmag metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="d5f65-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f65-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f65-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5f65-128">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5f65-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d5f65-129">Ez a parancsmag a DSC csomópontok konfigurációjának metaadatait adja meg abban az erőforráscsoport-konfigurációban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="d5f65-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f65-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="d5f65-130">-RollupStatus</span></span>
<span data-ttu-id="d5f65-131">A parancsmag által beolvasott DSC csomópont-konfigurációk összesítő állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5f65-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="d5f65-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d5f65-132">Valid values are:</span></span> 

- <span data-ttu-id="d5f65-133">rossz</span><span class="sxs-lookup"><span data-stu-id="d5f65-133">Bad</span></span> 
- <span data-ttu-id="d5f65-134">jó</span><span class="sxs-lookup"><span data-stu-id="d5f65-134">Good</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f65-135">CommonParameters</span></span>
<span data-ttu-id="d5f65-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5f65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f65-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f65-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f65-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f65-138">INPUTS</span></span>

### <span data-ttu-id="d5f65-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="d5f65-139">None</span></span>
<span data-ttu-id="d5f65-140">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d5f65-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d5f65-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f65-141">OUTPUTS</span></span>

### <span data-ttu-id="d5f65-142">Microsoft. Azure. Command. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="d5f65-142">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="d5f65-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5f65-143">NOTES</span></span>

## <span data-ttu-id="d5f65-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5f65-144">RELATED LINKS</span></span>

[<span data-ttu-id="d5f65-145">Importálás – AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5f65-145">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


