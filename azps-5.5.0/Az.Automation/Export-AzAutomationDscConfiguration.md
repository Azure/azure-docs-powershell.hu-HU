---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164355"
---
# <span data-ttu-id="1ab26-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ab26-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="1ab26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ab26-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab26-103">DSC-konfiguráció exportálása az automatizálásból egy helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="1ab26-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="1ab26-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ab26-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ab26-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ab26-105">DESCRIPTION</span></span>
<span data-ttu-id="1ab26-106">Az **Export-AzAutomationDscConfiguration** parancsmag egy APS–kívánt államkonfigurációs (DSC) konfigurációt exportál az Azure Automationből egy helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="1ab26-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="1ab26-107">Az exportált fájl kiterjesztése .ps1.</span><span class="sxs-lookup"><span data-stu-id="1ab26-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="1ab26-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ab26-108">EXAMPLES</span></span>

### <span data-ttu-id="1ab26-109">1. példa: DSC-konfiguráció közzétett verziójának exportálása</span><span class="sxs-lookup"><span data-stu-id="1ab26-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="1ab26-110">Ez a parancs exportálja egy DSC-konfiguráció közzétett verzióját az Automatizálásban a megadott mappába, azaz az asztalra.</span><span class="sxs-lookup"><span data-stu-id="1ab26-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="1ab26-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ab26-111">PARAMETERS</span></span>

### <span data-ttu-id="1ab26-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ab26-112">-AutomationAccountName</span></span>
<span data-ttu-id="1ab26-113">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által exportálni kívánt DSC-t tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1ab26-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="1ab26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab26-114">-DefaultProfile</span></span>
<span data-ttu-id="1ab26-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1ab26-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ab26-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1ab26-116">-Force</span></span>
<span data-ttu-id="1ab26-117">Azt jelzi, hogy ez a parancsmag lecserél egy meglévő helyi fájlt egy új, azonos nevű fájlra.</span><span class="sxs-lookup"><span data-stu-id="1ab26-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="1ab26-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1ab26-118">-Name</span></span>
<span data-ttu-id="1ab26-119">Annak a DSC-konfigurációnak a nevét adja meg, amely exportálja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1ab26-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="1ab26-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1ab26-120">-OutputFolder</span></span>
<span data-ttu-id="1ab26-121">Azt a kimeneti mappát adja meg, amelybe a parancsmag exportálja a DSC-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="1ab26-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="1ab26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab26-122">-ResourceGroupName</span></span>
<span data-ttu-id="1ab26-123">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja DSC-konfigurációt exportál.</span><span class="sxs-lookup"><span data-stu-id="1ab26-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="1ab26-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="1ab26-124">-Slot</span></span>
<span data-ttu-id="1ab26-125">Megadja, hogy a parancsmag a DSC-konfiguráció melyik verzióját exportálja.</span><span class="sxs-lookup"><span data-stu-id="1ab26-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="1ab26-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="1ab26-126">Valid values are:</span></span> 
- <span data-ttu-id="1ab26-127">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="1ab26-127">Draft</span></span>
- <span data-ttu-id="1ab26-128">Közzétéve: Az alapértelmezett érték Közzétéve.</span><span class="sxs-lookup"><span data-stu-id="1ab26-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="1ab26-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ab26-129">-Confirm</span></span>
<span data-ttu-id="1ab26-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ab26-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ab26-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ab26-131">-WhatIf</span></span>
<span data-ttu-id="1ab26-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ab26-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ab26-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ab26-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ab26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab26-134">CommonParameters</span></span>
<span data-ttu-id="1ab26-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ab26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab26-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ab26-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab26-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ab26-137">INPUTS</span></span>

### <span data-ttu-id="1ab26-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1ab26-138">System.String</span></span>

## <span data-ttu-id="1ab26-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ab26-139">OUTPUTS</span></span>

### <span data-ttu-id="1ab26-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1ab26-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="1ab26-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ab26-141">NOTES</span></span>

## <span data-ttu-id="1ab26-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ab26-142">RELATED LINKS</span></span>

[<span data-ttu-id="1ab26-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ab26-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="1ab26-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ab26-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


