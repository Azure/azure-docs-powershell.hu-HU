---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679354"
---
# <span data-ttu-id="5735c-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5735c-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="5735c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5735c-102">SYNOPSIS</span></span>
<span data-ttu-id="5735c-103">Frissíti (frissíti a kiszolgálót) az Azure webhely-helyreállítási szolgáltatótól kapott adatokról.</span><span class="sxs-lookup"><span data-stu-id="5735c-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5735c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5735c-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5735c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5735c-105">DESCRIPTION</span></span>
<span data-ttu-id="5735c-106">Az **Update-AzureRmRecoveryServicesAsrServicesProvider** parancsmag frissíti az Azure webhely-helyreállítási szolgáltatás szolgáltatójától kapott információkat.</span><span class="sxs-lookup"><span data-stu-id="5735c-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="5735c-107">Ezzel a parancsmaggal megadhatja a helyreállítási szolgáltatótól kapott információk frissítését.</span><span class="sxs-lookup"><span data-stu-id="5735c-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="5735c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5735c-108">EXAMPLES</span></span>

### <span data-ttu-id="5735c-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5735c-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="5735c-110">Elindítja a megadott ASR-szolgáltatótól származó adatok frissítésének műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="5735c-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="5735c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5735c-111">PARAMETERS</span></span>

### <span data-ttu-id="5735c-112">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5735c-112">-InputObject</span></span>
<span data-ttu-id="5735c-113">Beviteli objektum: Itt adhatja meg az ASR-szolgáltató objektumnak az ASR-szolgáltatónak megfelelő adatszolgáltatót, amely azonosítja azt a kiszolgálót, amely a frissítendő információkat tartalmazza (frissült.)</span><span class="sxs-lookup"><span data-stu-id="5735c-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5735c-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5735c-114">-Confirm</span></span>
<span data-ttu-id="5735c-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5735c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5735c-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5735c-116">-WhatIf</span></span>
<span data-ttu-id="5735c-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5735c-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5735c-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5735c-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5735c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5735c-119">CommonParameters</span></span>
<span data-ttu-id="5735c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5735c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5735c-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5735c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5735c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5735c-122">INPUTS</span></span>

### <span data-ttu-id="5735c-123">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5735c-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="5735c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5735c-124">OUTPUTS</span></span>

### <span data-ttu-id="5735c-125">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5735c-125">System.Object</span></span>

## <span data-ttu-id="5735c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5735c-126">NOTES</span></span>

## <span data-ttu-id="5735c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5735c-127">RELATED LINKS</span></span>

[<span data-ttu-id="5735c-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5735c-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="5735c-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5735c-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
