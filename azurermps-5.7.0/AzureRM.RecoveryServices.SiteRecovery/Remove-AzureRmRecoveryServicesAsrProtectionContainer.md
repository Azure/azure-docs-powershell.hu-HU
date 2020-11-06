---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 496eeed8b4ed4b41ce2c67d47fc636711cd5cb84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495314"
---
# <span data-ttu-id="472f4-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="472f4-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="472f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="472f4-102">SYNOPSIS</span></span>
<span data-ttu-id="472f4-103">Törli a megadott védelmi tárolót a szerkezetéről.</span><span class="sxs-lookup"><span data-stu-id="472f4-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="472f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="472f4-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="472f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="472f4-105">DESCRIPTION</span></span>
<span data-ttu-id="472f4-106">A Remove-AzureRmRecoveryServicesAsrProtectionContainer parancsmag törli a megadott Azure site Recovery Protection tárolót.</span><span class="sxs-lookup"><span data-stu-id="472f4-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="472f4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="472f4-107">EXAMPLES</span></span>

### <span data-ttu-id="472f4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="472f4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="472f4-109">Elindítja a megadott védelmi tároló törlését, és az eltávolítási művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="472f4-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="472f4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="472f4-110">PARAMETERS</span></span>

### <span data-ttu-id="472f4-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="472f4-111">-Confirm</span></span>
<span data-ttu-id="472f4-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="472f4-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="472f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472f4-113">-DefaultProfile</span></span>
<span data-ttu-id="472f4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="472f4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="472f4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="472f4-115">-InputObject</span></span>
<span data-ttu-id="472f4-116">Az eltávolítani kívánt védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="472f4-116">Specifies the protection container to be removed .</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="472f4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="472f4-117">-WhatIf</span></span>
<span data-ttu-id="472f4-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="472f4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="472f4-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="472f4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="472f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472f4-120">CommonParameters</span></span>
<span data-ttu-id="472f4-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="472f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472f4-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="472f4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472f4-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="472f4-123">INPUTS</span></span>

### <span data-ttu-id="472f4-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="472f4-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="472f4-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="472f4-125">OUTPUTS</span></span>

### <span data-ttu-id="472f4-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="472f4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="472f4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="472f4-127">NOTES</span></span>

## <span data-ttu-id="472f4-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="472f4-128">RELATED LINKS</span></span>
