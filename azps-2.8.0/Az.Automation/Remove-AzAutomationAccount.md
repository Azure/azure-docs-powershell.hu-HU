---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: 8db8ab416203c9e33ec6fd7a30d2c6170318c627
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667777"
---
# <span data-ttu-id="ef1d5-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef1d5-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="ef1d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef1d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1d5-103">Automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ef1d5-103">Removes an Automation account.</span></span>

## <span data-ttu-id="ef1d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef1d5-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef1d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef1d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ef1d5-106">A **Remove-AzAutomationAccount** parancsmag az Azure automatizálási fiókokat távolítja el egy erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="ef1d5-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="ef1d5-107">Az automatizálási fiókokról további információt az New-AzAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="ef1d5-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="ef1d5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ef1d5-108">EXAMPLES</span></span>

### <span data-ttu-id="ef1d5-109">1. példa: automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ef1d5-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ef1d5-110">Ez a parancs eltávolítja a ContosoAutomationAccount nevű automatizálási fiókot a felhasználó érvényesítése kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ef1d5-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="ef1d5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef1d5-111">PARAMETERS</span></span>

### <span data-ttu-id="ef1d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1d5-112">-DefaultProfile</span></span>
<span data-ttu-id="ef1d5-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ef1d5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef1d5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ef1d5-114">-Force</span></span>
<span data-ttu-id="ef1d5-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="ef1d5-115">ps_force</span></span>

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

### <span data-ttu-id="ef1d5-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef1d5-116">-Name</span></span>
<span data-ttu-id="ef1d5-117">A parancsmag által eltávolított automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef1d5-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ef1d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="ef1d5-119">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="ef1d5-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="ef1d5-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef1d5-120">-Confirm</span></span>
<span data-ttu-id="ef1d5-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef1d5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef1d5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef1d5-122">-WhatIf</span></span>
<span data-ttu-id="ef1d5-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef1d5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef1d5-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef1d5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef1d5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1d5-125">CommonParameters</span></span>
<span data-ttu-id="ef1d5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef1d5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1d5-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1d5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1d5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef1d5-128">INPUTS</span></span>

### <span data-ttu-id="ef1d5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ef1d5-129">System.String</span></span>

## <span data-ttu-id="ef1d5-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef1d5-130">OUTPUTS</span></span>

### <span data-ttu-id="ef1d5-131">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef1d5-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ef1d5-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef1d5-132">NOTES</span></span>

## <span data-ttu-id="ef1d5-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef1d5-133">RELATED LINKS</span></span>

[<span data-ttu-id="ef1d5-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef1d5-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="ef1d5-135">Új – AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef1d5-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="ef1d5-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef1d5-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


