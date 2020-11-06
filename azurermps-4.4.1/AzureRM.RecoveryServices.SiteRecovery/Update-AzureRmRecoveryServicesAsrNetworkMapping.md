---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501668"
---
# <span data-ttu-id="d0146-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d0146-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="d0146-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0146-102">SYNOPSIS</span></span>
<span data-ttu-id="d0146-103">Frissíti a megadott ASR-hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="d0146-103">Updates the specified ASR network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0146-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0146-104">SYNTAX</span></span>

### <span data-ttu-id="d0146-105">ByNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0146-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0146-106">ById</span><span class="sxs-lookup"><span data-stu-id="d0146-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0146-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0146-107">DESCRIPTION</span></span>
<span data-ttu-id="d0146-108">Az **Update-AzureRmRecoveryServicesAsrNetworkMapping** parancsmag frissíti a megadott Azure-webhely-helyreállítási hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="d0146-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="d0146-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d0146-109">EXAMPLES</span></span>

### <span data-ttu-id="d0146-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d0146-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="d0146-111">Elindítja a hálózati megfeleltetési műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d0146-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d0146-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0146-112">PARAMETERS</span></span>

### <span data-ttu-id="d0146-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0146-113">-InputObject</span></span>
<span data-ttu-id="d0146-114">Beviteli objektum: Itt adhatja meg, hogy az ASR-hálózati megfeleltetési objektum az ASR-hálózati megfeleltetésnek megfelelően frissüljön-e</span><span class="sxs-lookup"><span data-stu-id="d0146-114">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated</span></span> 

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0146-115">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="d0146-115">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="d0146-116">A helyreállítási Azure hálózati AZONOSÍTÓját adja meg a hálózati megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="d0146-116">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0146-117">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="d0146-117">-RecoveryNetwork</span></span>
<span data-ttu-id="d0146-118">A hálózati megfeleltetéshez a helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0146-118">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0146-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0146-119">-Confirm</span></span>
<span data-ttu-id="d0146-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0146-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0146-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0146-121">-WhatIf</span></span>
<span data-ttu-id="d0146-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0146-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0146-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0146-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0146-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0146-124">CommonParameters</span></span>
<span data-ttu-id="d0146-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0146-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0146-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0146-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0146-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0146-127">INPUTS</span></span>

### <span data-ttu-id="d0146-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d0146-128">None</span></span>

## <span data-ttu-id="d0146-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0146-129">OUTPUTS</span></span>

### <span data-ttu-id="d0146-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d0146-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d0146-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0146-131">NOTES</span></span>

## <span data-ttu-id="d0146-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0146-132">RELATED LINKS</span></span>

