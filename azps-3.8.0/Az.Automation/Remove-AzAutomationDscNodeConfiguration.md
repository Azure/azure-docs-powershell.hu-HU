---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 28add3b4bffe808be5391de3ddbac759c36f5820
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014932"
---
# <span data-ttu-id="b031f-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b031f-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="b031f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b031f-102">SYNOPSIS</span></span>
<span data-ttu-id="b031f-103">Eltávolítja a metaadatokat a DSC csomópont-konfigurációból az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="b031f-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="b031f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b031f-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b031f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b031f-105">DESCRIPTION</span></span>
<span data-ttu-id="b031f-106">A **Remove-AzAutomationDscNodeConfiguration** parancsmag eltávolítja a metaadatokat az APS-től származó kívánt állapot-konfiguráció (DSC) csomópont-konfigurációkról az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="b031f-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="b031f-107">Az automatizálás a DSC-csomópontok konfigurációját a Managed Object Format (MOF) konfigurációs dokumentumként tárolja.</span><span class="sxs-lookup"><span data-stu-id="b031f-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="b031f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b031f-108">EXAMPLES</span></span>

## <span data-ttu-id="b031f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b031f-109">PARAMETERS</span></span>

### <span data-ttu-id="b031f-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b031f-110">-AutomationAccountName</span></span>
<span data-ttu-id="b031f-111">Megadja annak az automatizálási fióknak a nevét, amely tartalmazza azokat a DSC csomópont-konfigurációkat, amelyeknél ez a parancsmag eltávolítja a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="b031f-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="b031f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b031f-112">-DefaultProfile</span></span>
<span data-ttu-id="b031f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b031f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b031f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b031f-114">-Force</span></span>
<span data-ttu-id="b031f-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="b031f-115">ps_force</span></span>

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

### <span data-ttu-id="b031f-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="b031f-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="b031f-117">Azt jelzi, hogy ez a parancsmag figyelmen kívül hagyja a csomópontok megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="b031f-117">Indicates that this cmdlet ignores node mappings.</span></span>

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

### <span data-ttu-id="b031f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b031f-118">-Name</span></span>
<span data-ttu-id="b031f-119">Annak a DSC-csomópontnak a neve, amelyhez ez a parancsmag eltávolítja a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="b031f-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="b031f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b031f-120">-ResourceGroupName</span></span>
<span data-ttu-id="b031f-121">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b031f-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b031f-122">Ez a parancsmag eltávolítja a DSC csomópont-konfigurációk metaadatait abban az erőforráscsoport-konfigurációban, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b031f-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b031f-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b031f-123">-Confirm</span></span>
<span data-ttu-id="b031f-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b031f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b031f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b031f-125">-WhatIf</span></span>
<span data-ttu-id="b031f-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b031f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b031f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b031f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b031f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b031f-128">CommonParameters</span></span>
<span data-ttu-id="b031f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b031f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b031f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b031f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b031f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b031f-131">INPUTS</span></span>

### <span data-ttu-id="b031f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b031f-132">System.String</span></span>

## <span data-ttu-id="b031f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b031f-133">OUTPUTS</span></span>

### <span data-ttu-id="b031f-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="b031f-134">System.Void</span></span>

## <span data-ttu-id="b031f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b031f-135">NOTES</span></span>

## <span data-ttu-id="b031f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b031f-136">RELATED LINKS</span></span>

[<span data-ttu-id="b031f-137">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b031f-137">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="b031f-138">Importálás – AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b031f-138">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="b031f-139">Azure automatizálási parancsmagok</span><span class="sxs-lookup"><span data-stu-id="b031f-139">Azure Automation Cmdlets</span></span>](./Az.Automation.md)


