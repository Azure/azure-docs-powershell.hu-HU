---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: e3dd0d475a2a2c34dfa7912bf9ced4ef958295c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494203"
---
# <span data-ttu-id="e2bac-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e2bac-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="e2bac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2bac-102">SYNOPSIS</span></span>
<span data-ttu-id="e2bac-103">Automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e2bac-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2bac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2bac-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2bac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2bac-105">DESCRIPTION</span></span>
<span data-ttu-id="e2bac-106">A **Remove-AzureRmAutomationAccount** parancsmag az Azure automatizálási fiókokat távolítja el egy erőforráscsoport-csoportból.</span><span class="sxs-lookup"><span data-stu-id="e2bac-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="e2bac-107">Az automatizálási fiókokról további információt az New-AzureRmAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="e2bac-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="e2bac-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e2bac-108">EXAMPLES</span></span>

### <span data-ttu-id="e2bac-109">1. példa: automatizálási fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e2bac-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e2bac-110">Ez a parancs eltávolítja a ContosoAutomationAccount nevű automatizálási fiókot a felhasználó érvényesítése kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="e2bac-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="e2bac-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2bac-111">PARAMETERS</span></span>

### <span data-ttu-id="e2bac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2bac-112">-DefaultProfile</span></span>
<span data-ttu-id="e2bac-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e2bac-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2bac-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e2bac-114">-Force</span></span>
<span data-ttu-id="e2bac-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="e2bac-115">ps_force</span></span>

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

### <span data-ttu-id="e2bac-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2bac-116">-Name</span></span>
<span data-ttu-id="e2bac-117">A parancsmag által eltávolított automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2bac-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e2bac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2bac-118">-ResourceGroupName</span></span>
<span data-ttu-id="e2bac-119">Annak az erőforrás-csoportnak a neve, amelyből a parancsmag eltávolítja az automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="e2bac-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="e2bac-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2bac-120">-Confirm</span></span>
<span data-ttu-id="e2bac-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2bac-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2bac-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2bac-122">-WhatIf</span></span>
<span data-ttu-id="e2bac-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2bac-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2bac-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2bac-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2bac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2bac-125">CommonParameters</span></span>
<span data-ttu-id="e2bac-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2bac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2bac-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2bac-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2bac-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2bac-128">INPUTS</span></span>

### <span data-ttu-id="e2bac-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e2bac-129">System.String</span></span>

## <span data-ttu-id="e2bac-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2bac-130">OUTPUTS</span></span>

### <span data-ttu-id="e2bac-131">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e2bac-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e2bac-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2bac-132">NOTES</span></span>

## <span data-ttu-id="e2bac-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2bac-133">RELATED LINKS</span></span>

[<span data-ttu-id="e2bac-134">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e2bac-134">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="e2bac-135">Új – AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e2bac-135">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="e2bac-136">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e2bac-136">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


