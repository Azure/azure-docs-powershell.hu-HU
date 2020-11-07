---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 11b6772325c3e5170c697b21d25092fd96f3e2e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680435"
---
# <span data-ttu-id="a48e3-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a48e3-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="a48e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a48e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a48e3-103">Automatizálási hitelesítő adatok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="a48e3-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a48e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a48e3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a48e3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a48e3-105">DESCRIPTION</span></span>
<span data-ttu-id="a48e3-106">A **Remove-AzureRmAutomationCredential** parancsmag eltávolítja a hitelesítő adatokat az Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="a48e3-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="a48e3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a48e3-107">EXAMPLES</span></span>

### <span data-ttu-id="a48e3-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a48e3-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a48e3-109">Ez a parancs eltávolítja a ContosoCredential nevű hitelesítő adatokat a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a48e3-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a48e3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a48e3-110">PARAMETERS</span></span>

### <span data-ttu-id="a48e3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a48e3-111">-AutomationAccountName</span></span>
<span data-ttu-id="a48e3-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="a48e3-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48e3-113">-DefaultProfile</span></span>
<span data-ttu-id="a48e3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a48e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48e3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a48e3-115">-Name</span></span>
<span data-ttu-id="a48e3-116">Annak a hitelesítő adatoknak a nevét adja meg, amelyet a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="a48e3-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a48e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="a48e3-118">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="a48e3-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a48e3-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a48e3-119">-Confirm</span></span>
<span data-ttu-id="a48e3-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a48e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a48e3-121">-WhatIf</span></span>
<span data-ttu-id="a48e3-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a48e3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a48e3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a48e3-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a48e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48e3-124">CommonParameters</span></span>
<span data-ttu-id="a48e3-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a48e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48e3-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a48e3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48e3-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a48e3-127">INPUTS</span></span>

### <span data-ttu-id="a48e3-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="a48e3-128">None</span></span>
<span data-ttu-id="a48e3-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a48e3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a48e3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a48e3-130">OUTPUTS</span></span>

## <span data-ttu-id="a48e3-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a48e3-131">NOTES</span></span>

## <span data-ttu-id="a48e3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a48e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="a48e3-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a48e3-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="a48e3-134">Új – AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a48e3-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="a48e3-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a48e3-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


