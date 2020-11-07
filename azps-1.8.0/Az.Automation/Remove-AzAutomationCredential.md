---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 703be26244e61b797f3359ef508d92e38847bf8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671536"
---
# <span data-ttu-id="15bfa-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="15bfa-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="15bfa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="15bfa-103">Automatizálási hitelesítő adatok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="15bfa-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="15bfa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15bfa-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15bfa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="15bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="15bfa-106">A **Remove-AzAutomationCredential** parancsmag eltávolítja a hitelesítő adatokat az Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="15bfa-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="15bfa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="15bfa-107">EXAMPLES</span></span>

### <span data-ttu-id="15bfa-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="15bfa-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="15bfa-109">Ez a parancs eltávolítja a ContosoCredential nevű hitelesítő adatokat a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="15bfa-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="15bfa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15bfa-110">PARAMETERS</span></span>

### <span data-ttu-id="15bfa-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="15bfa-111">-AutomationAccountName</span></span>
<span data-ttu-id="15bfa-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="15bfa-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="15bfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bfa-113">-DefaultProfile</span></span>
<span data-ttu-id="15bfa-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="15bfa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15bfa-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15bfa-115">-Name</span></span>
<span data-ttu-id="15bfa-116">Annak a hitelesítő adatoknak a nevét adja meg, amelyet a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="15bfa-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="15bfa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15bfa-117">-ResourceGroupName</span></span>
<span data-ttu-id="15bfa-118">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="15bfa-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="15bfa-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15bfa-119">-Confirm</span></span>
<span data-ttu-id="15bfa-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15bfa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15bfa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15bfa-121">-WhatIf</span></span>
<span data-ttu-id="15bfa-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15bfa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15bfa-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15bfa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15bfa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bfa-124">CommonParameters</span></span>
<span data-ttu-id="15bfa-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15bfa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bfa-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15bfa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bfa-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15bfa-127">INPUTS</span></span>

### <span data-ttu-id="15bfa-128">System. String</span><span class="sxs-lookup"><span data-stu-id="15bfa-128">System.String</span></span>

## <span data-ttu-id="15bfa-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15bfa-129">OUTPUTS</span></span>

### <span data-ttu-id="15bfa-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="15bfa-130">System.Void</span></span>

## <span data-ttu-id="15bfa-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15bfa-131">NOTES</span></span>

## <span data-ttu-id="15bfa-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15bfa-132">RELATED LINKS</span></span>

[<span data-ttu-id="15bfa-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="15bfa-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="15bfa-134">Új – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="15bfa-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="15bfa-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="15bfa-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


