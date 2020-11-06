---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: 7498310c232fd623b131bdf9ae59136d9a4c500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498479"
---
# <span data-ttu-id="1350a-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1350a-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="1350a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1350a-102">SYNOPSIS</span></span>
<span data-ttu-id="1350a-103">Automatizálási tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1350a-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1350a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1350a-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1350a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1350a-105">DESCRIPTION</span></span>
<span data-ttu-id="1350a-106">A **Remove-AzureRmAutomationCertificate** parancsmag eltávolítja az Azure automatizálási tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="1350a-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="1350a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1350a-107">EXAMPLES</span></span>

### <span data-ttu-id="1350a-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1350a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1350a-109">Ez a parancs eltávolítja a Cert01 nevű tanúsítványt a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="1350a-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1350a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1350a-110">PARAMETERS</span></span>

### <span data-ttu-id="1350a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1350a-111">-AutomationAccountName</span></span>
<span data-ttu-id="1350a-112">Annak az automatizálási fióknak a neve, amelyhez a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="1350a-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="1350a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1350a-113">-DefaultProfile</span></span>
<span data-ttu-id="1350a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1350a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1350a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1350a-115">-Name</span></span>
<span data-ttu-id="1350a-116">Annak a tanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="1350a-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1350a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1350a-117">-ResourceGroupName</span></span>
<span data-ttu-id="1350a-118">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="1350a-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="1350a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1350a-119">-Confirm</span></span>
<span data-ttu-id="1350a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1350a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1350a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1350a-121">-WhatIf</span></span>
<span data-ttu-id="1350a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1350a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1350a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1350a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1350a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1350a-124">CommonParameters</span></span>
<span data-ttu-id="1350a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1350a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1350a-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1350a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1350a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1350a-127">INPUTS</span></span>

### <span data-ttu-id="1350a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1350a-128">System.String</span></span>

## <span data-ttu-id="1350a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1350a-129">OUTPUTS</span></span>

### <span data-ttu-id="1350a-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="1350a-130">System.Void</span></span>

## <span data-ttu-id="1350a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1350a-131">NOTES</span></span>

## <span data-ttu-id="1350a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1350a-132">RELATED LINKS</span></span>

[<span data-ttu-id="1350a-133">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1350a-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1350a-134">Új – AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1350a-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1350a-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1350a-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


