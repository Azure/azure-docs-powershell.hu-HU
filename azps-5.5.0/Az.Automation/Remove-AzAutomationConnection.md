---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205519"
---
# <span data-ttu-id="da9f8-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="da9f8-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="da9f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da9f8-102">SYNOPSIS</span></span>
<span data-ttu-id="da9f8-103">Eltávolítja az automatizálási kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="da9f8-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="da9f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da9f8-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da9f8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da9f8-105">DESCRIPTION</span></span>
<span data-ttu-id="da9f8-106">A **Remove-AzAutomationConnection** parancsmag eltávolítja a kapcsolatot az Azure Automationből.</span><span class="sxs-lookup"><span data-stu-id="da9f8-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="da9f8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da9f8-107">EXAMPLES</span></span>

### <span data-ttu-id="da9f8-108">1. példa: Kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="da9f8-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="da9f8-109">Ez a parancs eltávolítja a ContosoConnection nevű tanúsítványt a Contoso17 nevű automatizálási fiókból.</span><span class="sxs-lookup"><span data-stu-id="da9f8-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="da9f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da9f8-110">PARAMETERS</span></span>

### <span data-ttu-id="da9f8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da9f8-111">-AutomationAccountName</span></span>
<span data-ttu-id="da9f8-112">Annak az automatizálási fióknak a nevét adja meg, amelyből a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="da9f8-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="da9f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9f8-113">-DefaultProfile</span></span>
<span data-ttu-id="da9f8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="da9f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da9f8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="da9f8-115">-Force</span></span>
<span data-ttu-id="da9f8-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="da9f8-116">ps_force</span></span>

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

### <span data-ttu-id="da9f8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da9f8-117">-Name</span></span>
<span data-ttu-id="da9f8-118">A parancsmag által eltávolított kapcsolat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da9f8-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="da9f8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da9f8-119">-ResourceGroupName</span></span>
<span data-ttu-id="da9f8-120">Annak az erőforráscsoportnak a nevét adja meg, amelyből a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="da9f8-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="da9f8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da9f8-121">-Confirm</span></span>
<span data-ttu-id="da9f8-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da9f8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da9f8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da9f8-123">-WhatIf</span></span>
<span data-ttu-id="da9f8-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da9f8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da9f8-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da9f8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da9f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9f8-126">CommonParameters</span></span>
<span data-ttu-id="da9f8-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da9f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9f8-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da9f8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9f8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da9f8-129">INPUTS</span></span>

### <span data-ttu-id="da9f8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="da9f8-130">System.String</span></span>

## <span data-ttu-id="da9f8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da9f8-131">OUTPUTS</span></span>

### <span data-ttu-id="da9f8-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="da9f8-132">System.Void</span></span>

## <span data-ttu-id="da9f8-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da9f8-133">NOTES</span></span>

## <span data-ttu-id="da9f8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da9f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="da9f8-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="da9f8-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="da9f8-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="da9f8-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


