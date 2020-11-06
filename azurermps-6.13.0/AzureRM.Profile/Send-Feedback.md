---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Send-Feedback.md
ms.openlocfilehash: efe4dd4c9601c7b03ba2a9621f098049b9b4af11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500152"
---
# <span data-ttu-id="f3269-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="f3269-101">Send-Feedback</span></span>

## <span data-ttu-id="f3269-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3269-102">SYNOPSIS</span></span>
<span data-ttu-id="f3269-103">Visszajelzést küld az Azure PowerShell-csoportnak egy sor interaktív utasítással.</span><span class="sxs-lookup"><span data-stu-id="f3269-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3269-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3269-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3269-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3269-105">DESCRIPTION</span></span>
<span data-ttu-id="f3269-106">Az Send-Feedback parancsmag visszajelzést küld az Azure PowerShell-csoportnak.</span><span class="sxs-lookup"><span data-stu-id="f3269-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="f3269-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3269-107">EXAMPLES</span></span>

### <span data-ttu-id="f3269-108">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="f3269-108">Example 1:</span></span>
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

## <span data-ttu-id="f3269-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3269-109">PARAMETERS</span></span>

### <span data-ttu-id="f3269-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3269-110">-DefaultProfile</span></span>
<span data-ttu-id="f3269-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3269-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3269-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3269-112">CommonParameters</span></span>
<span data-ttu-id="f3269-113">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3269-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3269-114">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3269-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3269-115">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3269-115">INPUTS</span></span>

### <span data-ttu-id="f3269-116">Nincs</span><span class="sxs-lookup"><span data-stu-id="f3269-116">None</span></span>

## <span data-ttu-id="f3269-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3269-117">OUTPUTS</span></span>

### <span data-ttu-id="f3269-118">System. Void</span><span class="sxs-lookup"><span data-stu-id="f3269-118">System.Void</span></span>

## <span data-ttu-id="f3269-119">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3269-119">NOTES</span></span>

## <span data-ttu-id="f3269-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3269-120">RELATED LINKS</span></span>
