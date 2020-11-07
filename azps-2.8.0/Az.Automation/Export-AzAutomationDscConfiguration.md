---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 8abd6859054245c6265cc32695fa56168aabd1c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667880"
---
# <span data-ttu-id="7e83c-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e83c-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="7e83c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e83c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e83c-103">DSC-konfiguráció exportálása Automatizálásról helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="7e83c-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="7e83c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e83c-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e83c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e83c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e83c-106">Az **export-AzAutomationDscConfiguration** parancsmag az Azure automatizálási beállításait egy helyi fájlba exportálja.</span><span class="sxs-lookup"><span data-stu-id="7e83c-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="7e83c-107">Az exportált fájl. ps1 fájlnévkiterjesztéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="7e83c-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="7e83c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7e83c-108">EXAMPLES</span></span>

### <span data-ttu-id="7e83c-109">1. példa: a DSC-konfiguráció közzétett verziójának exportálása</span><span class="sxs-lookup"><span data-stu-id="7e83c-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="7e83c-110">Ez a parancs a DSC-konfiguráció közzétett verzióját exportálja az automatizálási környezetbe a megadott mappába, amely az asztali számítógép.</span><span class="sxs-lookup"><span data-stu-id="7e83c-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="7e83c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e83c-111">PARAMETERS</span></span>

### <span data-ttu-id="7e83c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7e83c-112">-AutomationAccountName</span></span>
<span data-ttu-id="7e83c-113">Annak az automatizálási fióknak a neve, amely a parancsmag által exportált DSC-t tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7e83c-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="7e83c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e83c-114">-DefaultProfile</span></span>
<span data-ttu-id="7e83c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7e83c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e83c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7e83c-116">-Force</span></span>
<span data-ttu-id="7e83c-117">Azt jelzi, hogy ez a parancsmag egy meglévő helyi fájlt cserél le egy új, azonos nevű fájllal.</span><span class="sxs-lookup"><span data-stu-id="7e83c-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="7e83c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e83c-118">-Name</span></span>
<span data-ttu-id="7e83c-119">A parancsmag által exportált DSC-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e83c-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e83c-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="7e83c-120">-OutputFolder</span></span>
<span data-ttu-id="7e83c-121">Azt a kimeneti mappát adja meg, ahol ez a parancsmag a DSC-konfigurációt exportálja.</span><span class="sxs-lookup"><span data-stu-id="7e83c-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e83c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e83c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e83c-123">Annak az erőforráscsoport a nevét adja meg, amelyhez ez a parancsmag a DSC-konfigurációt exportálja.</span><span class="sxs-lookup"><span data-stu-id="7e83c-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="7e83c-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="7e83c-124">-Slot</span></span>
<span data-ttu-id="7e83c-125">Itt adhatja meg, hogy a DSC-konfiguráció melyik verziójával exportálja az adott parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7e83c-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="7e83c-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="7e83c-126">Valid values are:</span></span> 
- <span data-ttu-id="7e83c-127">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="7e83c-127">Draft</span></span>
- <span data-ttu-id="7e83c-128">Közzétette: az alapértelmezett érték közzé lett téve.</span><span class="sxs-lookup"><span data-stu-id="7e83c-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e83c-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e83c-129">-Confirm</span></span>
<span data-ttu-id="7e83c-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e83c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e83c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e83c-131">-WhatIf</span></span>
<span data-ttu-id="7e83c-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e83c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e83c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e83c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e83c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e83c-134">CommonParameters</span></span>
<span data-ttu-id="7e83c-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e83c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e83c-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e83c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e83c-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e83c-137">INPUTS</span></span>

### <span data-ttu-id="7e83c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7e83c-138">System.String</span></span>

## <span data-ttu-id="7e83c-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e83c-139">OUTPUTS</span></span>

### <span data-ttu-id="7e83c-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="7e83c-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="7e83c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e83c-141">NOTES</span></span>

## <span data-ttu-id="7e83c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e83c-142">RELATED LINKS</span></span>

[<span data-ttu-id="7e83c-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e83c-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="7e83c-144">Importálás – AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e83c-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


