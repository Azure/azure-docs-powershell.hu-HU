---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 876d30cd3c046136acc24a8492425c69fc845f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494413"
---
# <span data-ttu-id="d32b8-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d32b8-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="d32b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d32b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d32b8-103">A védelemmel ellátott elemek beolvasása az ASR-védelmi tárolóban</span><span class="sxs-lookup"><span data-stu-id="d32b8-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d32b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d32b8-104">SYNTAX</span></span>

### <span data-ttu-id="d32b8-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d32b8-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d32b8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d32b8-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d32b8-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d32b8-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d32b8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d32b8-108">DESCRIPTION</span></span>
<span data-ttu-id="d32b8-109">A **Get-AzureRmRecoveryServicesAsrProtectableItem** parancsmag az Azure webhely-helyreállítási védelmi tárolóban található védelemmel ellátott elemeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d32b8-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d32b8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d32b8-110">EXAMPLES</span></span>

### <span data-ttu-id="d32b8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d32b8-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="d32b8-112">A megadott ASR-védelmi tároló minden védett elemének beolvasása</span><span class="sxs-lookup"><span data-stu-id="d32b8-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="d32b8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d32b8-113">Example 2</span></span>
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

<span data-ttu-id="d32b8-114">A védelemmel ellátott elemek beszerzése meghatározott ASR-védelmi tárolóban és az adott felhasználóbarát névvel</span><span class="sxs-lookup"><span data-stu-id="d32b8-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="d32b8-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="d32b8-115">Example 3</span></span>
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

<span data-ttu-id="d32b8-116">A megadott ASR-védelmi tároló minden védett elemének beolvasása</span><span class="sxs-lookup"><span data-stu-id="d32b8-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="d32b8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d32b8-117">PARAMETERS</span></span>

### <span data-ttu-id="d32b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d32b8-118">-DefaultProfile</span></span>
<span data-ttu-id="d32b8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d32b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="d32b8-120">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="d32b8-120">-FriendlyName</span></span>
<span data-ttu-id="d32b8-121">Az ASR-védelemmel ellátott elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32b8-121">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32b8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d32b8-122">-Name</span></span>
<span data-ttu-id="d32b8-123">Az ASR-védelemmel ellátott elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32b8-123">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d32b8-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d32b8-124">-ProtectionContainer</span></span>
<span data-ttu-id="d32b8-125">Az Azure site Recovery Protection Container objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32b8-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d32b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32b8-126">CommonParameters</span></span>
<span data-ttu-id="d32b8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d32b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32b8-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d32b8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32b8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d32b8-129">INPUTS</span></span>

### <span data-ttu-id="d32b8-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d32b8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d32b8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d32b8-131">OUTPUTS</span></span>

### <span data-ttu-id="d32b8-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d32b8-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d32b8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d32b8-133">NOTES</span></span>

## <span data-ttu-id="d32b8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d32b8-134">RELATED LINKS</span></span>

[<span data-ttu-id="d32b8-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d32b8-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="d32b8-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d32b8-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
