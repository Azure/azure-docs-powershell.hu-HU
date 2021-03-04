---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 497865446e943fc34f45f6c98713d559086cca84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932266"
---
# <span data-ttu-id="2618b-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="2618b-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="2618b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2618b-102">SYNOPSIS</span></span>
<span data-ttu-id="2618b-103">Biztonsági pontszámvezérlőket és azok eredményeit kapja meg egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="2618b-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="2618b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2618b-104">SYNTAX</span></span>

### <span data-ttu-id="2618b-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2618b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2618b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2618b-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2618b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2618b-107">EXAMPLES</span></span>

### <span data-ttu-id="2618b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2618b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="2618b-109">Lekérte az összes biztonsági pontszámot egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="2618b-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="2618b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2618b-110">PARAMETERS</span></span>

### <span data-ttu-id="2618b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2618b-111">-DefaultProfile</span></span>
<span data-ttu-id="2618b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2618b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2618b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2618b-113">-Name</span></span>
<span data-ttu-id="2618b-114">Biztonsági pontszám neve.</span><span class="sxs-lookup"><span data-stu-id="2618b-114">Secure score name.</span></span>

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

### <span data-ttu-id="2618b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2618b-115">CommonParameters</span></span>
<span data-ttu-id="2618b-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2618b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2618b-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2618b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2618b-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2618b-118">INPUTS</span></span>

### <span data-ttu-id="2618b-119">System.String</span><span class="sxs-lookup"><span data-stu-id="2618b-119">System.String</span></span>

## <span data-ttu-id="2618b-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2618b-120">OUTPUTS</span></span>

### <span data-ttu-id="2618b-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="2618b-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="2618b-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2618b-122">NOTES</span></span>

## <span data-ttu-id="2618b-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2618b-123">RELATED LINKS</span></span>
