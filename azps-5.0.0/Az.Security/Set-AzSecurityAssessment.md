---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188003"
---
# <span data-ttu-id="7f3fb-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="7f3fb-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="7f3fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3fb-103">Egy erőforrás biztonsági felmérési eredményének létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="7f3fb-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="7f3fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f3fb-104">SYNTAX</span></span>

### <span data-ttu-id="7f3fb-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f3fb-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f3fb-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="7f3fb-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f3fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f3fb-107">DESCRIPTION</span></span>
<span data-ttu-id="7f3fb-108">Egy erőforrás biztonsági felmérési eredményének létrehozása vagy frissítése a meglévő találatok állapotának módosításához vagy további adatforrások hozzáadásához használható.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="7f3fb-109">csak a "CustomerManaged" típusú felmérésekhez használhatók, és csak a kiértékelt felmérési metaadatok létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="7f3fb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7f3fb-110">EXAMPLES</span></span>

### <span data-ttu-id="7f3fb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7f3fb-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="7f3fb-112">Az előfizetés eredményének jelzése "egészségtelen" néven az "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" típus kiértékeléséhez – az értékelés típusáról további információt az assessmentMetadata típusa című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="7f3fb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f3fb-113">PARAMETERS</span></span>

### <span data-ttu-id="7f3fb-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="7f3fb-114">-AdditionalData</span></span>
<span data-ttu-id="7f3fb-115">A vizsgálat eredményéhez a jobb vizsgálatok vagy az állapot egyértelművé tételéhez csatolt adatértékek.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

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

### <span data-ttu-id="7f3fb-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="7f3fb-116">-AssessedResourceId</span></span>
<span data-ttu-id="7f3fb-117">Annak az erőforrásnak a teljes erőforrás-azonosítója, amelyre a felmérést kiszámítja.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="7f3fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3fb-118">-DefaultProfile</span></span>
<span data-ttu-id="7f3fb-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f3fb-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7f3fb-120">-Name</span></span>
<span data-ttu-id="7f3fb-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="7f3fb-121">Resource name.</span></span>

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

### <span data-ttu-id="7f3fb-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="7f3fb-122">-StatusCause</span></span>
<span data-ttu-id="7f3fb-123">Progremmatic kódja az értékelés eredményének okáról.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="7f3fb-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7f3fb-124">-StatusCode</span></span>
<span data-ttu-id="7f3fb-125">Az értékelés eredményének Progremmatic kódja.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="7f3fb-126">lehet "egészséges", "egészségtelen" vagy "NotApplicable"</span><span class="sxs-lookup"><span data-stu-id="7f3fb-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

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

### <span data-ttu-id="7f3fb-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="7f3fb-127">-StatusDescription</span></span>
<span data-ttu-id="7f3fb-128">Az értékelés eredményének olvasható leírása.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="7f3fb-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f3fb-129">-Confirm</span></span>
<span data-ttu-id="7f3fb-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f3fb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f3fb-131">-WhatIf</span></span>
<span data-ttu-id="7f3fb-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f3fb-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f3fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3fb-134">CommonParameters</span></span>
<span data-ttu-id="7f3fb-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f3fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3fb-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7f3fb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3fb-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f3fb-137">INPUTS</span></span>

### <span data-ttu-id="7f3fb-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="7f3fb-138">None</span></span>

## <span data-ttu-id="7f3fb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f3fb-139">OUTPUTS</span></span>

### <span data-ttu-id="7f3fb-140">Microsoft. Azure. commands. Security. models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="7f3fb-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="7f3fb-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f3fb-141">NOTES</span></span>

## <span data-ttu-id="7f3fb-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f3fb-142">RELATED LINKS</span></span>