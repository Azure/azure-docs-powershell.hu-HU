---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504792"
---
# <span data-ttu-id="bd08c-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="bd08c-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="bd08c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd08c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd08c-103">Bekapcsolja az ASR-védelem tárolóit a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="bd08c-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd08c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd08c-104">SYNTAX</span></span>

### <span data-ttu-id="bd08c-105">ByFabricObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd08c-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="bd08c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="bd08c-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="bd08c-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="bd08c-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="bd08c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd08c-108">DESCRIPTION</span></span>
<span data-ttu-id="bd08c-109">A **Get-AzureRmRecoveryServicesAsrProtectionContainer** parancsmag az Azure site Recovery Protection tárolói tárolókat kapja meg a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="bd08c-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="bd08c-110">A védelmi tároló logikai tárolója a védelemmel ellátott (észlelt) és védett objektumoknak (például virtuális gépek).</span><span class="sxs-lookup"><span data-stu-id="bd08c-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="bd08c-111">A replikációs házirendek határozzák meg a védett elemek replikációs beállításait, és a védelemmel ellátott tárolóban használhatók, és a védelemmel ellátott elemekre alkalmazhatók.</span><span class="sxs-lookup"><span data-stu-id="bd08c-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="bd08c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="bd08c-112">EXAMPLES</span></span>

### <span data-ttu-id="bd08c-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bd08c-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="bd08c-114">A megadott ASR-anyagból beolvassa az összes ASR-védelmi tárolót (a fenti példában a pipeline bemenetet).</span><span class="sxs-lookup"><span data-stu-id="bd08c-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="bd08c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd08c-115">PARAMETERS</span></span>

### <span data-ttu-id="bd08c-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="bd08c-116">-Fabric</span></span>
<span data-ttu-id="bd08c-117">A megadott ASR-anyagban keresse meg a védelmi tárolót.</span><span class="sxs-lookup"><span data-stu-id="bd08c-117">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="bd08c-118">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="bd08c-118">-FriendlyName</span></span>
<span data-ttu-id="bd08c-119">A kereséshez használt ASR-védelmi tároló rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd08c-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="bd08c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd08c-120">-Name</span></span>
<span data-ttu-id="bd08c-121">A keresni kívánt ASR-védelmi tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd08c-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="bd08c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd08c-122">CommonParameters</span></span>
<span data-ttu-id="bd08c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd08c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd08c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd08c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd08c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd08c-125">INPUTS</span></span>

### <span data-ttu-id="bd08c-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bd08c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="bd08c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd08c-127">OUTPUTS</span></span>

### <span data-ttu-id="bd08c-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bd08c-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bd08c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd08c-129">NOTES</span></span>

## <span data-ttu-id="bd08c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd08c-130">RELATED LINKS</span></span>

