---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/send-feedback
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Send-Feedback.md
ms.openlocfilehash: 1405886572efabf1ffc91f071f262ca98515d141
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331434"
---
# <span data-ttu-id="8a612-101">Send-Feedback</span><span class="sxs-lookup"><span data-stu-id="8a612-101">Send-Feedback</span></span>

## <span data-ttu-id="8a612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a612-102">SYNOPSIS</span></span>
<span data-ttu-id="8a612-103">Visszajelzést küld az Azure PowerShell-csapatnak egy interaktív üzenetcsoporton keresztül.</span><span class="sxs-lookup"><span data-stu-id="8a612-103">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

## <span data-ttu-id="8a612-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a612-104">SYNTAX</span></span>

```
Send-Feedback [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a612-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a612-105">DESCRIPTION</span></span>
<span data-ttu-id="8a612-106">A Send-Feedback parancsmag visszajelzést küld az Azure PowerShell-csapatnak.</span><span class="sxs-lookup"><span data-stu-id="8a612-106">The Send-Feedback cmdlet sends feedback to the Azure PowerShell team.</span></span>

## <span data-ttu-id="8a612-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a612-107">EXAMPLES</span></span>

### <span data-ttu-id="8a612-108">1. példa:</span><span class="sxs-lookup"><span data-stu-id="8a612-108">Example 1:</span></span>
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

## <span data-ttu-id="8a612-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a612-109">PARAMETERS</span></span>

### <span data-ttu-id="8a612-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a612-110">-DefaultProfile</span></span>
<span data-ttu-id="8a612-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a612-111">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a612-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a612-112">CommonParameters</span></span>
<span data-ttu-id="8a612-113">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a612-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a612-114">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a612-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a612-115">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a612-115">INPUTS</span></span>

### <span data-ttu-id="8a612-116">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a612-116">None</span></span>

## <span data-ttu-id="8a612-117">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a612-117">OUTPUTS</span></span>

### <span data-ttu-id="8a612-118">System.Void</span><span class="sxs-lookup"><span data-stu-id="8a612-118">System.Void</span></span>

## <span data-ttu-id="8a612-119">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a612-119">NOTES</span></span>

## <span data-ttu-id="8a612-120">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a612-120">RELATED LINKS</span></span>
