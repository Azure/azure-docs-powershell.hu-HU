---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: b336104fea097b0f5adf0993853dd6fff7bba1f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673183"
---
# <span data-ttu-id="9f031-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9f031-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="9f031-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f031-102">SYNOPSIS</span></span>
<span data-ttu-id="9f031-103">Automatizálási változó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9f031-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f031-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f031-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f031-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f031-105">DESCRIPTION</span></span>
<span data-ttu-id="9f031-106">A **Remove-AzureRmAutomationVariable** parancsmag egy változót távolít el az Azure automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="9f031-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="9f031-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9f031-107">EXAMPLES</span></span>

### <span data-ttu-id="9f031-108">Példa 1: változó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9f031-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9f031-109">Ez a parancs eltávolítja a StringVariable22 nevű változót a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="9f031-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="9f031-110">Ez a parancs az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f031-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9f031-111">Ezért nem kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f031-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9f031-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f031-112">PARAMETERS</span></span>

### <span data-ttu-id="9f031-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f031-113">-AutomationAccountName</span></span>
<span data-ttu-id="9f031-114">Annak az automatizálási fióknak a neve, amely a parancsmag által törölt változót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9f031-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="9f031-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f031-115">-DefaultProfile</span></span>
<span data-ttu-id="9f031-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9f031-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f031-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f031-117">-Name</span></span>
<span data-ttu-id="9f031-118">A parancsmag által törölt változó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9f031-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f031-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f031-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f031-120">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag törli a változót.</span><span class="sxs-lookup"><span data-stu-id="9f031-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="9f031-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f031-121">-Confirm</span></span>
<span data-ttu-id="9f031-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f031-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f031-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f031-123">-WhatIf</span></span>
<span data-ttu-id="9f031-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f031-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f031-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f031-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f031-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f031-126">CommonParameters</span></span>
<span data-ttu-id="9f031-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f031-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f031-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f031-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f031-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f031-129">INPUTS</span></span>

### <span data-ttu-id="9f031-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9f031-130">System.String</span></span>

## <span data-ttu-id="9f031-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f031-131">OUTPUTS</span></span>

### <span data-ttu-id="9f031-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="9f031-132">System.Void</span></span>

## <span data-ttu-id="9f031-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f031-133">NOTES</span></span>

## <span data-ttu-id="9f031-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f031-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f031-135">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9f031-135">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="9f031-136">Új – AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9f031-136">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="9f031-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="9f031-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


