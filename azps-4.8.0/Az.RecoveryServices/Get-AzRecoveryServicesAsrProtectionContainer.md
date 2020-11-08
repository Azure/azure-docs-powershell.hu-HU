---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017699"
---
# <span data-ttu-id="88bd2-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="88bd2-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="88bd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="88bd2-103">Bekapcsolja az ASR-védelem tárolóit a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="88bd2-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="88bd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88bd2-104">SYNTAX</span></span>

### <span data-ttu-id="88bd2-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88bd2-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88bd2-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="88bd2-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88bd2-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="88bd2-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88bd2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="88bd2-108">DESCRIPTION</span></span>
<span data-ttu-id="88bd2-109">A **Get-AzRecoveryServicesAsrProtectionContainer** parancsmag az Azure site Recovery Protection tárolói tárolókat kapja meg a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="88bd2-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="88bd2-110">A védelmi tároló logikai tárolója a védelemmel ellátott (észlelt) és védett objektumoknak (például virtuális gépek).</span><span class="sxs-lookup"><span data-stu-id="88bd2-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="88bd2-111">A replikációs házirendek határozzák meg a védett elemek replikációs beállításait, és a védelemmel ellátott tárolóban használhatók, és a védelemmel ellátott elemekre alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="88bd2-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="88bd2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="88bd2-112">EXAMPLES</span></span>

### <span data-ttu-id="88bd2-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88bd2-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="88bd2-114">A Fabric-$fabric védelmi tárolójának listája.</span><span class="sxs-lookup"><span data-stu-id="88bd2-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="88bd2-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="88bd2-115">Example 2</span></span>
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

<span data-ttu-id="88bd2-116">Protection tároló a szövet $fabric névvel.</span><span class="sxs-lookup"><span data-stu-id="88bd2-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="88bd2-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="88bd2-117">Example 3</span></span>
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

<span data-ttu-id="88bd2-118">Védett tároló a szövet $fabric felhasználóbarát névvel.</span><span class="sxs-lookup"><span data-stu-id="88bd2-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="88bd2-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88bd2-119">PARAMETERS</span></span>

### <span data-ttu-id="88bd2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bd2-120">-DefaultProfile</span></span>
<span data-ttu-id="88bd2-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88bd2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="88bd2-122">-Szövet</span><span class="sxs-lookup"><span data-stu-id="88bd2-122">-Fabric</span></span>
<span data-ttu-id="88bd2-123">A megadott ASR-anyagban keresse meg a védelmi tárolót.</span><span class="sxs-lookup"><span data-stu-id="88bd2-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="88bd2-124">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="88bd2-124">-FriendlyName</span></span>
<span data-ttu-id="88bd2-125">A kereséshez használt ASR-védelmi tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88bd2-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="88bd2-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88bd2-126">-Name</span></span>
<span data-ttu-id="88bd2-127">A keresni kívánt ASR-védelmi tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88bd2-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="88bd2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bd2-128">CommonParameters</span></span>
<span data-ttu-id="88bd2-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88bd2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bd2-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88bd2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bd2-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88bd2-131">INPUTS</span></span>

### <span data-ttu-id="88bd2-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="88bd2-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="88bd2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88bd2-133">OUTPUTS</span></span>

### <span data-ttu-id="88bd2-134">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="88bd2-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="88bd2-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88bd2-135">NOTES</span></span>

## <span data-ttu-id="88bd2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88bd2-136">RELATED LINKS</span></span>
