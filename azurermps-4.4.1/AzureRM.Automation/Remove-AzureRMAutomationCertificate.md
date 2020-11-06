---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499243"
---
# <span data-ttu-id="6e76c-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6e76c-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="6e76c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e76c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e76c-103">Automatizálási tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6e76c-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e76c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e76c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e76c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e76c-105">DESCRIPTION</span></span>
<span data-ttu-id="6e76c-106">A **Remove-AzureRmAutomationCertificate** parancsmag eltávolítja az Azure automatizálási tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="6e76c-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="6e76c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6e76c-107">EXAMPLES</span></span>

### <span data-ttu-id="6e76c-108">1. példa: tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6e76c-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6e76c-109">Ez a parancs eltávolítja a Cert01 nevű tanúsítványt a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="6e76c-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6e76c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e76c-110">PARAMETERS</span></span>

### <span data-ttu-id="6e76c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6e76c-111">-AutomationAccountName</span></span>
<span data-ttu-id="6e76c-112">Annak az automatizálási fióknak a neve, amelyhez a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="6e76c-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="6e76c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e76c-113">-Name</span></span>
<span data-ttu-id="6e76c-114">Annak a tanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="6e76c-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6e76c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e76c-115">-ResourceGroupName</span></span>
<span data-ttu-id="6e76c-116">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez a parancsmag eltávolítja a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="6e76c-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="6e76c-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e76c-117">-Confirm</span></span>
<span data-ttu-id="6e76c-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e76c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e76c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e76c-119">-WhatIf</span></span>
<span data-ttu-id="6e76c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e76c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e76c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e76c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e76c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e76c-122">-DefaultProfile</span></span>
<span data-ttu-id="6e76c-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e76c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e76c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e76c-124">CommonParameters</span></span>
<span data-ttu-id="6e76c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e76c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e76c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e76c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e76c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e76c-127">INPUTS</span></span>

## <span data-ttu-id="6e76c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e76c-128">OUTPUTS</span></span>

## <span data-ttu-id="6e76c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e76c-129">NOTES</span></span>

## <span data-ttu-id="6e76c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e76c-130">RELATED LINKS</span></span>

[<span data-ttu-id="6e76c-131">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6e76c-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="6e76c-132">Új – AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6e76c-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="6e76c-133">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6e76c-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


