---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169282"
---
# <span data-ttu-id="f759b-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f759b-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="f759b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f759b-102">SYNOPSIS</span></span>
<span data-ttu-id="f759b-103">AsR védelmi tárolókat kap a Helyreállítási szolgáltatások tárolóban.</span><span class="sxs-lookup"><span data-stu-id="f759b-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="f759b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f759b-104">SYNTAX</span></span>

### <span data-ttu-id="f759b-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f759b-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f759b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f759b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f759b-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f759b-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f759b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f759b-108">DESCRIPTION</span></span>
<span data-ttu-id="f759b-109">A **Get-AzRecoveryServicesAsrProtectionContainer** parancsmag azure-webhely-helyreállítási védelmi tárolókat kap a Helyreállítási szolgáltatások tárolóban.</span><span class="sxs-lookup"><span data-stu-id="f759b-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="f759b-110">A védelmi tároló egy logikai tároló, amely védett (felderített) és védett objektumokat, például virtuális gépeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="f759b-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="f759b-111">A replikációs házirendek replikációs beállításokat definiálnak a védett elemekhez, és egy védelmi tárolóhoz társíthatók, és egy védett elemre alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="f759b-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="f759b-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f759b-112">EXAMPLES</span></span>

### <span data-ttu-id="f759b-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="f759b-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="f759b-114">A védőtárolók listája szöveti $fabric.</span><span class="sxs-lookup"><span data-stu-id="f759b-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="f759b-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="f759b-115">Example 2</span></span>
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

<span data-ttu-id="f759b-116">A szövetben található védelmi tároló $fabric névvel.</span><span class="sxs-lookup"><span data-stu-id="f759b-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="f759b-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="f759b-117">Example 3</span></span>
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

<span data-ttu-id="f759b-118">A felhasználóbarát névvel $fabric anyagba $fabric tároló.</span><span class="sxs-lookup"><span data-stu-id="f759b-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="f759b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f759b-119">PARAMETERS</span></span>

### <span data-ttu-id="f759b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f759b-120">-DefaultProfile</span></span>
<span data-ttu-id="f759b-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f759b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f759b-122">-Fabric</span><span class="sxs-lookup"><span data-stu-id="f759b-122">-Fabric</span></span>
<span data-ttu-id="f759b-123">Keresse meg a védelmi tárolót a megadott ASR-anyagban.</span><span class="sxs-lookup"><span data-stu-id="f759b-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="f759b-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f759b-124">-FriendlyName</span></span>
<span data-ttu-id="f759b-125">A keresve keresve található ASR védelmi tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f759b-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="f759b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f759b-126">-Name</span></span>
<span data-ttu-id="f759b-127">Megadja a keresve keresve található ASR védelmi tároló nevét.</span><span class="sxs-lookup"><span data-stu-id="f759b-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="f759b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f759b-128">CommonParameters</span></span>
<span data-ttu-id="f759b-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f759b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f759b-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f759b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f759b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f759b-131">INPUTS</span></span>

### <span data-ttu-id="f759b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f759b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f759b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f759b-133">OUTPUTS</span></span>

### <span data-ttu-id="f759b-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f759b-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="f759b-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f759b-135">NOTES</span></span>

## <span data-ttu-id="f759b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f759b-136">RELATED LINKS</span></span>
