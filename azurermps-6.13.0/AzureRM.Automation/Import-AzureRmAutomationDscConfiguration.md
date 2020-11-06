---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 98e7875297e55660615607eef91c4187e8144fa1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498503"
---
# <span data-ttu-id="16410-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="16410-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="16410-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16410-102">SYNOPSIS</span></span>
<span data-ttu-id="16410-103">A DSC-konfiguráció importálása automatizálásra</span><span class="sxs-lookup"><span data-stu-id="16410-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16410-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16410-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16410-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16410-105">DESCRIPTION</span></span>
<span data-ttu-id="16410-106">Az **import-AzureRmAutomationDscConfiguration** PARANCSMAG az APS-alapú szükséges állapot-konfigurációs (DSC) konfigurációt importálja az Azure automatizálási szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="16410-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="16410-107">Adja meg egy olyan APS-parancsfájl elérési útját, amely egyetlen DSC-konfigurációt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="16410-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="16410-108">Példák</span><span class="sxs-lookup"><span data-stu-id="16410-108">EXAMPLES</span></span>

### <span data-ttu-id="16410-109">1. példa: DSC-konfiguráció importálása automatizálásra</span><span class="sxs-lookup"><span data-stu-id="16410-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="16410-110">Ez a parancs importálja a DSC konfigurációt a client.ps1 nevű fájlban a Contoso17 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="16410-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="16410-111">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="16410-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="16410-112">Ha van egy meglévő DSC-konfiguráció, az azt jelenti, hogy a parancs felülírja.</span><span class="sxs-lookup"><span data-stu-id="16410-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="16410-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16410-113">PARAMETERS</span></span>

### <span data-ttu-id="16410-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="16410-114">-AutomationAccountName</span></span>
<span data-ttu-id="16410-115">Annak az automatizálási fióknak a neve, amelybe a parancsmag DSC-konfigurációt importál.</span><span class="sxs-lookup"><span data-stu-id="16410-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="16410-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16410-116">-DefaultProfile</span></span>
<span data-ttu-id="16410-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16410-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16410-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="16410-118">-Description</span></span>
<span data-ttu-id="16410-119">A parancsmag által importált konfiguráció leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="16410-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="16410-120">-Force</span><span class="sxs-lookup"><span data-stu-id="16410-120">-Force</span></span>
<span data-ttu-id="16410-121">Azt jelzi, hogy ez a parancsmag egy meglévő DSC-konfigurációt cserél az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="16410-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="16410-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="16410-122">-LogVerbose</span></span>
<span data-ttu-id="16410-123">Megadja, hogy ez a parancsmag a DSC-konfiguráció összeállításakor a részletes naplózást be-vagy kikapcsolja.</span><span class="sxs-lookup"><span data-stu-id="16410-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="16410-124">Adja meg az $True értékét, ha be szeretné kapcsolni a részletes naplózást, vagy $False a funkció kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="16410-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16410-125">Által közzétett</span><span class="sxs-lookup"><span data-stu-id="16410-125">-Published</span></span>
<span data-ttu-id="16410-126">Jelzi, hogy ez a parancsmag a DSC-konfigurációt importálja a közzétett állapotba.</span><span class="sxs-lookup"><span data-stu-id="16410-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="16410-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16410-127">-ResourceGroupName</span></span>
<span data-ttu-id="16410-128">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag DSC-konfigurációt importál.</span><span class="sxs-lookup"><span data-stu-id="16410-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="16410-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="16410-129">-SourcePath</span></span>
<span data-ttu-id="16410-130">A parancsmag által importált DSC-konfigurációt tartalmazó wps_2 parancsfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16410-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16410-131">-Címkék</span><span class="sxs-lookup"><span data-stu-id="16410-131">-Tags</span></span>
<span data-ttu-id="16410-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="16410-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="16410-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="16410-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16410-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="16410-134">-Confirm</span></span>
<span data-ttu-id="16410-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="16410-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16410-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16410-136">-WhatIf</span></span>
<span data-ttu-id="16410-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="16410-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16410-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="16410-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16410-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16410-139">CommonParameters</span></span>
<span data-ttu-id="16410-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16410-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16410-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16410-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16410-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16410-142">INPUTS</span></span>

### <span data-ttu-id="16410-143">System. String</span><span class="sxs-lookup"><span data-stu-id="16410-143">System.String</span></span>

### <span data-ttu-id="16410-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="16410-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="16410-145">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="16410-145">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="16410-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16410-146">OUTPUTS</span></span>

### <span data-ttu-id="16410-147">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="16410-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="16410-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16410-148">NOTES</span></span>

## <span data-ttu-id="16410-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16410-149">RELATED LINKS</span></span>

[<span data-ttu-id="16410-150">Exportálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="16410-150">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="16410-151">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="16410-151">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
