---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679672"
---
# <span data-ttu-id="df2d0-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="df2d0-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="df2d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="df2d0-103">Az Azure webhely-helyreállítási védelmi tároló megfeleltetésének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="df2d0-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df2d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df2d0-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df2d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="df2d0-105">DESCRIPTION</span></span>
<span data-ttu-id="df2d0-106">A **Remove-AzureRmSiteRecoveryProtectionContainerMapping** parancsmag eltávolítja az Azure webhely-helyreállítási védelmi tárolók megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="df2d0-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="df2d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="df2d0-107">EXAMPLES</span></span>

## <span data-ttu-id="df2d0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df2d0-108">PARAMETERS</span></span>

### <span data-ttu-id="df2d0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df2d0-109">-DefaultProfile</span></span>
<span data-ttu-id="df2d0-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df2d0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df2d0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="df2d0-111">-Force</span></span>
<span data-ttu-id="df2d0-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="df2d0-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df2d0-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="df2d0-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="df2d0-114">Az Azure webhely-helyreállítási védelmi tároló megfeleltetési objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df2d0-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df2d0-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df2d0-115">-Confirm</span></span>
<span data-ttu-id="df2d0-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df2d0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df2d0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df2d0-117">-WhatIf</span></span>
<span data-ttu-id="df2d0-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="df2d0-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="df2d0-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df2d0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df2d0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df2d0-120">CommonParameters</span></span>
<span data-ttu-id="df2d0-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df2d0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df2d0-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df2d0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df2d0-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df2d0-123">INPUTS</span></span>

### <span data-ttu-id="df2d0-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="df2d0-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="df2d0-125">A ' ProtectionContainerMapping ' paraméter az "ASRProtectionContainerMapping" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="df2d0-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="df2d0-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df2d0-126">OUTPUTS</span></span>

### <span data-ttu-id="df2d0-127">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="df2d0-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="df2d0-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df2d0-128">NOTES</span></span>

## <span data-ttu-id="df2d0-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df2d0-129">RELATED LINKS</span></span>

[<span data-ttu-id="df2d0-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="df2d0-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="df2d0-131">Új – AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="df2d0-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
