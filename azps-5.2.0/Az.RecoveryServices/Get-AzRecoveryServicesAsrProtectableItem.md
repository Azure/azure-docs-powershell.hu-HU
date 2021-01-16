---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c9c50e26e99493fb693b8bded693bceb24f5a40f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364768"
---
# <span data-ttu-id="73952-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="73952-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="73952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73952-102">SYNOPSIS</span></span>
<span data-ttu-id="73952-103">Szerezze be a védett elemeket egy ASR védelmi tárolóban.</span><span class="sxs-lookup"><span data-stu-id="73952-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="73952-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73952-104">SYNTAX</span></span>

### <span data-ttu-id="73952-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73952-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73952-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="73952-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73952-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="73952-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73952-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73952-108">DESCRIPTION</span></span>
<span data-ttu-id="73952-109">A **Get-AzRecoveryServicesAsrProtectableItem** parancsmag egy Azure-webhely-helyreállítási védelmi tárolóban kapja meg a védett elemeket.</span><span class="sxs-lookup"><span data-stu-id="73952-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="73952-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73952-110">EXAMPLES</span></span>

### <span data-ttu-id="73952-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="73952-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="73952-112">Beveszi a megadott ASR védelmi tárolóban lévő összes védett elemet.</span><span class="sxs-lookup"><span data-stu-id="73952-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="73952-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="73952-113">Example 2</span></span>
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

<span data-ttu-id="73952-114">Szerezze be a védett elemeket a megadott ASR védelmi tárolóban, és a megadott rövid névvel.</span><span class="sxs-lookup"><span data-stu-id="73952-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="73952-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="73952-115">Example 3</span></span>
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

<span data-ttu-id="73952-116">Beveszi a megadott ASR védelmi tárolóban lévő összes védett elemet.</span><span class="sxs-lookup"><span data-stu-id="73952-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="73952-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73952-117">PARAMETERS</span></span>

### <span data-ttu-id="73952-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73952-118">-DefaultProfile</span></span>
<span data-ttu-id="73952-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73952-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="73952-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="73952-120">-FriendlyName</span></span>
<span data-ttu-id="73952-121">Az ASR által védett elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73952-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="73952-122">-Name</span><span class="sxs-lookup"><span data-stu-id="73952-122">-Name</span></span>
<span data-ttu-id="73952-123">Az ASR által védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73952-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="73952-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="73952-124">-ProtectionContainer</span></span>
<span data-ttu-id="73952-125">Az Azure Site Recovery Protection Container objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="73952-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="73952-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73952-126">CommonParameters</span></span>
<span data-ttu-id="73952-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73952-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73952-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73952-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73952-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73952-129">INPUTS</span></span>

### <span data-ttu-id="73952-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="73952-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="73952-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73952-131">OUTPUTS</span></span>

### <span data-ttu-id="73952-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="73952-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="73952-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73952-133">NOTES</span></span>

## <span data-ttu-id="73952-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73952-134">RELATED LINKS</span></span>

[<span data-ttu-id="73952-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="73952-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="73952-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="73952-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
