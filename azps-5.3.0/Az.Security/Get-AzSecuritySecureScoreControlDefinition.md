---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479780"
---
# <span data-ttu-id="57697-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="57697-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="57697-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57697-102">SYNOPSIS</span></span>
<span data-ttu-id="57697-103">Biztonsági pontszám-definíciókat kap egy előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="57697-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="57697-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57697-104">SYNTAX</span></span>

### <span data-ttu-id="57697-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57697-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57697-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="57697-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57697-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57697-107">EXAMPLES</span></span>

### <span data-ttu-id="57697-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="57697-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="57697-109">Az előfizetés biztonsági biztonsági pontszám-vezérlődefiníciói</span><span class="sxs-lookup"><span data-stu-id="57697-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="57697-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57697-110">PARAMETERS</span></span>

### <span data-ttu-id="57697-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57697-111">-DefaultProfile</span></span>
<span data-ttu-id="57697-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57697-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57697-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57697-113">CommonParameters</span></span>
<span data-ttu-id="57697-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57697-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57697-115">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57697-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57697-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57697-116">INPUTS</span></span>

### <span data-ttu-id="57697-117">System.String</span><span class="sxs-lookup"><span data-stu-id="57697-117">System.String</span></span>

## <span data-ttu-id="57697-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57697-118">OUTPUTS</span></span>

### <span data-ttu-id="57697-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="57697-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="57697-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57697-120">NOTES</span></span>

## <span data-ttu-id="57697-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57697-121">RELATED LINKS</span></span>
