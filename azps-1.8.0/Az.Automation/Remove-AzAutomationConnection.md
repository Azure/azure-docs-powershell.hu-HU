---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 76f82e81ca9593865fea642d44bf1bde58f60eb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671538"
---
# <span data-ttu-id="a5626-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a5626-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="a5626-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5626-102">SYNOPSIS</span></span>
<span data-ttu-id="a5626-103">Automatizálási kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a5626-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="a5626-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5626-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5626-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5626-105">DESCRIPTION</span></span>
<span data-ttu-id="a5626-106">A **Remove-AzAutomationConnection** parancsmag eltávolít egy kapcsolatot az Azure Automation szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="a5626-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="a5626-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5626-107">EXAMPLES</span></span>

### <span data-ttu-id="a5626-108">1. példa: kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a5626-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a5626-109">Ez a parancs eltávolítja a ContosoConnection nevű tanúsítványt a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a5626-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a5626-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5626-110">PARAMETERS</span></span>

### <span data-ttu-id="a5626-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a5626-111">-AutomationAccountName</span></span>
<span data-ttu-id="a5626-112">Annak az automatizálási fióknak a neve, amelyhez a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="a5626-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="a5626-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5626-113">-DefaultProfile</span></span>
<span data-ttu-id="a5626-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5626-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5626-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a5626-115">-Force</span></span>
<span data-ttu-id="a5626-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a5626-116">ps_force</span></span>

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

### <span data-ttu-id="a5626-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5626-117">-Name</span></span>
<span data-ttu-id="a5626-118">Annak a kapcsolatnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="a5626-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a5626-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5626-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5626-120">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="a5626-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="a5626-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5626-121">-Confirm</span></span>
<span data-ttu-id="a5626-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5626-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5626-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5626-123">-WhatIf</span></span>
<span data-ttu-id="a5626-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5626-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5626-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5626-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5626-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5626-126">CommonParameters</span></span>
<span data-ttu-id="a5626-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5626-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5626-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5626-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5626-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5626-129">INPUTS</span></span>

### <span data-ttu-id="a5626-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a5626-130">System.String</span></span>

## <span data-ttu-id="a5626-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5626-131">OUTPUTS</span></span>

### <span data-ttu-id="a5626-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="a5626-132">System.Void</span></span>

## <span data-ttu-id="a5626-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5626-133">NOTES</span></span>

## <span data-ttu-id="a5626-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5626-134">RELATED LINKS</span></span>

[<span data-ttu-id="a5626-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a5626-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="a5626-136">Új – AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a5626-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


