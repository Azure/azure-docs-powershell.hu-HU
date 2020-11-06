---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 9c336602aebdb82e4860ee744fb99f3a6fbf5a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493039"
---
# <span data-ttu-id="54228-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="54228-101">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="54228-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54228-102">SYNOPSIS</span></span>
<span data-ttu-id="54228-103">Elindítja a replikációs újraszinkronizálást.</span><span class="sxs-lookup"><span data-stu-id="54228-103">Starts replication resynchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54228-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54228-104">SYNTAX</span></span>

### <span data-ttu-id="54228-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54228-105">Default (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54228-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="54228-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54228-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="54228-107">DESCRIPTION</span></span>
<span data-ttu-id="54228-108">A **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** parancsmag a megadott védett elem replikációjának újraszinkronizálását indítja el, ha a védett állapot újraszinkronizálása kötelező.</span><span class="sxs-lookup"><span data-stu-id="54228-108">The **Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="54228-109">Példák</span><span class="sxs-lookup"><span data-stu-id="54228-109">EXAMPLES</span></span>

### <span data-ttu-id="54228-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54228-110">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="54228-111">Elindítja a feladatot, hogy újraszinkronizálja a replikálást az átadott replikációs szolgáltatással védett elemeken.</span><span class="sxs-lookup"><span data-stu-id="54228-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="54228-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54228-112">PARAMETERS</span></span>

### <span data-ttu-id="54228-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54228-113">-Confirm</span></span>
<span data-ttu-id="54228-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54228-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54228-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54228-115">-DefaultProfile</span></span>
<span data-ttu-id="54228-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54228-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54228-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="54228-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="54228-118">Az ASR-replikációval védett elem a replikáció újraszinkronizálásához.</span><span class="sxs-lookup"><span data-stu-id="54228-118">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54228-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54228-119">-ResourceId</span></span>
<span data-ttu-id="54228-120">Az újraszinkronizáláshoz a replikációs védelemmel ellátott elem erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54228-120">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54228-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54228-121">-WhatIf</span></span>
<span data-ttu-id="54228-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54228-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54228-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54228-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54228-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54228-124">CommonParameters</span></span>
<span data-ttu-id="54228-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54228-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54228-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54228-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54228-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54228-127">INPUTS</span></span>

### <span data-ttu-id="54228-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="54228-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="54228-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54228-129">OUTPUTS</span></span>

### <span data-ttu-id="54228-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="54228-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="54228-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54228-131">NOTES</span></span>

## <span data-ttu-id="54228-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54228-132">RELATED LINKS</span></span>
