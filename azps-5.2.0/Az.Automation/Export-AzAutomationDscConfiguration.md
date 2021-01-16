---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328435"
---
# <span data-ttu-id="f3045-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3045-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="f3045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3045-102">SYNOPSIS</span></span>
<span data-ttu-id="f3045-103">DSC-konfiguráció exportálása az automatizálásból egy helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="f3045-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="f3045-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3045-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3045-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3045-105">DESCRIPTION</span></span>
<span data-ttu-id="f3045-106">Az **Export-AzAutomationDscConfiguration** parancsmag egy APS–kívánt államkonfigurációs (DSC) konfigurációt exportál az Azure Automationből egy helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="f3045-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="f3045-107">Az exportált fájl kiterjesztése .ps1.</span><span class="sxs-lookup"><span data-stu-id="f3045-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="f3045-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3045-108">EXAMPLES</span></span>

### <span data-ttu-id="f3045-109">1. példa: DSC-konfiguráció közzétett verziójának exportálása</span><span class="sxs-lookup"><span data-stu-id="f3045-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="f3045-110">Ez a parancs exportálja egy DSC-konfiguráció közzétett verzióját az Automatizálásban a megadott mappába, amely az asztal.</span><span class="sxs-lookup"><span data-stu-id="f3045-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="f3045-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3045-111">PARAMETERS</span></span>

### <span data-ttu-id="f3045-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3045-112">-AutomationAccountName</span></span>
<span data-ttu-id="f3045-113">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által exportálni kívánt DSC-t tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f3045-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="f3045-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3045-114">-DefaultProfile</span></span>
<span data-ttu-id="f3045-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f3045-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3045-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f3045-116">-Force</span></span>
<span data-ttu-id="f3045-117">Azt jelzi, hogy ez a parancsmag lecserél egy meglévő helyi fájlt egy új, azonos nevű fájlra.</span><span class="sxs-lookup"><span data-stu-id="f3045-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="f3045-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f3045-118">-Name</span></span>
<span data-ttu-id="f3045-119">Annak a DSC-konfigurációnak a nevét adja meg, amely exportálja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f3045-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="f3045-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="f3045-120">-OutputFolder</span></span>
<span data-ttu-id="f3045-121">Azt a kimeneti mappát adja meg, amelybe a parancsmag exportálja a DSC-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f3045-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="f3045-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3045-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3045-123">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja DSC-konfigurációt exportál.</span><span class="sxs-lookup"><span data-stu-id="f3045-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="f3045-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="f3045-124">-Slot</span></span>
<span data-ttu-id="f3045-125">Megadja a DSC-konfigurációnak azt a verzióját, amelyet a parancsmag exportál.</span><span class="sxs-lookup"><span data-stu-id="f3045-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="f3045-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="f3045-126">Valid values are:</span></span> 
- <span data-ttu-id="f3045-127">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="f3045-127">Draft</span></span>
- <span data-ttu-id="f3045-128">Közzétéve: Az alapértelmezett érték Közzétéve.</span><span class="sxs-lookup"><span data-stu-id="f3045-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="f3045-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3045-129">-Confirm</span></span>
<span data-ttu-id="f3045-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3045-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3045-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3045-131">-WhatIf</span></span>
<span data-ttu-id="f3045-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3045-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3045-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3045-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3045-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3045-134">CommonParameters</span></span>
<span data-ttu-id="f3045-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3045-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3045-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3045-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3045-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3045-137">INPUTS</span></span>

### <span data-ttu-id="f3045-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f3045-138">System.String</span></span>

## <span data-ttu-id="f3045-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3045-139">OUTPUTS</span></span>

### <span data-ttu-id="f3045-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="f3045-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="f3045-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3045-141">NOTES</span></span>

## <span data-ttu-id="f3045-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3045-142">RELATED LINKS</span></span>

[<span data-ttu-id="f3045-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3045-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="f3045-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3045-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


