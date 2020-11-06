---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501680"
---
# <span data-ttu-id="c1834-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c1834-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="c1834-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1834-102">SYNOPSIS</span></span>
<span data-ttu-id="c1834-103">ASR-hálózati megfeleltetést hoz létre két hálózat között.</span><span class="sxs-lookup"><span data-stu-id="c1834-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1834-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1834-104">SYNTAX</span></span>

### <span data-ttu-id="c1834-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1834-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1834-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c1834-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1834-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1834-107">DESCRIPTION</span></span>
<span data-ttu-id="c1834-108">A **New-AzureRmRecoveryServicesAsrNetworkMapping** parancsmag a két hálózat közötti ASR-hálózati megfeleltetések létrehozásának működését indítja el, és a művelet nyomon követéséhez használt ASR-feladat értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="c1834-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c1834-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c1834-109">EXAMPLES</span></span>

### <span data-ttu-id="c1834-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c1834-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="c1834-111">A megadott név, elsődleges és helyreállítási hálózat segítségével elindítja a hálózati megfeleltetés létrehozásának műveletét, és egy ASR-feladatot ad eredményül a művelet nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="c1834-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="c1834-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1834-112">PARAMETERS</span></span>

### <span data-ttu-id="c1834-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1834-113">-Name</span></span>
<span data-ttu-id="c1834-114">A létrehozandó ASR-hálózati megfeleltetés neve.</span><span class="sxs-lookup"><span data-stu-id="c1834-114">Name of the ASR network mapping to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1834-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="c1834-115">-PrimaryNetwork</span></span>
<span data-ttu-id="c1834-116">A hálózati megfeleltetés elsődleges hálózati objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1834-116">Specifies the primary network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1834-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="c1834-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="c1834-118">A helyreállítási Azure hálózati AZONOSÍTÓját adja meg a hálózati megfeleltetéshez.</span><span class="sxs-lookup"><span data-stu-id="c1834-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1834-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c1834-119">-RecoveryNetwork</span></span>
<span data-ttu-id="c1834-120">A hálózati megfeleltetéshez a helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1834-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1834-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1834-121">-Confirm</span></span>
<span data-ttu-id="c1834-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1834-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1834-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1834-123">-WhatIf</span></span>
<span data-ttu-id="c1834-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1834-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1834-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1834-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1834-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1834-126">CommonParameters</span></span>
<span data-ttu-id="c1834-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1834-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1834-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1834-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1834-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1834-129">INPUTS</span></span>

### <span data-ttu-id="c1834-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="c1834-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="c1834-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1834-131">OUTPUTS</span></span>

### <span data-ttu-id="c1834-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c1834-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c1834-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1834-133">NOTES</span></span>

## <span data-ttu-id="c1834-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1834-134">RELATED LINKS</span></span>

[<span data-ttu-id="c1834-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c1834-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="c1834-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c1834-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
