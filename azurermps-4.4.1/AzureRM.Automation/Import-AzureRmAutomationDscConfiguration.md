---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497971"
---
# <span data-ttu-id="3b040-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b040-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="3b040-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b040-102">SYNOPSIS</span></span>
<span data-ttu-id="3b040-103">A DSC-konfiguráció importálása automatizálásra</span><span class="sxs-lookup"><span data-stu-id="3b040-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b040-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b040-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b040-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b040-105">DESCRIPTION</span></span>
<span data-ttu-id="3b040-106">Az **import-AzureRmAutomationDscConfiguration** PARANCSMAG az APS-alapú szükséges állapot-konfigurációs (DSC) konfigurációt importálja az Azure automatizálási szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="3b040-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="3b040-107">Adja meg egy olyan APS-parancsfájl elérési útját, amely egyetlen DSC-konfigurációt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3b040-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="3b040-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3b040-108">EXAMPLES</span></span>

### <span data-ttu-id="3b040-109">1. példa: DSC-konfiguráció importálása automatizálásra</span><span class="sxs-lookup"><span data-stu-id="3b040-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="3b040-110">Ez a parancs importálja a DSC konfigurációt a client.ps1 nevű fájlban a Contoso17 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="3b040-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="3b040-111">A parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b040-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="3b040-112">Ha van egy meglévő DSC-konfiguráció, az azt jelenti, hogy a parancs felülírja.</span><span class="sxs-lookup"><span data-stu-id="3b040-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="3b040-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b040-113">PARAMETERS</span></span>

### <span data-ttu-id="3b040-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3b040-114">-AutomationAccountName</span></span>
<span data-ttu-id="3b040-115">Annak az automatizálási fióknak a neve, amelybe a parancsmag DSC-konfigurációt importál.</span><span class="sxs-lookup"><span data-stu-id="3b040-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="3b040-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3b040-116">-Description</span></span>
<span data-ttu-id="3b040-117">A parancsmag által importált konfiguráció leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b040-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="3b040-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3b040-118">-Force</span></span>
<span data-ttu-id="3b040-119">Azt jelzi, hogy ez a parancsmag egy meglévő DSC-konfigurációt cserél az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="3b040-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="3b040-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="3b040-120">-LogVerbose</span></span>
<span data-ttu-id="3b040-121">Megadja, hogy ez a parancsmag a DSC-konfiguráció összeállításakor a részletes naplózást be-vagy kikapcsolja.</span><span class="sxs-lookup"><span data-stu-id="3b040-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="3b040-122">Adja meg az $True értékét, ha be szeretné kapcsolni a részletes naplózást, vagy $False a funkció kikapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="3b040-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="3b040-123">Által közzétett</span><span class="sxs-lookup"><span data-stu-id="3b040-123">-Published</span></span>
<span data-ttu-id="3b040-124">Jelzi, hogy ez a parancsmag a DSC-konfigurációt importálja a közzétett állapotba.</span><span class="sxs-lookup"><span data-stu-id="3b040-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="3b040-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b040-125">-ResourceGroupName</span></span>
<span data-ttu-id="3b040-126">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag DSC-konfigurációt importál.</span><span class="sxs-lookup"><span data-stu-id="3b040-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="3b040-127">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="3b040-127">-SourcePath</span></span>
<span data-ttu-id="3b040-128">A parancsmag által importált DSC-konfigurációt tartalmazó wps_2 parancsfájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b040-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="3b040-129">-Címkék</span><span class="sxs-lookup"><span data-stu-id="3b040-129">-Tags</span></span>
<span data-ttu-id="3b040-130">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3b040-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3b040-131">Példa:</span><span class="sxs-lookup"><span data-stu-id="3b040-131">For example:</span></span>

<span data-ttu-id="3b040-132">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3b040-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3b040-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b040-133">-Confirm</span></span>
<span data-ttu-id="3b040-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b040-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b040-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b040-135">-WhatIf</span></span>
<span data-ttu-id="3b040-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b040-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b040-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b040-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b040-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b040-138">-DefaultProfile</span></span>
<span data-ttu-id="3b040-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b040-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b040-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b040-140">CommonParameters</span></span>
<span data-ttu-id="3b040-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b040-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b040-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b040-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b040-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b040-143">INPUTS</span></span>

## <span data-ttu-id="3b040-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b040-144">OUTPUTS</span></span>

### <span data-ttu-id="3b040-145">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b040-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="3b040-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b040-146">NOTES</span></span>

## <span data-ttu-id="3b040-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b040-147">RELATED LINKS</span></span>

[<span data-ttu-id="3b040-148">Exportálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b040-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="3b040-149">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b040-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
