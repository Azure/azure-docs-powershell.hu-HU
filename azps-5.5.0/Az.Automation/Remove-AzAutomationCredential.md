---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205510"
---
# <span data-ttu-id="d8d60-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d8d60-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="d8d60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d60-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d60-103">Eltávolítja az automatizálási hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="d8d60-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="d8d60-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8d60-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d60-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8d60-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d60-106">A **Remove-AzAutomationCredential** parancsmag eltávolítja a hitelesítő adatokat az Azure Automation szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="d8d60-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="d8d60-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8d60-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d60-108">1. példa: Hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d8d60-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d8d60-109">Ez a parancs eltávolítja a ContosoCredential nevű hitelesítő adatokat a Contoso17 nevű Azure Automation-fiókból.</span><span class="sxs-lookup"><span data-stu-id="d8d60-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d8d60-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8d60-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d60-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8d60-111">-AutomationAccountName</span></span>
<span data-ttu-id="d8d60-112">Annak az automatizálási fióknak a nevét adja meg, amelyből a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="d8d60-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="d8d60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d60-113">-DefaultProfile</span></span>
<span data-ttu-id="d8d60-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8d60-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8d60-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d8d60-115">-Name</span></span>
<span data-ttu-id="d8d60-116">Megadja annak a hitelesítő adatnak a nevét, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d8d60-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d8d60-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d60-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8d60-118">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja eltávolítja a hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="d8d60-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="d8d60-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8d60-119">-Confirm</span></span>
<span data-ttu-id="d8d60-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8d60-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d60-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d60-121">-WhatIf</span></span>
<span data-ttu-id="d8d60-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8d60-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d60-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8d60-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d60-124">CommonParameters</span></span>
<span data-ttu-id="d8d60-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d60-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d60-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d60-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8d60-127">INPUTS</span></span>

### <span data-ttu-id="d8d60-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d8d60-128">System.String</span></span>

## <span data-ttu-id="d8d60-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8d60-129">OUTPUTS</span></span>

### <span data-ttu-id="d8d60-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d8d60-130">System.Void</span></span>

## <span data-ttu-id="d8d60-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8d60-131">NOTES</span></span>

## <span data-ttu-id="d8d60-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8d60-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8d60-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d8d60-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="d8d60-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d8d60-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="d8d60-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d8d60-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


