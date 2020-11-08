---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025067"
---
# <span data-ttu-id="238a0-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="238a0-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="238a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="238a0-102">SYNOPSIS</span></span>
<span data-ttu-id="238a0-103">A push Mobility Service Agent a védett gépekre vonatkozó frissítéseket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="238a0-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="238a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="238a0-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="238a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="238a0-105">DESCRIPTION</span></span>
<span data-ttu-id="238a0-106">Az **Update-AzRecoveryServicesAsrMobilityService** parancsmag megkíséreli a Mobility Service Agent frissítését a védett gépekre (ha van elérhető frissítés).</span><span class="sxs-lookup"><span data-stu-id="238a0-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="238a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="238a0-107">EXAMPLES</span></span>

### <span data-ttu-id="238a0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="238a0-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="238a0-109">Feladat: a replikációs szolgáltatással védett elem Mozgékonysági szolgáltatási ügynökének nyomon követése.</span><span class="sxs-lookup"><span data-stu-id="238a0-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="238a0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="238a0-110">PARAMETERS</span></span>

### <span data-ttu-id="238a0-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="238a0-111">-Account</span></span>
<span data-ttu-id="238a0-112">A frissítés leküldésekor használni kívánt fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="238a0-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="238a0-113">Ahhoz, hogy az ASR-szövetben a Machine Update-nek megfelelő, a Run (Futtatás) fiókból kell lennie.</span><span class="sxs-lookup"><span data-stu-id="238a0-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238a0-114">-DefaultProfile</span></span>
<span data-ttu-id="238a0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="238a0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="238a0-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="238a0-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="238a0-117">Azure webhely-helyreállítási replikációval védett elem frissítése</span><span class="sxs-lookup"><span data-stu-id="238a0-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="238a0-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="238a0-118">-Confirm</span></span>
<span data-ttu-id="238a0-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="238a0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="238a0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="238a0-120">-WhatIf</span></span>
<span data-ttu-id="238a0-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="238a0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="238a0-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="238a0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="238a0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238a0-123">CommonParameters</span></span>
<span data-ttu-id="238a0-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="238a0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238a0-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="238a0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238a0-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="238a0-126">INPUTS</span></span>

### <span data-ttu-id="238a0-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="238a0-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="238a0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="238a0-128">OUTPUTS</span></span>

### <span data-ttu-id="238a0-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="238a0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="238a0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="238a0-130">NOTES</span></span>

## <span data-ttu-id="238a0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="238a0-131">RELATED LINKS</span></span>
