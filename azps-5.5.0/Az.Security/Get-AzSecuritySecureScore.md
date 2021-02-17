---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156403"
---
# <span data-ttu-id="7e747-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="7e747-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="7e747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e747-102">SYNOPSIS</span></span>
<span data-ttu-id="7e747-103">Biztonsági biztonsági pontszámokat és azok eredményeit kapja meg egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="7e747-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="7e747-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e747-104">SYNTAX</span></span>

### <span data-ttu-id="7e747-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e747-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e747-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7e747-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e747-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e747-107">EXAMPLES</span></span>

### <span data-ttu-id="7e747-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7e747-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="7e747-109">Lekérte az összes biztonsági pontszámot egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="7e747-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="7e747-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e747-110">PARAMETERS</span></span>

### <span data-ttu-id="7e747-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e747-111">-DefaultProfile</span></span>
<span data-ttu-id="7e747-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e747-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e747-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7e747-113">-Name</span></span>
<span data-ttu-id="7e747-114">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="7e747-114">Resource name.</span></span>

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

### <span data-ttu-id="7e747-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e747-115">CommonParameters</span></span>
<span data-ttu-id="7e747-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e747-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e747-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e747-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e747-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e747-118">INPUTS</span></span>

### <span data-ttu-id="7e747-119">System.String</span><span class="sxs-lookup"><span data-stu-id="7e747-119">System.String</span></span>

## <span data-ttu-id="7e747-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e747-120">OUTPUTS</span></span>

### <span data-ttu-id="7e747-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="7e747-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="7e747-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e747-122">NOTES</span></span>

## <span data-ttu-id="7e747-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e747-123">RELATED LINKS</span></span>
