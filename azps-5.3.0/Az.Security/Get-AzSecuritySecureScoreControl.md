---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377843"
---
# <span data-ttu-id="08eac-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="08eac-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="08eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08eac-102">SYNOPSIS</span></span>
<span data-ttu-id="08eac-103">Biztonsági pontszámvezérlőket és azok eredményeit kapja meg egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="08eac-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="08eac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08eac-104">SYNTAX</span></span>

### <span data-ttu-id="08eac-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08eac-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08eac-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="08eac-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08eac-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08eac-107">EXAMPLES</span></span>

### <span data-ttu-id="08eac-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="08eac-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="08eac-109">Lekérte az összes biztonsági pontszámot egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="08eac-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="08eac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08eac-110">PARAMETERS</span></span>

### <span data-ttu-id="08eac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08eac-111">-DefaultProfile</span></span>
<span data-ttu-id="08eac-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08eac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eac-113">-Name</span><span class="sxs-lookup"><span data-stu-id="08eac-113">-Name</span></span>
<span data-ttu-id="08eac-114">Biztonsági pontszám neve.</span><span class="sxs-lookup"><span data-stu-id="08eac-114">Secure score name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eac-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08eac-115">CommonParameters</span></span>
<span data-ttu-id="08eac-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08eac-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08eac-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08eac-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08eac-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08eac-118">INPUTS</span></span>

### <span data-ttu-id="08eac-119">System.String</span><span class="sxs-lookup"><span data-stu-id="08eac-119">System.String</span></span>

## <span data-ttu-id="08eac-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08eac-120">OUTPUTS</span></span>

### <span data-ttu-id="08eac-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="08eac-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="08eac-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08eac-122">NOTES</span></span>

## <span data-ttu-id="08eac-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08eac-123">RELATED LINKS</span></span>
