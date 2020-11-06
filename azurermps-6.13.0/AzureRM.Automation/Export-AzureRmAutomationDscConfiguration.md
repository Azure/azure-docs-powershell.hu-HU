---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: f690e5d7e35b819b727e2ea3f12c8f5e0b2a375f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492055"
---
# <span data-ttu-id="b4143-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4143-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="b4143-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4143-102">SYNOPSIS</span></span>
<span data-ttu-id="b4143-103">DSC-konfiguráció exportálása Automatizálásról helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="b4143-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4143-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4143-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4143-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4143-105">DESCRIPTION</span></span>
<span data-ttu-id="b4143-106">Az **export-AzureRmAutomationDscConfiguration** parancsmag az Azure automatizálási beállításait egy helyi fájlba exportálja.</span><span class="sxs-lookup"><span data-stu-id="b4143-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="b4143-107">Az exportált fájl. ps1 fájlnévkiterjesztéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="b4143-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="b4143-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b4143-108">EXAMPLES</span></span>

### <span data-ttu-id="b4143-109">1. példa: a DSC-konfiguráció közzétett verziójának exportálása</span><span class="sxs-lookup"><span data-stu-id="b4143-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="b4143-110">Ez a parancs a DSC-konfiguráció közzétett verzióját exportálja az automatizálási környezetbe a megadott mappába, amely az asztali számítógép.</span><span class="sxs-lookup"><span data-stu-id="b4143-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="b4143-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4143-111">PARAMETERS</span></span>

### <span data-ttu-id="b4143-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b4143-112">-AutomationAccountName</span></span>
<span data-ttu-id="b4143-113">Annak az automatizálási fióknak a neve, amely a parancsmag által exportált DSC-t tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b4143-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="b4143-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4143-114">-DefaultProfile</span></span>
<span data-ttu-id="b4143-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b4143-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4143-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b4143-116">-Force</span></span>
<span data-ttu-id="b4143-117">Azt jelzi, hogy ez a parancsmag egy meglévő helyi fájlt cserél le egy új, azonos nevű fájllal.</span><span class="sxs-lookup"><span data-stu-id="b4143-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="b4143-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4143-118">-Name</span></span>
<span data-ttu-id="b4143-119">A parancsmag által exportált DSC-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4143-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="b4143-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="b4143-120">-OutputFolder</span></span>
<span data-ttu-id="b4143-121">Azt a kimeneti mappát adja meg, ahol ez a parancsmag a DSC-konfigurációt exportálja.</span><span class="sxs-lookup"><span data-stu-id="b4143-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="b4143-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4143-122">-ResourceGroupName</span></span>
<span data-ttu-id="b4143-123">Annak az erőforráscsoport a nevét adja meg, amelyhez ez a parancsmag a DSC-konfigurációt exportálja.</span><span class="sxs-lookup"><span data-stu-id="b4143-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="b4143-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="b4143-124">-Slot</span></span>
<span data-ttu-id="b4143-125">Itt adhatja meg, hogy a DSC-konfiguráció melyik verziójával exportálja az adott parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4143-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="b4143-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b4143-126">Valid values are:</span></span> 
- <span data-ttu-id="b4143-127">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="b4143-127">Draft</span></span>
- <span data-ttu-id="b4143-128">Közzétette: az alapértelmezett érték közzé lett téve.</span><span class="sxs-lookup"><span data-stu-id="b4143-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="b4143-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4143-129">-Confirm</span></span>
<span data-ttu-id="b4143-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4143-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4143-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4143-131">-WhatIf</span></span>
<span data-ttu-id="b4143-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4143-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4143-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4143-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4143-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4143-134">CommonParameters</span></span>
<span data-ttu-id="b4143-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4143-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4143-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4143-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4143-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4143-137">INPUTS</span></span>

### <span data-ttu-id="b4143-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b4143-138">System.String</span></span>

## <span data-ttu-id="b4143-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4143-139">OUTPUTS</span></span>

### <span data-ttu-id="b4143-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="b4143-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="b4143-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4143-141">NOTES</span></span>

## <span data-ttu-id="b4143-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4143-142">RELATED LINKS</span></span>

[<span data-ttu-id="b4143-143">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4143-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="b4143-144">Importálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4143-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


