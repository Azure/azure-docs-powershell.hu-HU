---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d6c93a6ca54a67c13fcba54a11d9f30c61377e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679671"
---
# <span data-ttu-id="ef1ea-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ef1ea-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="ef1ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1ea-103">Webhely-helyreállítási csomag eltávolítása a webhely-helyreállításból.</span><span class="sxs-lookup"><span data-stu-id="ef1ea-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef1ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef1ea-104">SYNTAX</span></span>

### <span data-ttu-id="ef1ea-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef1ea-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef1ea-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ef1ea-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef1ea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef1ea-107">DESCRIPTION</span></span>
<span data-ttu-id="ef1ea-108">A **Remove-AzureRmSiteRecoveryRecoveryPlan** parancsmag eltávolítja a webhely-helyreállítási csomagot az Azure jelenlegi helyreállítási webhelyről.</span><span class="sxs-lookup"><span data-stu-id="ef1ea-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="ef1ea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef1ea-109">EXAMPLES</span></span>

### <span data-ttu-id="ef1ea-110">1. példa: helyreállítási terv eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ef1ea-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="ef1ea-111">Az első parancs az Get-AzureRmSiteRecoveryRecoveryPlan parancsmagot használja a webhely-helyreállítási terv beszerzéséhez, majd a $RecoveryPlan változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ef1ea-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="ef1ea-112">A második parancs eltávolítja az $RecoveryPlan helyreállítási tervét.</span><span class="sxs-lookup"><span data-stu-id="ef1ea-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="ef1ea-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef1ea-113">PARAMETERS</span></span>

### <span data-ttu-id="ef1ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1ea-114">-DefaultProfile</span></span>
<span data-ttu-id="ef1ea-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef1ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef1ea-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef1ea-116">-Name</span></span>
<span data-ttu-id="ef1ea-117">Annak a helyreállítási tervnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ef1ea-117">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef1ea-118">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ef1ea-118">-RecoveryPlan</span></span>
<span data-ttu-id="ef1ea-119">Azt a helyreállítási tervet adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ef1ea-119">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef1ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1ea-120">CommonParameters</span></span>
<span data-ttu-id="ef1ea-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef1ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1ea-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1ea-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef1ea-123">INPUTS</span></span>

### <span data-ttu-id="ef1ea-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ef1ea-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="ef1ea-125">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ef1ea-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="ef1ea-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef1ea-126">OUTPUTS</span></span>

## <span data-ttu-id="ef1ea-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef1ea-127">NOTES</span></span>

## <span data-ttu-id="ef1ea-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef1ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="ef1ea-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ef1ea-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ef1ea-130">Új – AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ef1ea-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ef1ea-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ef1ea-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


