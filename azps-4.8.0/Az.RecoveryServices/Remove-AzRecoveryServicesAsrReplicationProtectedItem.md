---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182184"
---
# <span data-ttu-id="d8ffe-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8ffe-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="d8ffe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ffe-103">Az Azure webhely-helyreállítási replikációval védett elem replikációjának leállítása/letiltása.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="d8ffe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8ffe-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8ffe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ffe-106">A **Remove-AzRecoveryServicesAsrReplicationProtectedItem** parancsmag letiltja a megadott Azure-helyreállítási replikációval védett elem replikálását.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="d8ffe-107">A művelet hatására a replikáció leáll a védett elemen.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="d8ffe-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d8ffe-108">EXAMPLES</span></span>

### <span data-ttu-id="d8ffe-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d8ffe-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="d8ffe-110">Elindítja a replikáció letiltása műveletet a megadott replikációs védett elemhez, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d8ffe-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8ffe-111">PARAMETERS</span></span>

### <span data-ttu-id="d8ffe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ffe-112">-DefaultProfile</span></span>
<span data-ttu-id="d8ffe-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d8ffe-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d8ffe-114">-Force</span></span>
<span data-ttu-id="d8ffe-115">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-115">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ffe-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8ffe-116">-InputObject</span></span>
<span data-ttu-id="d8ffe-117">A bemeneti objektum a parancsmag: az ASR-replikációs szolgáltatással védett elem objektum, amely megfelel a replikációt letiltó replikációs védelemmel ellátott elemnek.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8ffe-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d8ffe-118">-WaitForCompletion</span></span>
<span data-ttu-id="d8ffe-119">Azt jelzi, hogy a parancsmagnak várnia kell, hogy a művelet csak a visszatérés előtt legyen végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ffe-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8ffe-120">-Confirm</span></span>
<span data-ttu-id="d8ffe-121">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-121">Specify if confirmation is required.</span></span> <span data-ttu-id="d8ffe-122">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="d8ffe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ffe-123">-WhatIf</span></span>
<span data-ttu-id="d8ffe-124">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="d8ffe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ffe-125">CommonParameters</span></span>
<span data-ttu-id="d8ffe-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8ffe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ffe-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d8ffe-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ffe-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8ffe-128">INPUTS</span></span>

### <span data-ttu-id="d8ffe-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8ffe-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d8ffe-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8ffe-130">OUTPUTS</span></span>

### <span data-ttu-id="d8ffe-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d8ffe-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d8ffe-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8ffe-132">NOTES</span></span>

## <span data-ttu-id="d8ffe-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8ffe-133">RELATED LINKS</span></span>

[<span data-ttu-id="d8ffe-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8ffe-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d8ffe-135">Új – AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8ffe-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d8ffe-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8ffe-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
