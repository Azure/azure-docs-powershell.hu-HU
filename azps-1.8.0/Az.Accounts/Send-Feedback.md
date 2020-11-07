---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 3dae531f23e5ef5e8ea800cf935a3b9f413ae640
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665774"
---
# <span data-ttu-id="60cc6-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="60cc6-101">Send-Feedback</span></span>

## <span data-ttu-id="60cc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="60cc6-103">Visszajelzést küld az Azure PowerShell-csoportnak egy sor interaktív utasítással.</span><span class="sxs-lookup"><span data-stu-id="60cc6-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="60cc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60cc6-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60cc6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="60cc6-106">Az Send-Feedback parancsmag visszajelzést küld az Azure PowerShell-csoportnak.</span><span class="sxs-lookup"><span data-stu-id="60cc6-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="60cc6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60cc6-107">EXAMPLES</span></span>

### <span data-ttu-id="60cc6-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="60cc6-108">Example 1:</span></span>
```
PS C:\> Send-Feedback

With zero (0) being the least and ten (10) being the most, how likely are you to recommend Azure PowerShell to a friend or colleague?

10

What does Azure PowerShell do well?

Response.

Upon what could Azure PowerShell improve?

Response.

Please enter your email if you are interested in providing follow up information:

your@email.com
```

## <span data-ttu-id="60cc6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60cc6-109">PARAMETERS</span></span>

### <span data-ttu-id="60cc6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60cc6-110">-DefaultProfile</span></span>
<span data-ttu-id="60cc6-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60cc6-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60cc6-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cc6-112">CommonParameters</span></span>
<span data-ttu-id="60cc6-113">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60cc6-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cc6-114">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60cc6-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cc6-115">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60cc6-115">INPUTS</span></span>

### <span data-ttu-id="60cc6-116">Nincs</span><span class="sxs-lookup"><span data-stu-id="60cc6-116">None</span></span>

## <span data-ttu-id="60cc6-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60cc6-117">OUTPUTS</span></span>

### <span data-ttu-id="60cc6-118">System. Void</span><span class="sxs-lookup"><span data-stu-id="60cc6-118">System.Void</span></span>

## <span data-ttu-id="60cc6-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60cc6-119">NOTES</span></span>

## <span data-ttu-id="60cc6-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60cc6-120">RELATED LINKS</span></span>
