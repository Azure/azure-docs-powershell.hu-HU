---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 1d7f8adfa0db67d66c65c5ac7f3df7c64b665fda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939449"
---
# <span data-ttu-id="0845d-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0845d-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="0845d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0845d-102">SYNOPSIS</span></span>
<span data-ttu-id="0845d-103">AsR védelmi tárolókat kap a Helyreállítási szolgáltatások tárolóban.</span><span class="sxs-lookup"><span data-stu-id="0845d-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="0845d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0845d-104">SYNTAX</span></span>

### <span data-ttu-id="0845d-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0845d-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0845d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0845d-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0845d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0845d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0845d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0845d-108">DESCRIPTION</span></span>
<span data-ttu-id="0845d-109">A **Get-AzRecoveryServicesAsrProtectionContainer** parancsmag azure-webhely-helyreállítási védelmi tárolókat kap a Helyreállítási szolgáltatások tárolóban.</span><span class="sxs-lookup"><span data-stu-id="0845d-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="0845d-110">A védelmi tároló egy logikai tároló, amely védett (felderített) és védett objektumokat, például virtuális gépeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0845d-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="0845d-111">A replikációs házirendek replikációs beállításokat definiálnak a védett elemekhez, és egy védelmi tárolóhoz társíthatók, és egy védett elemre alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="0845d-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="0845d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0845d-112">EXAMPLES</span></span>

### <span data-ttu-id="0845d-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="0845d-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="0845d-114">A védelmi tároló listája szöveti $fabric.</span><span class="sxs-lookup"><span data-stu-id="0845d-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="0845d-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="0845d-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="0845d-116">A szövetben található védelmi tároló $fabric névvel.</span><span class="sxs-lookup"><span data-stu-id="0845d-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="0845d-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="0845d-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="0845d-118">A felhasználóbarát névvel $fabric anyagba $fabric tároló.</span><span class="sxs-lookup"><span data-stu-id="0845d-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="0845d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0845d-119">PARAMETERS</span></span>

### <span data-ttu-id="0845d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0845d-120">-DefaultProfile</span></span>
<span data-ttu-id="0845d-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0845d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0845d-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="0845d-122">-Fabric</span></span>
<span data-ttu-id="0845d-123">Keresse meg a védelmi tárolót a megadott ASR-anyagban.</span><span class="sxs-lookup"><span data-stu-id="0845d-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0845d-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0845d-124">-FriendlyName</span></span>
<span data-ttu-id="0845d-125">A keresve keresve található ASR védelmi tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0845d-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="0845d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0845d-126">-Name</span></span>
<span data-ttu-id="0845d-127">Megadja a keresve keresve található ASR védelmi tároló nevét.</span><span class="sxs-lookup"><span data-stu-id="0845d-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="0845d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0845d-128">CommonParameters</span></span>
<span data-ttu-id="0845d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0845d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0845d-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0845d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0845d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0845d-131">INPUTS</span></span>

### <span data-ttu-id="0845d-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="0845d-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="0845d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0845d-133">OUTPUTS</span></span>

### <span data-ttu-id="0845d-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0845d-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="0845d-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0845d-135">NOTES</span></span>

## <span data-ttu-id="0845d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0845d-136">RELATED LINKS</span></span>
