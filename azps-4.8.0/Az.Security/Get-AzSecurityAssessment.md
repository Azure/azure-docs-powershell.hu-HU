---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024468"
---
# <span data-ttu-id="a71de-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a71de-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="a71de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a71de-102">SYNOPSIS</span></span>
<span data-ttu-id="a71de-103">Biztonsági felmérések és eredményeik befizetése az előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="a71de-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="a71de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a71de-104">SYNTAX</span></span>

### <span data-ttu-id="a71de-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a71de-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a71de-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a71de-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a71de-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="a71de-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a71de-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a71de-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a71de-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a71de-109">DESCRIPTION</span></span>
<span data-ttu-id="a71de-110">Megkapja a biztonsági felmérést és a találatokat az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a71de-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="a71de-111">A biztonsági felmérések segítségével megtudhatja, hogy az Azure Security Center mely ajánlott eljárásokat fogja csökkenteni az Azure-előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="a71de-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="a71de-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a71de-112">EXAMPLES</span></span>

### <span data-ttu-id="a71de-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a71de-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="a71de-114">Minden biztonsági felmérés beolvasása egy előfizetésben</span><span class="sxs-lookup"><span data-stu-id="a71de-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="a71de-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a71de-115">PARAMETERS</span></span>

### <span data-ttu-id="a71de-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a71de-116">-AssessedResourceId</span></span>
<span data-ttu-id="a71de-117">Annak az erőforrásnak a teljes erőforrás-azonosítója, amelyre a felmérést kiszámítja.</span><span class="sxs-lookup"><span data-stu-id="a71de-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a71de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71de-118">-DefaultProfile</span></span>
<span data-ttu-id="a71de-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a71de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a71de-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a71de-120">-Name</span></span>
<span data-ttu-id="a71de-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="a71de-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71de-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a71de-122">-ResourceId</span></span>
<span data-ttu-id="a71de-123">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="a71de-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a71de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71de-124">CommonParameters</span></span>
<span data-ttu-id="a71de-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a71de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71de-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a71de-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71de-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a71de-127">INPUTS</span></span>

### <span data-ttu-id="a71de-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a71de-128">System.String</span></span>

## <span data-ttu-id="a71de-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a71de-129">OUTPUTS</span></span>

### <span data-ttu-id="a71de-130">Microsoft. Azure. commands. Security. models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a71de-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="a71de-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a71de-131">NOTES</span></span>

## <span data-ttu-id="a71de-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a71de-132">RELATED LINKS</span></span>
