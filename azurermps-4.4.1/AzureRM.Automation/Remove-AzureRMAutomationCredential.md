---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 2c98cde73610a7a72b237bbe268f527fefaf71a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499236"
---
# <span data-ttu-id="70504-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="70504-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="70504-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70504-102">SYNOPSIS</span></span>
<span data-ttu-id="70504-103">Automatizálási hitelesítő adatok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="70504-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70504-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70504-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70504-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70504-105">DESCRIPTION</span></span>
<span data-ttu-id="70504-106">A **Remove-AzureRmAutomationCredential** parancsmag eltávolítja a hitelesítő adatokat az Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="70504-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="70504-107">Példák</span><span class="sxs-lookup"><span data-stu-id="70504-107">EXAMPLES</span></span>

### <span data-ttu-id="70504-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70504-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="70504-109">Ez a parancs eltávolítja a ContosoCredential nevű hitelesítő adatokat a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="70504-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="70504-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70504-110">PARAMETERS</span></span>

### <span data-ttu-id="70504-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70504-111">-AutomationAccountName</span></span>
<span data-ttu-id="70504-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="70504-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="70504-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70504-113">-Name</span></span>
<span data-ttu-id="70504-114">Annak a hitelesítő adatoknak a nevét adja meg, amelyet a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="70504-114">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="70504-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70504-115">-ResourceGroupName</span></span>
<span data-ttu-id="70504-116">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="70504-116">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="70504-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70504-117">-Confirm</span></span>
<span data-ttu-id="70504-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70504-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70504-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70504-119">-WhatIf</span></span>
<span data-ttu-id="70504-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70504-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70504-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70504-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70504-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70504-122">-DefaultProfile</span></span>
<span data-ttu-id="70504-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70504-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70504-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70504-124">CommonParameters</span></span>
<span data-ttu-id="70504-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70504-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70504-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70504-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70504-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70504-127">INPUTS</span></span>

## <span data-ttu-id="70504-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70504-128">OUTPUTS</span></span>

## <span data-ttu-id="70504-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70504-129">NOTES</span></span>

## <span data-ttu-id="70504-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70504-130">RELATED LINKS</span></span>

[<span data-ttu-id="70504-131">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="70504-131">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="70504-132">Új – AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="70504-132">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="70504-133">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="70504-133">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


