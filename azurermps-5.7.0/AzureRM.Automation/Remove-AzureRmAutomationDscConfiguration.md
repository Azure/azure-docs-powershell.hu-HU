---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: c328dcbf912b5b907f0e27c902bc7eb3dc31a44e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493280"
---
# <span data-ttu-id="acc4b-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="acc4b-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="acc4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="acc4b-103">Az automatizálásból eltávolítja a DSC-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="acc4b-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acc4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acc4b-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acc4b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="acc4b-105">DESCRIPTION</span></span>
<span data-ttu-id="acc4b-106">A **Remove-AzureRmAutomationDscConfiguration** parancsmag az Azure automatizálási beállításainak (DSC) megfelelő konfigurációját távolítja el.</span><span class="sxs-lookup"><span data-stu-id="acc4b-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="acc4b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="acc4b-107">EXAMPLES</span></span>

## <span data-ttu-id="acc4b-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acc4b-108">PARAMETERS</span></span>

### <span data-ttu-id="acc4b-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="acc4b-109">-AutomationAccountName</span></span>
<span data-ttu-id="acc4b-110">Megadja annak az automatizálási fióknak a nevét, amely a parancsmag által eltávolított DSC-beállításokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="acc4b-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="acc4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc4b-111">-DefaultProfile</span></span>
<span data-ttu-id="acc4b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="acc4b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acc4b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="acc4b-113">-Force</span></span>
<span data-ttu-id="acc4b-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="acc4b-114">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acc4b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="acc4b-115">-Name</span></span>
<span data-ttu-id="acc4b-116">Annak a DSC-konfigurációnak a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="acc4b-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acc4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="acc4b-118">Annak a csoportnak a neve, amelyhez ez a parancsmag DSC-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="acc4b-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="acc4b-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="acc4b-119">-Confirm</span></span>
<span data-ttu-id="acc4b-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="acc4b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc4b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc4b-121">-WhatIf</span></span>
<span data-ttu-id="acc4b-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="acc4b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acc4b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="acc4b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc4b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc4b-124">CommonParameters</span></span>
<span data-ttu-id="acc4b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acc4b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc4b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc4b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc4b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acc4b-127">INPUTS</span></span>

### <span data-ttu-id="acc4b-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="acc4b-128">None</span></span>
<span data-ttu-id="acc4b-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="acc4b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acc4b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acc4b-130">OUTPUTS</span></span>

## <span data-ttu-id="acc4b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acc4b-131">NOTES</span></span>

## <span data-ttu-id="acc4b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acc4b-132">RELATED LINKS</span></span>

[<span data-ttu-id="acc4b-133">Exportálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="acc4b-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="acc4b-134">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="acc4b-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="acc4b-135">Importálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="acc4b-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


