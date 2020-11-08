---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195172"
---
# <span data-ttu-id="13d1c-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="13d1c-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="13d1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="13d1c-103">A biztonsági felmérések típusai és metadta az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="13d1c-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="13d1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13d1c-104">SYNTAX</span></span>

### <span data-ttu-id="13d1c-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13d1c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d1c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="13d1c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d1c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13d1c-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13d1c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="13d1c-108">DESCRIPTION</span></span>
<span data-ttu-id="13d1c-109">A biztonsági felmérések típusai és metadta az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="13d1c-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="13d1c-110">A biztonsági felmérés metaadatai között szerepel a felhasználó által definiált Built-In felmérések és egyéni értékelési típusok.</span><span class="sxs-lookup"><span data-stu-id="13d1c-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="13d1c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="13d1c-111">EXAMPLES</span></span>

### <span data-ttu-id="13d1c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13d1c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="13d1c-113">Beolvassa az összes beépített felmérést és a jelenlegi előfizetésben konfigurált egyéni felméréseket.</span><span class="sxs-lookup"><span data-stu-id="13d1c-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="13d1c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13d1c-114">PARAMETERS</span></span>

### <span data-ttu-id="13d1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d1c-115">-DefaultProfile</span></span>
<span data-ttu-id="13d1c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13d1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d1c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13d1c-117">-Name</span></span>
<span data-ttu-id="13d1c-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="13d1c-118">Resource name.</span></span>

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

### <span data-ttu-id="13d1c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13d1c-119">-ResourceId</span></span>
<span data-ttu-id="13d1c-120">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="13d1c-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="13d1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d1c-121">CommonParameters</span></span>
<span data-ttu-id="13d1c-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13d1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d1c-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="13d1c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d1c-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d1c-124">INPUTS</span></span>

### <span data-ttu-id="13d1c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="13d1c-125">System.String</span></span>

## <span data-ttu-id="13d1c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d1c-126">OUTPUTS</span></span>

### <span data-ttu-id="13d1c-127">Microsoft. Azure. commands. Security. models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="13d1c-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="13d1c-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13d1c-128">NOTES</span></span>

## <span data-ttu-id="13d1c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13d1c-129">RELATED LINKS</span></span>
