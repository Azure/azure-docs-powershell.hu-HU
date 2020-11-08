---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014940"
---
# <span data-ttu-id="48316-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="48316-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="48316-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48316-102">SYNOPSIS</span></span>
<span data-ttu-id="48316-103">Automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="48316-103">Removes an Automation account.</span></span>

## <span data-ttu-id="48316-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48316-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48316-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48316-105">DESCRIPTION</span></span>
<span data-ttu-id="48316-106">A **Remove-AzAutomationAccount** parancsmag az Azure automatizálási fiókokat távolítja el egy erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="48316-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="48316-107">Az automatizálási fiókokról további információt az New-AzAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="48316-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="48316-108">Példák</span><span class="sxs-lookup"><span data-stu-id="48316-108">EXAMPLES</span></span>

### <span data-ttu-id="48316-109">1. példa: automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="48316-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="48316-110">Ez a parancs eltávolítja a ContosoAutomationAccount nevű automatizálási fiókot a felhasználó érvényesítése kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="48316-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="48316-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48316-111">PARAMETERS</span></span>

### <span data-ttu-id="48316-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48316-112">-DefaultProfile</span></span>
<span data-ttu-id="48316-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="48316-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48316-114">-Force</span><span class="sxs-lookup"><span data-stu-id="48316-114">-Force</span></span>
<span data-ttu-id="48316-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="48316-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48316-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48316-116">-Name</span></span>
<span data-ttu-id="48316-117">A parancsmag által eltávolított automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48316-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48316-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48316-118">-ResourceGroupName</span></span>
<span data-ttu-id="48316-119">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="48316-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="48316-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48316-120">-Confirm</span></span>
<span data-ttu-id="48316-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48316-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48316-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48316-122">-WhatIf</span></span>
<span data-ttu-id="48316-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48316-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48316-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48316-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48316-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48316-125">CommonParameters</span></span>
<span data-ttu-id="48316-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48316-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48316-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48316-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48316-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48316-128">INPUTS</span></span>

### <span data-ttu-id="48316-129">System. String</span><span class="sxs-lookup"><span data-stu-id="48316-129">System.String</span></span>

## <span data-ttu-id="48316-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48316-130">OUTPUTS</span></span>

### <span data-ttu-id="48316-131">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="48316-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="48316-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48316-132">NOTES</span></span>

## <span data-ttu-id="48316-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48316-133">RELATED LINKS</span></span>

[<span data-ttu-id="48316-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="48316-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="48316-135">Új – AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="48316-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="48316-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="48316-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


