---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 9c3fd17454381cf17604eb430588255b4889b3cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497968"
---
# <span data-ttu-id="a1347-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1347-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="a1347-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1347-102">SYNOPSIS</span></span>
<span data-ttu-id="a1347-103">Egy MOF-dokumentumot importál a DSC csomópont-konfigurációba az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="a1347-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1347-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1347-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1347-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1347-105">DESCRIPTION</span></span>
<span data-ttu-id="a1347-106">Az **Importálás-AzureRmAutomationDscConfiguration** parancsmag a Managed Object Format (MOF) konfigurációs dokumentumot az Azure automatizálási szolgáltatásba importálja, mint a megfelelő állami konfigurációs (DSC) csomópontos konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="a1347-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="a1347-107">Adja meg a. MOF fájlok elérési útját.</span><span class="sxs-lookup"><span data-stu-id="a1347-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="a1347-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a1347-108">EXAMPLES</span></span>

### <span data-ttu-id="a1347-109">1. példa: DSC csomópont-konfiguráció importálása automatizálásra</span><span class="sxs-lookup"><span data-stu-id="a1347-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="a1347-110">Ez a parancs a DSC-csomópontok konfigurációját a webserver. MOF fájlból importálja a Contoso17 nevű automatizálási fiókba a DSC Configuration ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a1347-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="a1347-111">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1347-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a1347-112">Ha létezik egy ContosoConfiguration. webszerver nevű meglévő DSC csomópont-konfiguráció, akkor ez a parancs a helyére lép.</span><span class="sxs-lookup"><span data-stu-id="a1347-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="a1347-113">2. példa: DSC csomópont-konfiguráció importálása automatizálásra, és új verzió létrehozása, és nem a meglévő NodeConfiguration felülírása.</span><span class="sxs-lookup"><span data-stu-id="a1347-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="a1347-114">Ez a parancs a DSC-csomópontok konfigurációját a webserver. MOF fájlból importálja a Contoso17 nevű automatizálási fiókba a DSC Configuration ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a1347-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="a1347-115">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1347-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a1347-116">Ha létezik egy ContosoConfiguration. webszerver nevű meglévő DSC csomópont-konfiguráció, a parancs hozzáadja az új verzió-összeállítást a következő néven: ContosoConfiguration [2]. webkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="a1347-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="a1347-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1347-117">PARAMETERS</span></span>

### <span data-ttu-id="a1347-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1347-118">-AutomationAccountName</span></span>
<span data-ttu-id="a1347-119">Annak az automatizálási fióknak a neve, amelybe a parancsmag a DSC-csomópontok konfigurációját importálja.</span><span class="sxs-lookup"><span data-stu-id="a1347-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="a1347-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a1347-120">-ConfigurationName</span></span>
<span data-ttu-id="a1347-121">Az automatizáláshoz használt DSC-konfiguráció nevét adja meg az importálandó csomópont-konfiguráció névteréhez és tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="a1347-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="a1347-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a1347-122">-Force</span></span>
<span data-ttu-id="a1347-123">Azt jelzi, hogy ez a parancsmag egy meglévő DSC csomópont-konfigurációt cserél az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="a1347-123">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="a1347-124">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="a1347-124">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="a1347-125">Létrehoz egy új csomópont-konfiguráció-összeállítási verziót.</span><span class="sxs-lookup"><span data-stu-id="a1347-125">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="a1347-126">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a1347-126">-Path</span></span>
<span data-ttu-id="a1347-127">A parancsmag által importált MOF-konfigurációs dokumentum elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1347-127">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="a1347-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1347-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1347-129">Annak az erőforráscsoport a nevét adja meg, amelyhez ez a parancsmag a DSC csomópont konfigurációját importálja.</span><span class="sxs-lookup"><span data-stu-id="a1347-129">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="a1347-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1347-130">-Confirm</span></span>
<span data-ttu-id="a1347-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1347-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1347-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1347-132">-WhatIf</span></span>
<span data-ttu-id="a1347-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1347-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1347-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1347-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1347-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1347-135">-DefaultProfile</span></span>
<span data-ttu-id="a1347-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1347-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1347-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1347-137">CommonParameters</span></span>
<span data-ttu-id="a1347-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1347-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1347-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1347-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1347-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1347-140">INPUTS</span></span>

## <span data-ttu-id="a1347-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1347-141">OUTPUTS</span></span>

### <span data-ttu-id="a1347-142">Microsoft. Azure. Command. Automation. Model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1347-142">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="a1347-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1347-143">NOTES</span></span>

## <span data-ttu-id="a1347-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1347-144">RELATED LINKS</span></span>

[<span data-ttu-id="a1347-145">Exportálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1347-145">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="a1347-146">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1347-146">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)


