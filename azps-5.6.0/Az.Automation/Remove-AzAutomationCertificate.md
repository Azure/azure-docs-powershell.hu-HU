---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: 17eb5530511ccc4303fdb2c978006223e6bd7ed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009989"
---
# <span data-ttu-id="7e9f1-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e9f1-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="7e9f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e9f1-103">Eltávolít egy automatizálási tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="7e9f1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e9f1-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e9f1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e9f1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e9f1-106">A **Remove-AzAutomationCertificate** parancsmag eltávolítja a tanúsítványokat az Azure Automationből.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="7e9f1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e9f1-107">EXAMPLES</span></span>

### <span data-ttu-id="7e9f1-108">1. példa: Tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7e9f1-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7e9f1-109">Ez a parancs eltávolítja a Cert01 nevű tanúsítványt a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7e9f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e9f1-110">PARAMETERS</span></span>

### <span data-ttu-id="7e9f1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7e9f1-111">-AutomationAccountName</span></span>
<span data-ttu-id="7e9f1-112">Annak az automatizálási fióknak a nevét adja meg, amelyből a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="7e9f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e9f1-113">-DefaultProfile</span></span>
<span data-ttu-id="7e9f1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7e9f1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e9f1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7e9f1-115">-Name</span></span>
<span data-ttu-id="7e9f1-116">Annak a tanúsítványnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7e9f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e9f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="7e9f1-118">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="7e9f1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e9f1-119">-Confirm</span></span>
<span data-ttu-id="7e9f1-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e9f1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e9f1-121">-WhatIf</span></span>
<span data-ttu-id="7e9f1-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e9f1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e9f1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e9f1-124">CommonParameters</span></span>
<span data-ttu-id="7e9f1-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e9f1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e9f1-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e9f1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e9f1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e9f1-127">INPUTS</span></span>

### <span data-ttu-id="7e9f1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7e9f1-128">System.String</span></span>

## <span data-ttu-id="7e9f1-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e9f1-129">OUTPUTS</span></span>

### <span data-ttu-id="7e9f1-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="7e9f1-130">System.Void</span></span>

## <span data-ttu-id="7e9f1-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e9f1-131">NOTES</span></span>

## <span data-ttu-id="7e9f1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e9f1-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e9f1-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e9f1-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="7e9f1-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e9f1-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="7e9f1-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e9f1-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


