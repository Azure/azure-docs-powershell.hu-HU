---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: dcc0424cd1d6dbd823793a3dc77e813c6e182176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680028"
---
# <span data-ttu-id="19c72-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="19c72-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="19c72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19c72-102">SYNOPSIS</span></span>
<span data-ttu-id="19c72-103">Törli a megadott ASR-replikációs házirendet a helyreállítási szolgáltatások boltozatról.</span><span class="sxs-lookup"><span data-stu-id="19c72-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19c72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19c72-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19c72-105">DESCRIPTION</span></span>
<span data-ttu-id="19c72-106">A **Remove-AzureRmRecoveryServicesAsrPolicy** parancsmag törölte a megadott replikációs házirendet a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="19c72-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="19c72-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19c72-107">EXAMPLES</span></span>

### <span data-ttu-id="19c72-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19c72-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="19c72-109">Elindítja a megadott replikációs házirend törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="19c72-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="19c72-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19c72-110">PARAMETERS</span></span>

### <span data-ttu-id="19c72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c72-111">-DefaultProfile</span></span>
<span data-ttu-id="19c72-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19c72-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="19c72-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19c72-113">-InputObject</span></span>
<span data-ttu-id="19c72-114">A bemeneti objektum a parancsmag: az ASR replikációs házirend-objektuma, amely a törlendő replikációs házirendnek megfelelő.</span><span class="sxs-lookup"><span data-stu-id="19c72-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19c72-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="19c72-115">-Confirm</span></span>
<span data-ttu-id="19c72-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="19c72-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c72-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c72-117">-WhatIf</span></span>
<span data-ttu-id="19c72-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="19c72-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19c72-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19c72-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c72-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c72-120">CommonParameters</span></span>
<span data-ttu-id="19c72-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19c72-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c72-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c72-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c72-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19c72-123">INPUTS</span></span>

### <span data-ttu-id="19c72-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="19c72-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="19c72-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19c72-125">OUTPUTS</span></span>

### <span data-ttu-id="19c72-126">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="19c72-126">System.Object</span></span>

## <span data-ttu-id="19c72-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19c72-127">NOTES</span></span>

## <span data-ttu-id="19c72-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19c72-128">RELATED LINKS</span></span>

[<span data-ttu-id="19c72-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="19c72-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="19c72-130">Új – AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="19c72-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
