---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 60bcdad644f07f627373c90791c8cd115d590bcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669566"
---
# <span data-ttu-id="39ecb-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="39ecb-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="39ecb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="39ecb-103">Frissíti (frissíti a kiszolgálót) az Azure webhely-helyreállítási szolgáltatótól kapott adatokról.</span><span class="sxs-lookup"><span data-stu-id="39ecb-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="39ecb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39ecb-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39ecb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="39ecb-106">Az **Update-AzRecoveryServicesAsrServicesProvider** parancsmag frissíti az Azure webhely-helyreállítási szolgáltatás szolgáltatójától kapott információkat.</span><span class="sxs-lookup"><span data-stu-id="39ecb-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="39ecb-107">Ezzel a parancsmaggal megadhatja a helyreállítási szolgáltatótól kapott információk frissítését.</span><span class="sxs-lookup"><span data-stu-id="39ecb-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="39ecb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="39ecb-108">EXAMPLES</span></span>

### <span data-ttu-id="39ecb-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="39ecb-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="39ecb-110">Elindítja a megadott ASR-szolgáltatótól származó adatok frissítésének műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="39ecb-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="39ecb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39ecb-111">PARAMETERS</span></span>

### <span data-ttu-id="39ecb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ecb-112">-DefaultProfile</span></span>
<span data-ttu-id="39ecb-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39ecb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="39ecb-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39ecb-114">-InputObject</span></span>
<span data-ttu-id="39ecb-115">Megadja azt az ASR-szolgáltató objektumot, amely azonosítja azt a kiszolgálót, amelyről frissíteni kell az információkat (frissült).</span><span class="sxs-lookup"><span data-stu-id="39ecb-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="39ecb-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39ecb-116">-Confirm</span></span>
<span data-ttu-id="39ecb-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39ecb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ecb-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ecb-118">-WhatIf</span></span>
<span data-ttu-id="39ecb-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39ecb-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39ecb-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39ecb-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ecb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ecb-121">CommonParameters</span></span>
<span data-ttu-id="39ecb-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39ecb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ecb-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ecb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ecb-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39ecb-124">INPUTS</span></span>

### <span data-ttu-id="39ecb-125">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="39ecb-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="39ecb-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39ecb-126">OUTPUTS</span></span>

### <span data-ttu-id="39ecb-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="39ecb-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="39ecb-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39ecb-128">NOTES</span></span>

## <span data-ttu-id="39ecb-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39ecb-129">RELATED LINKS</span></span>

[<span data-ttu-id="39ecb-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="39ecb-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="39ecb-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="39ecb-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
