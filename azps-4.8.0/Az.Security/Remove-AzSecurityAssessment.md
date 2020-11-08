---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183970"
---
# <span data-ttu-id="052a3-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="052a3-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="052a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="052a3-102">SYNOPSIS</span></span>
<span data-ttu-id="052a3-103">Egy biztonsági felmérés eredményének törlése az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="052a3-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="052a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="052a3-104">SYNTAX</span></span>

### <span data-ttu-id="052a3-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="052a3-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052a3-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="052a3-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052a3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="052a3-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052a3-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="052a3-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="052a3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="052a3-109">DESCRIPTION</span></span>
<span data-ttu-id="052a3-110">Törli a biztonsági vizsgálat eredményét egy előfizetésből, amely általában akkor használatos, amikor egy resoruce törlődik, vagy ha az értékelés nem releváns egy adott erőforrásnál.</span><span class="sxs-lookup"><span data-stu-id="052a3-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="052a3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="052a3-111">EXAMPLES</span></span>

### <span data-ttu-id="052a3-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="052a3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="052a3-113">A felmérés eredményének törlése az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="052a3-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="052a3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="052a3-114">PARAMETERS</span></span>

### <span data-ttu-id="052a3-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="052a3-115">-AssessedResourceId</span></span>
<span data-ttu-id="052a3-116">Annak az erőforrásnak a teljes erőforrás-azonosítója, amelyre a felmérést kiszámítja.</span><span class="sxs-lookup"><span data-stu-id="052a3-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052a3-117">-DefaultProfile</span></span>
<span data-ttu-id="052a3-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="052a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="052a3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="052a3-119">-InputObject</span></span>
<span data-ttu-id="052a3-120">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="052a3-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="052a3-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="052a3-121">-Name</span></span>
<span data-ttu-id="052a3-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="052a3-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052a3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="052a3-123">-PassThru</span></span>
<span data-ttu-id="052a3-124">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="052a3-124">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="052a3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="052a3-125">-ResourceId</span></span>
<span data-ttu-id="052a3-126">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="052a3-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="052a3-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="052a3-127">-Confirm</span></span>
<span data-ttu-id="052a3-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="052a3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="052a3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="052a3-129">-WhatIf</span></span>
<span data-ttu-id="052a3-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="052a3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="052a3-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="052a3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="052a3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052a3-132">CommonParameters</span></span>
<span data-ttu-id="052a3-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="052a3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052a3-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="052a3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052a3-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="052a3-135">INPUTS</span></span>

### <span data-ttu-id="052a3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="052a3-136">System.String</span></span>

### <span data-ttu-id="052a3-137">Microsoft. Azure. commands. Security. models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="052a3-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="052a3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="052a3-138">OUTPUTS</span></span>

### <span data-ttu-id="052a3-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="052a3-139">System.Boolean</span></span>

## <span data-ttu-id="052a3-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="052a3-140">NOTES</span></span>

## <span data-ttu-id="052a3-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="052a3-141">RELATED LINKS</span></span>
