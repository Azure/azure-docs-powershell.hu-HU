---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012641"
---
# <span data-ttu-id="5f070-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5f070-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="5f070-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f070-102">SYNOPSIS</span></span>
<span data-ttu-id="5f070-103">Törli a megadott ASR-replikációs házirendet a helyreállítási szolgáltatások boltozatról.</span><span class="sxs-lookup"><span data-stu-id="5f070-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="5f070-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f070-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f070-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f070-105">DESCRIPTION</span></span>
<span data-ttu-id="5f070-106">A **Remove-AzRecoveryServicesAsrPolicy** parancsmag törölte a megadott replikációs házirendet a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="5f070-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="5f070-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5f070-107">EXAMPLES</span></span>

### <span data-ttu-id="5f070-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5f070-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="5f070-109">Elindítja a megadott replikációs házirend törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="5f070-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5f070-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f070-110">PARAMETERS</span></span>

### <span data-ttu-id="5f070-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f070-111">-DefaultProfile</span></span>
<span data-ttu-id="5f070-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f070-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f070-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f070-113">-InputObject</span></span>
<span data-ttu-id="5f070-114">A bemeneti objektum a parancsmag: az ASR replikációs házirend-objektuma, amely a törlendő replikációs házirendnek megfelelő.</span><span class="sxs-lookup"><span data-stu-id="5f070-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="5f070-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f070-115">-Confirm</span></span>
<span data-ttu-id="5f070-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f070-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f070-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f070-117">-WhatIf</span></span>
<span data-ttu-id="5f070-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f070-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f070-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f070-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f070-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f070-120">CommonParameters</span></span>
<span data-ttu-id="5f070-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f070-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f070-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5f070-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f070-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f070-123">INPUTS</span></span>

### <span data-ttu-id="5f070-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="5f070-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="5f070-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f070-125">OUTPUTS</span></span>

### <span data-ttu-id="5f070-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5f070-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5f070-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f070-127">NOTES</span></span>

## <span data-ttu-id="5f070-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f070-128">RELATED LINKS</span></span>

[<span data-ttu-id="5f070-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5f070-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="5f070-130">Új – AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5f070-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
