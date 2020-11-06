---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2cd60a70b057689cf7edf154df28253b86e110a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497939"
---
# <span data-ttu-id="9d6dd-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d6dd-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="9d6dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="9d6dd-103">Az automatizálásból eltávolítja a DSC-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d6dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d6dd-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d6dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="9d6dd-106">A **Remove-AzureRmAutomationDscConfiguration** parancsmag az Azure automatizálási beállításainak (DSC) megfelelő konfigurációját távolítja el.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="9d6dd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d6dd-107">EXAMPLES</span></span>

## <span data-ttu-id="9d6dd-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d6dd-108">PARAMETERS</span></span>

### <span data-ttu-id="9d6dd-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d6dd-109">-AutomationAccountName</span></span>
<span data-ttu-id="9d6dd-110">Megadja annak az automatizálási fióknak a nevét, amely a parancsmag által eltávolított DSC-beállításokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9d6dd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9d6dd-111">-Force</span></span>
<span data-ttu-id="9d6dd-112">ps_force</span><span class="sxs-lookup"><span data-stu-id="9d6dd-112">ps_force</span></span>

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

### <span data-ttu-id="9d6dd-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d6dd-113">-Name</span></span>
<span data-ttu-id="9d6dd-114">Annak a DSC-konfigurációnak a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-114">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9d6dd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d6dd-115">-ResourceGroupName</span></span>
<span data-ttu-id="9d6dd-116">Annak a csoportnak a neve, amelyhez ez a parancsmag DSC-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-116">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="9d6dd-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d6dd-117">-Confirm</span></span>
<span data-ttu-id="9d6dd-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d6dd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d6dd-119">-WhatIf</span></span>
<span data-ttu-id="9d6dd-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d6dd-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d6dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d6dd-122">-DefaultProfile</span></span>
<span data-ttu-id="9d6dd-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d6dd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d6dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d6dd-124">CommonParameters</span></span>
<span data-ttu-id="9d6dd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d6dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d6dd-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d6dd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d6dd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d6dd-127">INPUTS</span></span>

## <span data-ttu-id="9d6dd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d6dd-128">OUTPUTS</span></span>

## <span data-ttu-id="9d6dd-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d6dd-129">NOTES</span></span>

## <span data-ttu-id="9d6dd-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d6dd-130">RELATED LINKS</span></span>

[<span data-ttu-id="9d6dd-131">Exportálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d6dd-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9d6dd-132">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d6dd-132">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9d6dd-133">Importálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d6dd-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


