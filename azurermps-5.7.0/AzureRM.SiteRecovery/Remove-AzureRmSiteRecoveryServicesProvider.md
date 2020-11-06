---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 88b6b83f24edb06871fd87f61fec1732893b0f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492176"
---
# <span data-ttu-id="89042-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="89042-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="89042-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89042-102">SYNOPSIS</span></span>
<span data-ttu-id="89042-103">Egy Azure webhely-helyreállítási szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="89042-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89042-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89042-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89042-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="89042-105">DESCRIPTION</span></span>
<span data-ttu-id="89042-106">A **Remove-AzureRmSiteRecoveryServicesProvider** parancsmag eltávolítja az Azure site Recovery Services szolgáltatót a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="89042-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="89042-107">Példák</span><span class="sxs-lookup"><span data-stu-id="89042-107">EXAMPLES</span></span>

## <span data-ttu-id="89042-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89042-108">PARAMETERS</span></span>

### <span data-ttu-id="89042-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89042-109">-DefaultProfile</span></span>
<span data-ttu-id="89042-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89042-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89042-111">-Force</span><span class="sxs-lookup"><span data-stu-id="89042-111">-Force</span></span>
<span data-ttu-id="89042-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="89042-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89042-113">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="89042-113">-ServicesProvider</span></span>
<span data-ttu-id="89042-114">A Services szolgáltató objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="89042-114">Specifies the Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89042-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89042-115">-Confirm</span></span>
<span data-ttu-id="89042-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89042-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89042-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89042-117">-WhatIf</span></span>
<span data-ttu-id="89042-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89042-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="89042-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89042-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89042-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89042-120">CommonParameters</span></span>
<span data-ttu-id="89042-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89042-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89042-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89042-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89042-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89042-123">INPUTS</span></span>

### <span data-ttu-id="89042-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="89042-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="89042-125">A ' ServicesProvider ' paraméter az "ASRRecoveryServicesProvider" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="89042-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="89042-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89042-126">OUTPUTS</span></span>

### <span data-ttu-id="89042-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRJob, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="89042-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="89042-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89042-128">NOTES</span></span>

## <span data-ttu-id="89042-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89042-129">RELATED LINKS</span></span>

[<span data-ttu-id="89042-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="89042-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="89042-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="89042-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
