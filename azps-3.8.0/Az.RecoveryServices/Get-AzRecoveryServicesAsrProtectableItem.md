---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: da9dd3d7b1ed0a54a34fdf5c8a0c9d65b507a07b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400603"
---
# <span data-ttu-id="c6836-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c6836-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="c6836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6836-102">SYNOPSIS</span></span>
<span data-ttu-id="c6836-103">Szerezze be a védett elemeket egy ASR védelmi tárolóban.</span><span class="sxs-lookup"><span data-stu-id="c6836-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="c6836-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c6836-104">SYNTAX</span></span>

### <span data-ttu-id="c6836-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6836-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6836-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c6836-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6836-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c6836-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6836-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c6836-108">DESCRIPTION</span></span>
<span data-ttu-id="c6836-109">A **Get-AzRecoveryServicesAsrProtectableItem** parancsmag egy Azure-webhely-helyreállítási védelmi tárolóban kapja meg a védett elemeket.</span><span class="sxs-lookup"><span data-stu-id="c6836-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="c6836-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c6836-110">EXAMPLES</span></span>

### <span data-ttu-id="c6836-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c6836-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="c6836-112">Beveszi a megadott ASR védelmi tárolóban lévő összes védett elemet.</span><span class="sxs-lookup"><span data-stu-id="c6836-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="c6836-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c6836-113">Example 2</span></span>
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

<span data-ttu-id="c6836-114">Szerezze be a védett elemeket a megadott ASR védelmi tárolóban, és a megadott rövid névvel.</span><span class="sxs-lookup"><span data-stu-id="c6836-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="c6836-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="c6836-115">Example 3</span></span>
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

<span data-ttu-id="c6836-116">Beveszi a megadott ASR védelmi tárolóban lévő összes védett elemet.</span><span class="sxs-lookup"><span data-stu-id="c6836-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="c6836-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6836-117">PARAMETERS</span></span>

### <span data-ttu-id="c6836-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6836-118">-DefaultProfile</span></span>
<span data-ttu-id="c6836-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6836-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c6836-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c6836-120">-FriendlyName</span></span>
<span data-ttu-id="c6836-121">Az ASR által védett elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6836-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="c6836-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c6836-122">-Name</span></span>
<span data-ttu-id="c6836-123">Az ASR által védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6836-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="c6836-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c6836-124">-ProtectionContainer</span></span>
<span data-ttu-id="c6836-125">Az Azure Site Recovery Protection Container objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="c6836-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="c6836-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6836-126">CommonParameters</span></span>
<span data-ttu-id="c6836-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6836-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6836-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6836-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6836-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6836-129">INPUTS</span></span>

### <span data-ttu-id="c6836-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c6836-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c6836-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6836-131">OUTPUTS</span></span>

### <span data-ttu-id="c6836-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c6836-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="c6836-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c6836-133">NOTES</span></span>

## <span data-ttu-id="c6836-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6836-134">RELATED LINKS</span></span>


