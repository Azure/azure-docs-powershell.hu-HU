---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014935"
---
# <span data-ttu-id="e78ec-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e78ec-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="e78ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e78ec-102">SYNOPSIS</span></span>
<span data-ttu-id="e78ec-103">Automatizálási hitelesítő adatok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e78ec-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="e78ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e78ec-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e78ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e78ec-105">DESCRIPTION</span></span>
<span data-ttu-id="e78ec-106">A **Remove-AzAutomationCredential** parancsmag eltávolítja a hitelesítő adatokat az Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="e78ec-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="e78ec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e78ec-107">EXAMPLES</span></span>

### <span data-ttu-id="e78ec-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e78ec-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e78ec-109">Ez a parancs eltávolítja a ContosoCredential nevű hitelesítő adatokat a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="e78ec-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e78ec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e78ec-110">PARAMETERS</span></span>

### <span data-ttu-id="e78ec-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e78ec-111">-AutomationAccountName</span></span>
<span data-ttu-id="e78ec-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="e78ec-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="e78ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e78ec-113">-DefaultProfile</span></span>
<span data-ttu-id="e78ec-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e78ec-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e78ec-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e78ec-115">-Name</span></span>
<span data-ttu-id="e78ec-116">Annak a hitelesítő adatoknak a nevét adja meg, amelyet a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="e78ec-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e78ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e78ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="e78ec-118">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="e78ec-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="e78ec-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e78ec-119">-Confirm</span></span>
<span data-ttu-id="e78ec-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e78ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e78ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e78ec-121">-WhatIf</span></span>
<span data-ttu-id="e78ec-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e78ec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e78ec-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e78ec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e78ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e78ec-124">CommonParameters</span></span>
<span data-ttu-id="e78ec-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e78ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e78ec-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e78ec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e78ec-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e78ec-127">INPUTS</span></span>

### <span data-ttu-id="e78ec-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e78ec-128">System.String</span></span>

## <span data-ttu-id="e78ec-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e78ec-129">OUTPUTS</span></span>

### <span data-ttu-id="e78ec-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="e78ec-130">System.Void</span></span>

## <span data-ttu-id="e78ec-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e78ec-131">NOTES</span></span>

## <span data-ttu-id="e78ec-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e78ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="e78ec-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e78ec-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="e78ec-134">Új – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e78ec-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="e78ec-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e78ec-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


