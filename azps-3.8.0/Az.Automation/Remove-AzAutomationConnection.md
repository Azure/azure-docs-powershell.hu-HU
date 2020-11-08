---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014936"
---
# <span data-ttu-id="e8ca0-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e8ca0-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="e8ca0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ca0-103">Automatizálási kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e8ca0-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="e8ca0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8ca0-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8ca0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ca0-106">A **Remove-AzAutomationConnection** parancsmag eltávolít egy kapcsolatot az Azure Automation szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="e8ca0-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="e8ca0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e8ca0-107">EXAMPLES</span></span>

### <span data-ttu-id="e8ca0-108">1. példa: kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e8ca0-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e8ca0-109">Ez a parancs eltávolítja a ContosoConnection nevű tanúsítványt a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="e8ca0-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e8ca0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8ca0-110">PARAMETERS</span></span>

### <span data-ttu-id="e8ca0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8ca0-111">-AutomationAccountName</span></span>
<span data-ttu-id="e8ca0-112">Annak az automatizálási fióknak a neve, amelyhez a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="e8ca0-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="e8ca0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ca0-113">-DefaultProfile</span></span>
<span data-ttu-id="e8ca0-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e8ca0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8ca0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e8ca0-115">-Force</span></span>
<span data-ttu-id="e8ca0-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="e8ca0-116">ps_force</span></span>

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

### <span data-ttu-id="e8ca0-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8ca0-117">-Name</span></span>
<span data-ttu-id="e8ca0-118">Annak a kapcsolatnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="e8ca0-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e8ca0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ca0-119">-ResourceGroupName</span></span>
<span data-ttu-id="e8ca0-120">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="e8ca0-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="e8ca0-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8ca0-121">-Confirm</span></span>
<span data-ttu-id="e8ca0-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8ca0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ca0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ca0-123">-WhatIf</span></span>
<span data-ttu-id="e8ca0-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8ca0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ca0-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8ca0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ca0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ca0-126">CommonParameters</span></span>
<span data-ttu-id="e8ca0-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8ca0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ca0-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ca0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ca0-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ca0-129">INPUTS</span></span>

### <span data-ttu-id="e8ca0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ca0-130">System.String</span></span>

## <span data-ttu-id="e8ca0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ca0-131">OUTPUTS</span></span>

### <span data-ttu-id="e8ca0-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="e8ca0-132">System.Void</span></span>

## <span data-ttu-id="e8ca0-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8ca0-133">NOTES</span></span>

## <span data-ttu-id="e8ca0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8ca0-134">RELATED LINKS</span></span>

[<span data-ttu-id="e8ca0-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e8ca0-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="e8ca0-136">Új – AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e8ca0-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


