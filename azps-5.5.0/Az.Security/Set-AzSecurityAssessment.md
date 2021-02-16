---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208230"
---
# <span data-ttu-id="1ef9f-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="1ef9f-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="1ef9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ef9f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef9f-103">Biztonsági felmérési eredmény létrehozása vagy frissítése erőforráson</span><span class="sxs-lookup"><span data-stu-id="1ef9f-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="1ef9f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ef9f-104">SYNTAX</span></span>

### <span data-ttu-id="1ef9f-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ef9f-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef9f-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="1ef9f-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ef9f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ef9f-107">DESCRIPTION</span></span>
<span data-ttu-id="1ef9f-108">Létrehozhat vagy frissíthet egy biztonsági felmérési eredményt egy erőforráson, módosíthatja egy meglévő eredmény állapotát, vagy további adatokat adhat hozzá.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="1ef9f-109">Csak a "CustomerManaged" típusú felmérési típusokhoz használhatók, és csak a megfelelő felmérési metaadatok létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="1ef9f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ef9f-110">EXAMPLES</span></span>

### <span data-ttu-id="1ef9f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1ef9f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="1ef9f-112">Az előfizetés eredményét "Nem megfelelőként" jelöli meg a "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" típusú értékeléshez – további részleteket a felméréstípusról az AssessmentMetadata típus alatt talál.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="1ef9f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ef9f-113">PARAMETERS</span></span>

### <span data-ttu-id="1ef9f-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="1ef9f-114">-AdditionalData</span></span>
<span data-ttu-id="1ef9f-115">Az értékelés eredményéhez csatolt adatok a jobb vizsgálatok vagy az állapot érthetősége érdekében.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef9f-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="1ef9f-116">-AssessedResourceId</span></span>
<span data-ttu-id="1ef9f-117">Annak az erőforrásnak a teljes erőforrás-azonosítója, amely alapján a felmérést kiszámították.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef9f-118">-DefaultProfile</span></span>
<span data-ttu-id="1ef9f-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ef9f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1ef9f-120">-Name</span></span>
<span data-ttu-id="1ef9f-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef9f-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="1ef9f-122">-StatusCause</span></span>
<span data-ttu-id="1ef9f-123">Progremmatic code for the cause of the assessment's result.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-123">Progremmatic code for the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef9f-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1ef9f-124">-StatusCode</span></span>
<span data-ttu-id="1ef9f-125">Progremmatic code for the result of the assessment.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="1ef9f-126">Lehet "Egészséges", "Nem egészséges" vagy "Nem Alkalmazható"</span><span class="sxs-lookup"><span data-stu-id="1ef9f-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef9f-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="1ef9f-127">-StatusDescription</span></span>
<span data-ttu-id="1ef9f-128">A felmérés eredményének okának emberi olvasható leírása.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-128">Human readable description of the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef9f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ef9f-129">-Confirm</span></span>
<span data-ttu-id="1ef9f-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef9f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ef9f-131">-WhatIf</span></span>
<span data-ttu-id="1ef9f-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ef9f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef9f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef9f-134">CommonParameters</span></span>
<span data-ttu-id="1ef9f-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ef9f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef9f-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ef9f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef9f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ef9f-137">INPUTS</span></span>

### <span data-ttu-id="1ef9f-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="1ef9f-138">None</span></span>

## <span data-ttu-id="1ef9f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ef9f-139">OUTPUTS</span></span>

### <span data-ttu-id="1ef9f-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="1ef9f-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="1ef9f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ef9f-141">NOTES</span></span>

## <span data-ttu-id="1ef9f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ef9f-142">RELATED LINKS</span></span>
