---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2f739c9471e2a6144c12033ade885a445bade12e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679902"
---
# <span data-ttu-id="70655-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="70655-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="70655-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70655-102">SYNOPSIS</span></span>
<span data-ttu-id="70655-103">DSC-konfiguráció exportálása Automatizálásról helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="70655-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70655-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70655-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70655-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70655-105">DESCRIPTION</span></span>
<span data-ttu-id="70655-106">Az **export-AzureRmAutomationDscConfiguration** parancsmag az Azure automatizálási beállításait egy helyi fájlba exportálja.</span><span class="sxs-lookup"><span data-stu-id="70655-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="70655-107">Az exportált fájl. ps1 fájlnévkiterjesztéssel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="70655-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="70655-108">Példák</span><span class="sxs-lookup"><span data-stu-id="70655-108">EXAMPLES</span></span>

### <span data-ttu-id="70655-109">1. példa: a DSC-konfiguráció közzétett verziójának exportálása</span><span class="sxs-lookup"><span data-stu-id="70655-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="70655-110">Ez a parancs a DSC-konfiguráció közzétett verzióját exportálja az automatizálási környezetbe a megadott mappába, amely az asztali számítógép.</span><span class="sxs-lookup"><span data-stu-id="70655-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="70655-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70655-111">PARAMETERS</span></span>

### <span data-ttu-id="70655-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70655-112">-AutomationAccountName</span></span>
<span data-ttu-id="70655-113">Annak az automatizálási fióknak a neve, amely a parancsmag által exportált DSC-t tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="70655-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="70655-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70655-114">-DefaultProfile</span></span>
<span data-ttu-id="70655-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="70655-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70655-116">-Force</span><span class="sxs-lookup"><span data-stu-id="70655-116">-Force</span></span>
<span data-ttu-id="70655-117">Azt jelzi, hogy ez a parancsmag egy meglévő helyi fájlt cserél le egy új, azonos nevű fájllal.</span><span class="sxs-lookup"><span data-stu-id="70655-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70655-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70655-118">-Name</span></span>
<span data-ttu-id="70655-119">A parancsmag által exportált DSC-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70655-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70655-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="70655-120">-OutputFolder</span></span>
<span data-ttu-id="70655-121">Azt a kimeneti mappát adja meg, ahol ez a parancsmag a DSC-konfigurációt exportálja.</span><span class="sxs-lookup"><span data-stu-id="70655-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70655-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70655-122">-ResourceGroupName</span></span>
<span data-ttu-id="70655-123">Annak az erőforráscsoport a nevét adja meg, amelyhez ez a parancsmag a DSC-konfigurációt exportálja.</span><span class="sxs-lookup"><span data-stu-id="70655-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="70655-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="70655-124">-Slot</span></span>
<span data-ttu-id="70655-125">Itt adhatja meg, hogy a DSC-konfiguráció melyik verziójával exportálja az adott parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70655-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="70655-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="70655-126">Valid values are:</span></span> 

- <span data-ttu-id="70655-127">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="70655-127">Draft</span></span>
- <span data-ttu-id="70655-128">Közzétett</span><span class="sxs-lookup"><span data-stu-id="70655-128">Published</span></span> 

<span data-ttu-id="70655-129">Az alapértelmezett érték jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="70655-129">The default value is Published.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70655-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70655-130">-Confirm</span></span>
<span data-ttu-id="70655-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70655-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70655-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70655-132">-WhatIf</span></span>
<span data-ttu-id="70655-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70655-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70655-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70655-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70655-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70655-135">CommonParameters</span></span>
<span data-ttu-id="70655-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70655-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70655-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70655-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70655-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70655-138">INPUTS</span></span>

### <span data-ttu-id="70655-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="70655-139">None</span></span>
<span data-ttu-id="70655-140">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="70655-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70655-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70655-141">OUTPUTS</span></span>

### <span data-ttu-id="70655-142">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="70655-142">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="70655-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70655-143">NOTES</span></span>

## <span data-ttu-id="70655-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70655-144">RELATED LINKS</span></span>

[<span data-ttu-id="70655-145">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="70655-145">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="70655-146">Importálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="70655-146">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


