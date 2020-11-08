---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: bd418037f29aefc27d92ccebe1f34024728c77c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014934"
---
# <span data-ttu-id="14eec-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="14eec-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="14eec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14eec-102">SYNOPSIS</span></span>
<span data-ttu-id="14eec-103">Az automatizálásból eltávolítja a DSC-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="14eec-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="14eec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14eec-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14eec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14eec-105">DESCRIPTION</span></span>
<span data-ttu-id="14eec-106">A **Remove-AzAutomationDscConfiguration** parancsmag az Azure automatizálási beállításainak (DSC) megfelelő konfigurációját távolítja el.</span><span class="sxs-lookup"><span data-stu-id="14eec-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="14eec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="14eec-107">EXAMPLES</span></span>

## <span data-ttu-id="14eec-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14eec-108">PARAMETERS</span></span>

### <span data-ttu-id="14eec-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="14eec-109">-AutomationAccountName</span></span>
<span data-ttu-id="14eec-110">Megadja annak az automatizálási fióknak a nevét, amely a parancsmag által eltávolított DSC-beállításokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="14eec-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="14eec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14eec-111">-DefaultProfile</span></span>
<span data-ttu-id="14eec-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="14eec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14eec-113">-Force</span><span class="sxs-lookup"><span data-stu-id="14eec-113">-Force</span></span>
<span data-ttu-id="14eec-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="14eec-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14eec-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14eec-115">-Name</span></span>
<span data-ttu-id="14eec-116">Annak a DSC-konfigurációnak a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="14eec-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14eec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14eec-117">-ResourceGroupName</span></span>
<span data-ttu-id="14eec-118">Annak a csoportnak a neve, amelyhez ez a parancsmag DSC-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="14eec-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="14eec-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="14eec-119">-Confirm</span></span>
<span data-ttu-id="14eec-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="14eec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14eec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14eec-121">-WhatIf</span></span>
<span data-ttu-id="14eec-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="14eec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14eec-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="14eec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14eec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14eec-124">CommonParameters</span></span>
<span data-ttu-id="14eec-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14eec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14eec-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14eec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14eec-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14eec-127">INPUTS</span></span>

### <span data-ttu-id="14eec-128">System. String</span><span class="sxs-lookup"><span data-stu-id="14eec-128">System.String</span></span>

## <span data-ttu-id="14eec-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14eec-129">OUTPUTS</span></span>

### <span data-ttu-id="14eec-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="14eec-130">System.Void</span></span>

## <span data-ttu-id="14eec-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14eec-131">NOTES</span></span>

## <span data-ttu-id="14eec-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14eec-132">RELATED LINKS</span></span>

[<span data-ttu-id="14eec-133">Exportálás – AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="14eec-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="14eec-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="14eec-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="14eec-135">Importálás – AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="14eec-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


