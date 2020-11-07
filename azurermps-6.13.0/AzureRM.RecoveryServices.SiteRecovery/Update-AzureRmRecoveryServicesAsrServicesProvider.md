---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9d7cfb1b5bdba7d82d42347dad697c5efa764919
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680794"
---
# <span data-ttu-id="28e44-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="28e44-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="28e44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28e44-102">SYNOPSIS</span></span>
<span data-ttu-id="28e44-103">Frissíti (frissíti a kiszolgálót) az Azure webhely-helyreállítási szolgáltatótól kapott adatokról.</span><span class="sxs-lookup"><span data-stu-id="28e44-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28e44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28e44-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28e44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="28e44-105">DESCRIPTION</span></span>
<span data-ttu-id="28e44-106">Az **Update-AzureRmRecoveryServicesAsrServicesProvider** parancsmag frissíti az Azure webhely-helyreállítási szolgáltatás szolgáltatójától kapott információkat.</span><span class="sxs-lookup"><span data-stu-id="28e44-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="28e44-107">Ezzel a parancsmaggal megadhatja a helyreállítási szolgáltatótól kapott információk frissítését.</span><span class="sxs-lookup"><span data-stu-id="28e44-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="28e44-108">Példák</span><span class="sxs-lookup"><span data-stu-id="28e44-108">EXAMPLES</span></span>

### <span data-ttu-id="28e44-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="28e44-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="28e44-110">Elindítja a megadott ASR-szolgáltatótól származó adatok frissítésének műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="28e44-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="28e44-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28e44-111">PARAMETERS</span></span>

### <span data-ttu-id="28e44-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e44-112">-DefaultProfile</span></span>
<span data-ttu-id="28e44-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28e44-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e44-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28e44-114">-InputObject</span></span>
<span data-ttu-id="28e44-115">Megadja azt az ASR-szolgáltató objektumot, amely azonosítja azt a kiszolgálót, amelyről frissíteni kell az információkat (frissült).</span><span class="sxs-lookup"><span data-stu-id="28e44-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28e44-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28e44-116">-Confirm</span></span>
<span data-ttu-id="28e44-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28e44-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e44-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e44-118">-WhatIf</span></span>
<span data-ttu-id="28e44-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28e44-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28e44-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28e44-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e44-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e44-121">CommonParameters</span></span>
<span data-ttu-id="28e44-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28e44-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e44-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28e44-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e44-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28e44-124">INPUTS</span></span>

### <span data-ttu-id="28e44-125">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="28e44-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="28e44-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28e44-126">OUTPUTS</span></span>

### <span data-ttu-id="28e44-127">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="28e44-127">System.Object</span></span>

## <span data-ttu-id="28e44-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28e44-128">NOTES</span></span>

## <span data-ttu-id="28e44-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28e44-129">RELATED LINKS</span></span>

[<span data-ttu-id="28e44-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="28e44-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="28e44-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="28e44-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
