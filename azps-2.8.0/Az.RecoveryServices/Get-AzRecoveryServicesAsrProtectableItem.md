---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 4ea8bcb0e27c9ca44cc30f36005bdcccdbd20d61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838619"
---
# <span data-ttu-id="dc3e5-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="dc3e5-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="dc3e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3e5-103">A védelemmel ellátott elemek beolvasása az ASR-védelmi tárolóban</span><span class="sxs-lookup"><span data-stu-id="dc3e5-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="dc3e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc3e5-104">SYNTAX</span></span>

### <span data-ttu-id="dc3e5-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc3e5-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc3e5-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="dc3e5-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc3e5-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="dc3e5-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc3e5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc3e5-108">DESCRIPTION</span></span>
<span data-ttu-id="dc3e5-109">A **Get-AzRecoveryServicesAsrProtectableItem** parancsmag az Azure webhely-helyreállítási védelmi tárolóban található védelemmel ellátott elemeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dc3e5-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="dc3e5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dc3e5-110">EXAMPLES</span></span>

### <span data-ttu-id="dc3e5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dc3e5-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="dc3e5-112">A megadott ASR-védelmi tároló minden védett elemének beolvasása</span><span class="sxs-lookup"><span data-stu-id="dc3e5-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="dc3e5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="dc3e5-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="dc3e5-114">A védelemmel ellátott elemek beszerzése meghatározott ASR-védelmi tárolóban és az adott felhasználóbarát névvel</span><span class="sxs-lookup"><span data-stu-id="dc3e5-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="dc3e5-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="dc3e5-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="dc3e5-116">A megadott ASR-védelmi tároló minden védett elemének beolvasása</span><span class="sxs-lookup"><span data-stu-id="dc3e5-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="dc3e5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc3e5-117">PARAMETERS</span></span>

### <span data-ttu-id="dc3e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3e5-118">-DefaultProfile</span></span>
<span data-ttu-id="dc3e5-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc3e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dc3e5-120">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="dc3e5-120">-FriendlyName</span></span>
<span data-ttu-id="dc3e5-121">Az ASR-védelemmel ellátott elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc3e5-121">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3e5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc3e5-122">-Name</span></span>
<span data-ttu-id="dc3e5-123">Az ASR-védelemmel ellátott elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc3e5-123">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3e5-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dc3e5-124">-ProtectionContainer</span></span>
<span data-ttu-id="dc3e5-125">Az Azure site Recovery Protection Container objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc3e5-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc3e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3e5-126">CommonParameters</span></span>
<span data-ttu-id="dc3e5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc3e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3e5-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3e5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3e5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc3e5-129">INPUTS</span></span>

### <span data-ttu-id="dc3e5-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dc3e5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="dc3e5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc3e5-131">OUTPUTS</span></span>

### <span data-ttu-id="dc3e5-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="dc3e5-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="dc3e5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc3e5-133">NOTES</span></span>

## <span data-ttu-id="dc3e5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc3e5-134">RELATED LINKS</span></span>

[<span data-ttu-id="dc3e5-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="dc3e5-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="dc3e5-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="dc3e5-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
