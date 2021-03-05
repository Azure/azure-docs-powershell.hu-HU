---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3680d277addba29444f3f2955d7cca28505435a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014038"
---
# <span data-ttu-id="9c65b-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c65b-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="9c65b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c65b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c65b-103">MOF-dokumentumot importál DSC-csomópont-konfigurációként az Automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="9c65b-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="9c65b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c65b-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c65b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c65b-105">DESCRIPTION</span></span>
<span data-ttu-id="9c65b-106">Az **Import-AzAutomationDscConfiguration** parancsmag egy Felügyelt objektumformátum (MOF) konfigurációs dokumentumot importál az Azure Automation alkalmazásba kívánt állapotkonfiguráció (DSC) csomópont-konfigurációként.</span><span class="sxs-lookup"><span data-stu-id="9c65b-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="9c65b-107">Adja meg egy .mof fájl elérési útját.</span><span class="sxs-lookup"><span data-stu-id="9c65b-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="9c65b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c65b-108">EXAMPLES</span></span>

### <span data-ttu-id="9c65b-109">1. példa: DSC-csomópont konfigurációjának importálása az automatizálásba</span><span class="sxs-lookup"><span data-stu-id="9c65b-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="9c65b-110">Ez a parancs egy DSC-csomópont-konfigurációt importál a webserver.mof nevű fájlból a Contoso17 nevű automatizálási fiókba a ContosoConfiguration DSC-konfiguráció alatt.</span><span class="sxs-lookup"><span data-stu-id="9c65b-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="9c65b-111">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c65b-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9c65b-112">Ha létezik egy ContosoConfiguration.webserver nevű meglévő DSC-csomópont-konfiguráció, ez a parancs helyettesíti azt.</span><span class="sxs-lookup"><span data-stu-id="9c65b-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="9c65b-113">2. példa: DSC-csomópont konfigurációjának importálása az Automatizálásba, és hozzon létre egy új buildverziót, és ne írja felül a meglévő NodeConfigurációt.</span><span class="sxs-lookup"><span data-stu-id="9c65b-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="9c65b-114">Ez a parancs egy DSC-csomópont-konfigurációt importál a webserver.mof nevű fájlból a Contoso17 nevű automatizálási fiókba a ContosoConfiguration DSC-konfiguráció alatt.</span><span class="sxs-lookup"><span data-stu-id="9c65b-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="9c65b-115">A parancs a Force *paramétert* adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c65b-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9c65b-116">Ha létezik egy ContosoConfiguration.webserver nevű meglévő DSC-csomópont-konfiguráció, ez a parancs hozzáad egy új buildverziót ContosoConfiguration[2].webserver néven.</span><span class="sxs-lookup"><span data-stu-id="9c65b-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="9c65b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c65b-117">PARAMETERS</span></span>

### <span data-ttu-id="9c65b-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9c65b-118">-AutomationAccountName</span></span>
<span data-ttu-id="9c65b-119">Annak az automatizálási fióknak a nevét adja meg, amelybe ez a parancsmag egy DSC-csomópont-konfigurációt importál.</span><span class="sxs-lookup"><span data-stu-id="9c65b-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="9c65b-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9c65b-120">-ConfigurationName</span></span>
<span data-ttu-id="9c65b-121">Az Automatizálásban egy olyan DSC-konfiguráció nevét adja meg, amely az importálni szükséges csomópont-konfiguráció névtere és tárolója.</span><span class="sxs-lookup"><span data-stu-id="9c65b-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="9c65b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c65b-122">-DefaultProfile</span></span>
<span data-ttu-id="9c65b-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9c65b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c65b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9c65b-124">-Force</span></span>
<span data-ttu-id="9c65b-125">Azt jelzi, hogy ez a parancsmag lecserél egy meglévő DSC-csomópont-konfigurációt az Automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="9c65b-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c65b-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="9c65b-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="9c65b-127">Létrehozza a csomópont konfigurációjának új verzióját.</span><span class="sxs-lookup"><span data-stu-id="9c65b-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="9c65b-128">-Path</span><span class="sxs-lookup"><span data-stu-id="9c65b-128">-Path</span></span>
<span data-ttu-id="9c65b-129">Annak az MOF konfigurációs dokumentumnak az elérési útját adja meg, amelybe ez a parancsmag importálva van.</span><span class="sxs-lookup"><span data-stu-id="9c65b-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="9c65b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c65b-130">-ResourceGroupName</span></span>
<span data-ttu-id="9c65b-131">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja DSC-csomópont-konfigurációt importál.</span><span class="sxs-lookup"><span data-stu-id="9c65b-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="9c65b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c65b-132">-Confirm</span></span>
<span data-ttu-id="9c65b-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9c65b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c65b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c65b-134">-WhatIf</span></span>
<span data-ttu-id="9c65b-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9c65b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c65b-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c65b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c65b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c65b-137">CommonParameters</span></span>
<span data-ttu-id="9c65b-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c65b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c65b-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c65b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c65b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c65b-140">INPUTS</span></span>

### <span data-ttu-id="9c65b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9c65b-141">System.String</span></span>

## <span data-ttu-id="9c65b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c65b-142">OUTPUTS</span></span>

### <span data-ttu-id="9c65b-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c65b-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="9c65b-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c65b-144">NOTES</span></span>

## <span data-ttu-id="9c65b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c65b-145">RELATED LINKS</span></span>

[<span data-ttu-id="9c65b-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c65b-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="9c65b-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c65b-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)


