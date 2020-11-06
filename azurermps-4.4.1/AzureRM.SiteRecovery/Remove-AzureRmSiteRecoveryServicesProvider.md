---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e7ee32974ef87b86d443d90b7dc628f9c9f1072f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494647"
---
# <span data-ttu-id="ef7e2-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ef7e2-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="ef7e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7e2-103">Egy Azure webhely-helyreállítási szolgáltató eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ef7e2-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef7e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef7e2-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef7e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef7e2-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7e2-106">A **Remove-AzureRmSiteRecoveryServicesProvider** parancsmag eltávolítja az Azure site Recovery Services szolgáltatót a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="ef7e2-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="ef7e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ef7e2-107">EXAMPLES</span></span>

## <span data-ttu-id="ef7e2-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef7e2-108">PARAMETERS</span></span>

### <span data-ttu-id="ef7e2-109">-Force</span><span class="sxs-lookup"><span data-stu-id="ef7e2-109">-Force</span></span>
<span data-ttu-id="ef7e2-110">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ef7e2-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7e2-111">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ef7e2-111">-ServicesProvider</span></span>
<span data-ttu-id="ef7e2-112">A Services szolgáltató objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef7e2-112">Specifies the Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7e2-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef7e2-113">-Confirm</span></span>
<span data-ttu-id="ef7e2-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef7e2-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7e2-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7e2-115">-WhatIf</span></span>
<span data-ttu-id="ef7e2-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef7e2-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ef7e2-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef7e2-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7e2-118">-DefaultProfile</span></span>
<span data-ttu-id="ef7e2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef7e2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef7e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7e2-120">CommonParameters</span></span>
<span data-ttu-id="ef7e2-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef7e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7e2-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7e2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7e2-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef7e2-123">INPUTS</span></span>

### <span data-ttu-id="ef7e2-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ef7e2-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="ef7e2-125">A ' ServicesProvider ' paraméter az "ASRRecoveryServicesProvider" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ef7e2-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="ef7e2-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef7e2-126">OUTPUTS</span></span>

### <span data-ttu-id="ef7e2-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRJob, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ef7e2-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ef7e2-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef7e2-128">NOTES</span></span>

## <span data-ttu-id="ef7e2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef7e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="ef7e2-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ef7e2-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="ef7e2-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ef7e2-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
