---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 31dc0a5e7fb9bba20aea6fb6395ec59ba54d0e2c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399838"
---
# <span data-ttu-id="50804-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="50804-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="50804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50804-102">SYNOPSIS</span></span>
<span data-ttu-id="50804-103">Szerezze be a védett elemeket egy ASR védelmi tárolóban.</span><span class="sxs-lookup"><span data-stu-id="50804-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="50804-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="50804-104">SYNTAX</span></span>

### <span data-ttu-id="50804-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50804-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50804-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="50804-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50804-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="50804-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50804-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="50804-108">DESCRIPTION</span></span>
<span data-ttu-id="50804-109">A **Get-AzRecoveryServicesAsrProtectableItem** parancsmag egy Azure-webhely-helyreállítási védelmi tárolóban kapja meg a védett elemeket.</span><span class="sxs-lookup"><span data-stu-id="50804-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="50804-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="50804-110">EXAMPLES</span></span>

### <span data-ttu-id="50804-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="50804-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="50804-112">Beveszi a megadott ASR védelmi tárolóban lévő összes védett elemet.</span><span class="sxs-lookup"><span data-stu-id="50804-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="50804-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="50804-113">Example 2</span></span>
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

<span data-ttu-id="50804-114">Szerezze be a védett elemeket a megadott ASR védelmi tárolóban, és a megadott rövid névvel.</span><span class="sxs-lookup"><span data-stu-id="50804-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="50804-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="50804-115">Example 3</span></span>
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

<span data-ttu-id="50804-116">Beveszi a megadott ASR védelmi tárolóban lévő összes védett elemet.</span><span class="sxs-lookup"><span data-stu-id="50804-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="50804-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50804-117">PARAMETERS</span></span>

### <span data-ttu-id="50804-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50804-118">-DefaultProfile</span></span>
<span data-ttu-id="50804-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50804-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="50804-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="50804-120">-FriendlyName</span></span>
<span data-ttu-id="50804-121">Az ASR által védett elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50804-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="50804-122">-Name</span><span class="sxs-lookup"><span data-stu-id="50804-122">-Name</span></span>
<span data-ttu-id="50804-123">Az ASR által védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50804-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="50804-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="50804-124">-ProtectionContainer</span></span>
<span data-ttu-id="50804-125">Az Azure Site Recovery Protection Container objektum megadása.</span><span class="sxs-lookup"><span data-stu-id="50804-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="50804-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50804-126">CommonParameters</span></span>
<span data-ttu-id="50804-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50804-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50804-128">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50804-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50804-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50804-129">INPUTS</span></span>

### <span data-ttu-id="50804-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="50804-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="50804-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50804-131">OUTPUTS</span></span>

### <span data-ttu-id="50804-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="50804-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="50804-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="50804-133">NOTES</span></span>

## <span data-ttu-id="50804-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50804-134">RELATED LINKS</span></span>


