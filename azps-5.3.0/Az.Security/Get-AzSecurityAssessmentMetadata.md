---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479793"
---
# <span data-ttu-id="91bad-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="91bad-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="91bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91bad-102">SYNOPSIS</span></span>
<span data-ttu-id="91bad-103">Biztonsági felméréstípusokat és metadtát kap egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="91bad-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="91bad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91bad-104">SYNTAX</span></span>

### <span data-ttu-id="91bad-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91bad-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91bad-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="91bad-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91bad-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="91bad-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91bad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91bad-108">DESCRIPTION</span></span>
<span data-ttu-id="91bad-109">Biztonsági felméréstípusokat és metadtát kap egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="91bad-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="91bad-110">A biztonsági felmérés metaadatai Built-In és egyéni felmérési típusokat tartalmaznak, amelyek a felhasználó által definiálhatóak.</span><span class="sxs-lookup"><span data-stu-id="91bad-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="91bad-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91bad-111">EXAMPLES</span></span>

### <span data-ttu-id="91bad-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="91bad-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="91bad-113">Beállítja az aktuális előfizetéshez konfigurált beépített felméréseket és egyéni felméréseket.</span><span class="sxs-lookup"><span data-stu-id="91bad-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="91bad-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91bad-114">PARAMETERS</span></span>

### <span data-ttu-id="91bad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91bad-115">-DefaultProfile</span></span>
<span data-ttu-id="91bad-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91bad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91bad-117">-Name</span><span class="sxs-lookup"><span data-stu-id="91bad-117">-Name</span></span>
<span data-ttu-id="91bad-118">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="91bad-118">Resource name.</span></span>

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

### <span data-ttu-id="91bad-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91bad-119">-ResourceId</span></span>
<span data-ttu-id="91bad-120">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="91bad-120">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91bad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91bad-121">CommonParameters</span></span>
<span data-ttu-id="91bad-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91bad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91bad-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91bad-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91bad-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91bad-124">INPUTS</span></span>

### <span data-ttu-id="91bad-125">System.String</span><span class="sxs-lookup"><span data-stu-id="91bad-125">System.String</span></span>

## <span data-ttu-id="91bad-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91bad-126">OUTPUTS</span></span>

### <span data-ttu-id="91bad-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="91bad-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="91bad-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91bad-128">NOTES</span></span>

## <span data-ttu-id="91bad-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91bad-129">RELATED LINKS</span></span>
