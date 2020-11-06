---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 43d9603a5938ecef084191ebe77888a5f1769673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502364"
---
# <span data-ttu-id="930a8-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="930a8-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="930a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="930a8-102">SYNOPSIS</span></span>
<span data-ttu-id="930a8-103">Az Azure webhely-helyreállítási anyag eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="930a8-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="930a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="930a8-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="930a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="930a8-105">DESCRIPTION</span></span>
<span data-ttu-id="930a8-106">A **Remove-AzureRmSiteRecoveryFabric** parancsmag eltávolítja az Azure-webhelyek helyreállítási szövetét.</span><span class="sxs-lookup"><span data-stu-id="930a8-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="930a8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="930a8-107">EXAMPLES</span></span>

## <span data-ttu-id="930a8-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="930a8-108">PARAMETERS</span></span>

### <span data-ttu-id="930a8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930a8-109">-DefaultProfile</span></span>
<span data-ttu-id="930a8-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="930a8-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="930a8-111">-Szövet</span><span class="sxs-lookup"><span data-stu-id="930a8-111">-Fabric</span></span>
<span data-ttu-id="930a8-112">Az Azure site Recovery Fabric objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="930a8-112">Specifies the Azure Site Recovery Fabric object.</span></span>

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

### <span data-ttu-id="930a8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="930a8-113">-Force</span></span>
<span data-ttu-id="930a8-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="930a8-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930a8-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="930a8-115">-Confirm</span></span>
<span data-ttu-id="930a8-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="930a8-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930a8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="930a8-117">-WhatIf</span></span>
<span data-ttu-id="930a8-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="930a8-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="930a8-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="930a8-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930a8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930a8-120">CommonParameters</span></span>
<span data-ttu-id="930a8-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="930a8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930a8-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="930a8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930a8-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="930a8-123">INPUTS</span></span>

### <span data-ttu-id="930a8-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="930a8-124">ASRFabric</span></span>
<span data-ttu-id="930a8-125">A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="930a8-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="930a8-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="930a8-126">OUTPUTS</span></span>

### <span data-ttu-id="930a8-127">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="930a8-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="930a8-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="930a8-128">NOTES</span></span>

## <span data-ttu-id="930a8-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="930a8-129">RELATED LINKS</span></span>

[<span data-ttu-id="930a8-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="930a8-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="930a8-131">Új – AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="930a8-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
