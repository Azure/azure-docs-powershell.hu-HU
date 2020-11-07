---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: 663573e7f4e111880c5ed0014dcad18480f665ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672390"
---
# <span data-ttu-id="65860-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="65860-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="65860-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65860-102">SYNOPSIS</span></span>
<span data-ttu-id="65860-103">Módosítja a DSC-csomópont által megfeleltetett csomópont-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="65860-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65860-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65860-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65860-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65860-105">DESCRIPTION</span></span>
<span data-ttu-id="65860-106">A **set-AzureRmAutomationDscNode** parancsmag módosította az APS-alapú kívánt állapot-konfiguráció (DSC) csomópont-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="65860-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="65860-107">Az Azure Automation a DSC csomópontok konfigurációját a Managed Object Format (MOF) konfigurációs dokumentumként tárolja.</span><span class="sxs-lookup"><span data-stu-id="65860-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="65860-108">Példák</span><span class="sxs-lookup"><span data-stu-id="65860-108">EXAMPLES</span></span>

### <span data-ttu-id="65860-109">Példa 1: csomópont-konfiguráció megfeleltetésének módosítása</span><span class="sxs-lookup"><span data-stu-id="65860-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="65860-110">Ez a parancs a contoso. NodeConfiguration01 nevű csomópont-konfigurációt hozzárendeli a megadott GUID azonosítóval rendelkező csomóponthoz.</span><span class="sxs-lookup"><span data-stu-id="65860-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="65860-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65860-111">PARAMETERS</span></span>

### <span data-ttu-id="65860-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65860-112">-AutomationAccountName</span></span>
<span data-ttu-id="65860-113">Megadja annak az automatizálási fióknak a nevét, amely az a DSC csomópontot tartalmazza, amelynek a parancsmagja módosítja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="65860-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="65860-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65860-114">-DefaultProfile</span></span>
<span data-ttu-id="65860-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="65860-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65860-116">-Force</span><span class="sxs-lookup"><span data-stu-id="65860-116">-Force</span></span>
<span data-ttu-id="65860-117">ps_force a parancs futtatását a felhasználó megerősítésének kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="65860-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65860-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="65860-118">-Id</span></span>
<span data-ttu-id="65860-119">Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez ez a parancsmag módosítja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="65860-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65860-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="65860-120">-NodeConfigurationName</span></span>
<span data-ttu-id="65860-121">Annak a csomópont-konfigurációnak a nevét adja meg, amelyre a parancsmag társítja a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="65860-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65860-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65860-122">-ResourceGroupName</span></span>
<span data-ttu-id="65860-123">Annak az erőforráscsoportnek a nevét adja meg, amelyben a parancsmag a DSC csomópontok konfigurációját módosítja.</span><span class="sxs-lookup"><span data-stu-id="65860-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="65860-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65860-124">-Confirm</span></span>
<span data-ttu-id="65860-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65860-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65860-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65860-126">-WhatIf</span></span>
<span data-ttu-id="65860-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65860-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65860-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65860-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65860-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65860-129">CommonParameters</span></span>
<span data-ttu-id="65860-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65860-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65860-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65860-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65860-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65860-132">INPUTS</span></span>

### <span data-ttu-id="65860-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="65860-133">None</span></span>
<span data-ttu-id="65860-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="65860-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65860-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65860-135">OUTPUTS</span></span>

### <span data-ttu-id="65860-136">Microsoft. Azure. Command. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="65860-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="65860-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65860-137">NOTES</span></span>

## <span data-ttu-id="65860-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65860-138">RELATED LINKS</span></span>

[<span data-ttu-id="65860-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="65860-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="65860-140">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="65860-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="65860-141">Regisztráció törlése – AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="65860-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


