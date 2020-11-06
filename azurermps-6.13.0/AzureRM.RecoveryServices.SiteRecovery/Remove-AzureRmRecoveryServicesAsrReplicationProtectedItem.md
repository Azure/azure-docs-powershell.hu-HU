---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bd8a06eb85658fe2ec06d65c0663550be78d1552
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492793"
---
# <span data-ttu-id="9238d-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9238d-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="9238d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9238d-102">SYNOPSIS</span></span>
<span data-ttu-id="9238d-103">Az Azure webhely-helyreállítási replikációval védett elem replikációjának leállítása/letiltása.</span><span class="sxs-lookup"><span data-stu-id="9238d-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9238d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9238d-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9238d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9238d-105">DESCRIPTION</span></span>
<span data-ttu-id="9238d-106">A **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag letiltja a megadott Azure-helyreállítási replikációval védett elem replikálását.</span><span class="sxs-lookup"><span data-stu-id="9238d-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="9238d-107">A művelet hatására a replikáció leáll a védett elemen.</span><span class="sxs-lookup"><span data-stu-id="9238d-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="9238d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9238d-108">EXAMPLES</span></span>

### <span data-ttu-id="9238d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9238d-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="9238d-110">Elindítja a replikáció letiltása műveletet a megadott replikációs védett elemhez, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9238d-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9238d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9238d-111">PARAMETERS</span></span>

### <span data-ttu-id="9238d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9238d-112">-DefaultProfile</span></span>
<span data-ttu-id="9238d-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9238d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9238d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9238d-114">-Force</span></span>
<span data-ttu-id="9238d-115">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="9238d-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="9238d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9238d-116">-InputObject</span></span>
<span data-ttu-id="9238d-117">A bemeneti objektum a parancsmag: az ASR-replikációs szolgáltatással védett elem objektum, amely megfelel a replikációt letiltó replikációs védelemmel ellátott elemnek.</span><span class="sxs-lookup"><span data-stu-id="9238d-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="9238d-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="9238d-118">-WaitForCompletion</span></span>
<span data-ttu-id="9238d-119">Azt jelzi, hogy a parancsmagnak várnia kell, hogy a művelet csak a visszatérés előtt legyen végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="9238d-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="9238d-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9238d-120">-Confirm</span></span>
<span data-ttu-id="9238d-121">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="9238d-121">Specify if confirmation is required.</span></span> <span data-ttu-id="9238d-122">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="9238d-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="9238d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9238d-123">-WhatIf</span></span>
<span data-ttu-id="9238d-124">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="9238d-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="9238d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9238d-125">CommonParameters</span></span>
<span data-ttu-id="9238d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9238d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9238d-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9238d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9238d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9238d-128">INPUTS</span></span>

### <span data-ttu-id="9238d-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9238d-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9238d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9238d-130">OUTPUTS</span></span>

### <span data-ttu-id="9238d-131">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9238d-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9238d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9238d-132">NOTES</span></span>

## <span data-ttu-id="9238d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9238d-133">RELATED LINKS</span></span>

[<span data-ttu-id="9238d-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9238d-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9238d-135">Új – AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9238d-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="9238d-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9238d-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
