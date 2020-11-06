---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 5862d76c574b469d3bc0e559892b505e1b90beab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494410"
---
# <span data-ttu-id="ba5bc-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ba5bc-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="ba5bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5bc-103">Bekapcsolja az ASR-védelem tárolóit a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba5bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba5bc-104">SYNTAX</span></span>

### <span data-ttu-id="ba5bc-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba5bc-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba5bc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ba5bc-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba5bc-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ba5bc-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba5bc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba5bc-108">DESCRIPTION</span></span>
<span data-ttu-id="ba5bc-109">A **Get-AzureRmRecoveryServicesAsrProtectionContainer** parancsmag az Azure site Recovery Protection tárolói tárolókat kapja meg a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="ba5bc-110">A védelmi tároló logikai tárolója a védelemmel ellátott (észlelt) és védett objektumoknak (például virtuális gépek).</span><span class="sxs-lookup"><span data-stu-id="ba5bc-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="ba5bc-111">A replikációs házirendek határozzák meg a védett elemek replikációs beállításait, és a védelemmel ellátott tárolóban használhatók, és a védelemmel ellátott elemekre alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="ba5bc-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ba5bc-112">EXAMPLES</span></span>

### <span data-ttu-id="ba5bc-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ba5bc-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="ba5bc-114">A Fabric-$fabric védelmi tárolójának listája.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="ba5bc-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="ba5bc-115">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
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

<span data-ttu-id="ba5bc-116">Protection tároló a szövet $fabric névvel.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="ba5bc-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="ba5bc-117">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
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

<span data-ttu-id="ba5bc-118">Védett tároló a szövet $fabric felhasználóbarát névvel.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="ba5bc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba5bc-119">PARAMETERS</span></span>

### <span data-ttu-id="ba5bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5bc-120">-DefaultProfile</span></span>
<span data-ttu-id="ba5bc-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="ba5bc-122">-Szövet</span><span class="sxs-lookup"><span data-stu-id="ba5bc-122">-Fabric</span></span>
<span data-ttu-id="ba5bc-123">A megadott ASR-anyagban keresse meg a védelmi tárolót.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5bc-124">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="ba5bc-124">-FriendlyName</span></span>
<span data-ttu-id="ba5bc-125">A kereséshez használt ASR-védelmi tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="ba5bc-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba5bc-126">-Name</span></span>
<span data-ttu-id="ba5bc-127">A keresni kívánt ASR-védelmi tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5bc-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="ba5bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5bc-128">CommonParameters</span></span>
<span data-ttu-id="ba5bc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba5bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5bc-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5bc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5bc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba5bc-131">INPUTS</span></span>

### <span data-ttu-id="ba5bc-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ba5bc-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ba5bc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba5bc-133">OUTPUTS</span></span>

### <span data-ttu-id="ba5bc-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ba5bc-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ba5bc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba5bc-135">NOTES</span></span>

## <span data-ttu-id="ba5bc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba5bc-136">RELATED LINKS</span></span>
