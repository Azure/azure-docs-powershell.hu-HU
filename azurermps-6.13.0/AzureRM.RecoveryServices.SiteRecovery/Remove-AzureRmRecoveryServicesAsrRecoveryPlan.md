---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b3bedc5c521736ff702f5e7378b4c401a42bce5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672104"
---
# <span data-ttu-id="99928-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="99928-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="99928-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99928-102">SYNOPSIS</span></span>
<span data-ttu-id="99928-103">Törli a megadott ASR-helyreállítási csomagot a helyreállítási szolgáltatások boltozatból.</span><span class="sxs-lookup"><span data-stu-id="99928-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99928-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99928-104">SYNTAX</span></span>

### <span data-ttu-id="99928-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99928-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99928-106">ByName</span><span class="sxs-lookup"><span data-stu-id="99928-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99928-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="99928-107">DESCRIPTION</span></span>
<span data-ttu-id="99928-108">A **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag törli a megadott helyreállítási csomagot a helyreállítási szolgáltatások boltozatból.</span><span class="sxs-lookup"><span data-stu-id="99928-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="99928-109">Példák</span><span class="sxs-lookup"><span data-stu-id="99928-109">EXAMPLES</span></span>

### <span data-ttu-id="99928-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99928-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="99928-111">Elindítja a megadott helyreállítási terv törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="99928-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="99928-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99928-112">PARAMETERS</span></span>

### <span data-ttu-id="99928-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99928-113">-DefaultProfile</span></span>
<span data-ttu-id="99928-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99928-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99928-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99928-115">-InputObject</span></span>
<span data-ttu-id="99928-116">A bemeneti objektum a parancsmag: az ASR-helyreállítási terv objektuma, amely megfelel a törlendő helyreállítási tervnek.</span><span class="sxs-lookup"><span data-stu-id="99928-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99928-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99928-117">-Name</span></span>
<span data-ttu-id="99928-118">A törlendő helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99928-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99928-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99928-119">-Confirm</span></span>
<span data-ttu-id="99928-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99928-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99928-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99928-121">-WhatIf</span></span>
<span data-ttu-id="99928-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99928-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99928-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99928-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99928-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99928-124">CommonParameters</span></span>
<span data-ttu-id="99928-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99928-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99928-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99928-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99928-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99928-127">INPUTS</span></span>

### <span data-ttu-id="99928-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="99928-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="99928-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99928-129">OUTPUTS</span></span>

### <span data-ttu-id="99928-130">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="99928-130">System.Object</span></span>

## <span data-ttu-id="99928-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99928-131">NOTES</span></span>

## <span data-ttu-id="99928-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99928-132">RELATED LINKS</span></span>

[<span data-ttu-id="99928-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="99928-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="99928-134">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="99928-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="99928-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="99928-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


