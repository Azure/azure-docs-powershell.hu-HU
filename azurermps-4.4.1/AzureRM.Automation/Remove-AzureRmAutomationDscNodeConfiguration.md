---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 56ceba33845061af4e0ccdf3247bab16e079e90c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497936"
---
# <span data-ttu-id="fc56f-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc56f-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="fc56f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc56f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc56f-103">Eltávolítja a metaadatokat a DSC csomópont-konfigurációból az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="fc56f-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc56f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc56f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc56f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc56f-105">DESCRIPTION</span></span>
<span data-ttu-id="fc56f-106">A **Remove-AzureRmAutomationDscNodeConfiguration** parancsmag eltávolítja a metaadatokat az APS-től származó kívánt állapot-konfiguráció (DSC) csomópont-konfigurációkról az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="fc56f-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="fc56f-107">Az automatizálás a DSC-csomópontok konfigurációját a Managed Object Format (MOF) konfigurációs dokumentumként tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc56f-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="fc56f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fc56f-108">EXAMPLES</span></span>

## <span data-ttu-id="fc56f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc56f-109">PARAMETERS</span></span>

### <span data-ttu-id="fc56f-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fc56f-110">-AutomationAccountName</span></span>
<span data-ttu-id="fc56f-111">Megadja annak az automatizálási fióknak a nevét, amely tartalmazza azokat a DSC csomópont-konfigurációkat, amelyeknél ez a parancsmag eltávolítja a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="fc56f-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="fc56f-112">-Force</span><span class="sxs-lookup"><span data-stu-id="fc56f-112">-Force</span></span>
<span data-ttu-id="fc56f-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="fc56f-113">ps_force</span></span>

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

### <span data-ttu-id="fc56f-114">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="fc56f-114">-IgnoreNodeMappings</span></span>
<span data-ttu-id="fc56f-115">Azt jelzi, hogy ez a parancsmag figyelmen kívül hagyja a csomópontok megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="fc56f-115">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc56f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc56f-116">-Name</span></span>
<span data-ttu-id="fc56f-117">Annak a DSC-csomópontnak a neve, amelyhez ez a parancsmag eltávolítja a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="fc56f-117">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc56f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc56f-118">-ResourceGroupName</span></span>
<span data-ttu-id="fc56f-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc56f-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fc56f-120">Ez a parancsmag eltávolítja a DSC csomópont-konfigurációk metaadatait abban az erőforráscsoport-konfigurációban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="fc56f-120">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc56f-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc56f-121">-Confirm</span></span>
<span data-ttu-id="fc56f-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc56f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc56f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc56f-123">-WhatIf</span></span>
<span data-ttu-id="fc56f-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc56f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc56f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc56f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc56f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc56f-126">-DefaultProfile</span></span>
<span data-ttu-id="fc56f-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc56f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc56f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc56f-128">CommonParameters</span></span>
<span data-ttu-id="fc56f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc56f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc56f-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc56f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc56f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc56f-131">INPUTS</span></span>

## <span data-ttu-id="fc56f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc56f-132">OUTPUTS</span></span>

## <span data-ttu-id="fc56f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc56f-133">NOTES</span></span>

## <span data-ttu-id="fc56f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc56f-134">RELATED LINKS</span></span>

[<span data-ttu-id="fc56f-135">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc56f-135">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="fc56f-136">Importálás – AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc56f-136">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="fc56f-137">Azure automatizálási parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fc56f-137">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


