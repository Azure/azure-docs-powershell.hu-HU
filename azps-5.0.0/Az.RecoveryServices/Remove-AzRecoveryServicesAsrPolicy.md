---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188043"
---
# <span data-ttu-id="281e1-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="281e1-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="281e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="281e1-102">SYNOPSIS</span></span>
<span data-ttu-id="281e1-103">Törli a megadott ASR-replikációs házirendet a helyreállítási szolgáltatások boltozatról.</span><span class="sxs-lookup"><span data-stu-id="281e1-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="281e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="281e1-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="281e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="281e1-105">DESCRIPTION</span></span>
<span data-ttu-id="281e1-106">A **Remove-AzRecoveryServicesAsrPolicy** parancsmag törölte a megadott replikációs házirendet a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="281e1-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="281e1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="281e1-107">EXAMPLES</span></span>

### <span data-ttu-id="281e1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="281e1-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="281e1-109">Elindítja a megadott replikációs házirend törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="281e1-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="281e1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="281e1-110">PARAMETERS</span></span>

### <span data-ttu-id="281e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="281e1-111">-DefaultProfile</span></span>
<span data-ttu-id="281e1-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="281e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="281e1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="281e1-113">-InputObject</span></span>
<span data-ttu-id="281e1-114">A bemeneti objektum a parancsmag: az ASR replikációs házirend-objektuma, amely a törlendő replikációs házirendnek megfelelő.</span><span class="sxs-lookup"><span data-stu-id="281e1-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="281e1-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="281e1-115">-Confirm</span></span>
<span data-ttu-id="281e1-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="281e1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="281e1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="281e1-117">-WhatIf</span></span>
<span data-ttu-id="281e1-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="281e1-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="281e1-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="281e1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="281e1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281e1-120">CommonParameters</span></span>
<span data-ttu-id="281e1-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="281e1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281e1-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="281e1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281e1-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="281e1-123">INPUTS</span></span>

### <span data-ttu-id="281e1-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="281e1-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="281e1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="281e1-125">OUTPUTS</span></span>

### <span data-ttu-id="281e1-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="281e1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="281e1-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="281e1-127">NOTES</span></span>

## <span data-ttu-id="281e1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="281e1-128">RELATED LINKS</span></span>

[<span data-ttu-id="281e1-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="281e1-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="281e1-130">Új – AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="281e1-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
