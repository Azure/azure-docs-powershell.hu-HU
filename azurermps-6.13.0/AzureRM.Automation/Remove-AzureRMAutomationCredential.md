---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 6c0fe1185bfa8d5233371788da87e7a13fe32c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492885"
---
# <span data-ttu-id="caf24-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="caf24-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="caf24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="caf24-102">SYNOPSIS</span></span>
<span data-ttu-id="caf24-103">Automatizálási hitelesítő adatok eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="caf24-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caf24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="caf24-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caf24-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="caf24-105">DESCRIPTION</span></span>
<span data-ttu-id="caf24-106">A **Remove-AzureRmAutomationCredential** parancsmag eltávolítja a hitelesítő adatokat az Azure automatizálási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="caf24-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="caf24-107">Példák</span><span class="sxs-lookup"><span data-stu-id="caf24-107">EXAMPLES</span></span>

### <span data-ttu-id="caf24-108">1. példa: hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="caf24-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="caf24-109">Ez a parancs eltávolítja a ContosoCredential nevű hitelesítő adatokat a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="caf24-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="caf24-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="caf24-110">PARAMETERS</span></span>

### <span data-ttu-id="caf24-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="caf24-111">-AutomationAccountName</span></span>
<span data-ttu-id="caf24-112">Annak az automatizálási fióknak a neve, amelyből a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="caf24-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="caf24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf24-113">-DefaultProfile</span></span>
<span data-ttu-id="caf24-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="caf24-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caf24-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="caf24-115">-Name</span></span>
<span data-ttu-id="caf24-116">Annak a hitelesítő adatoknak a nevét adja meg, amelyet a parancsmag eltávolít.</span><span class="sxs-lookup"><span data-stu-id="caf24-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="caf24-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf24-117">-ResourceGroupName</span></span>
<span data-ttu-id="caf24-118">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="caf24-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="caf24-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="caf24-119">-Confirm</span></span>
<span data-ttu-id="caf24-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="caf24-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caf24-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caf24-121">-WhatIf</span></span>
<span data-ttu-id="caf24-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="caf24-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caf24-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="caf24-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caf24-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf24-124">CommonParameters</span></span>
<span data-ttu-id="caf24-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="caf24-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf24-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf24-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf24-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="caf24-127">INPUTS</span></span>

### <span data-ttu-id="caf24-128">System. String</span><span class="sxs-lookup"><span data-stu-id="caf24-128">System.String</span></span>

## <span data-ttu-id="caf24-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="caf24-129">OUTPUTS</span></span>

### <span data-ttu-id="caf24-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="caf24-130">System.Void</span></span>

## <span data-ttu-id="caf24-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="caf24-131">NOTES</span></span>

## <span data-ttu-id="caf24-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="caf24-132">RELATED LINKS</span></span>

[<span data-ttu-id="caf24-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="caf24-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="caf24-134">Új – AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="caf24-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="caf24-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="caf24-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


