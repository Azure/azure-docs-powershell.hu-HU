---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 31887397c6b9b0a3a18a4af3cb4b4faca7c4a91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502407"
---
# <span data-ttu-id="dee2f-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dee2f-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="dee2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dee2f-102">SYNOPSIS</span></span>
<span data-ttu-id="dee2f-103">Megkapja az Azure site Recovery Protection Container-megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="dee2f-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dee2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dee2f-104">SYNTAX</span></span>

### <span data-ttu-id="dee2f-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dee2f-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dee2f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="dee2f-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee2f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dee2f-107">DESCRIPTION</span></span>
<span data-ttu-id="dee2f-108">A **Get-AzureRmSiteRecoveryProtectionContainerMapping** parancsmag információkat kap a védelemmel ellátni a tárolóban lévő házirend-megfeleltetésekre.</span><span class="sxs-lookup"><span data-stu-id="dee2f-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="dee2f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dee2f-109">EXAMPLES</span></span>

## <span data-ttu-id="dee2f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dee2f-110">PARAMETERS</span></span>

### <span data-ttu-id="dee2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee2f-111">-DefaultProfile</span></span>
<span data-ttu-id="dee2f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dee2f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dee2f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dee2f-113">-Name</span></span>
<span data-ttu-id="dee2f-114">A védelmi tároló megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dee2f-114">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee2f-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dee2f-115">-ProtectionContainer</span></span>
<span data-ttu-id="dee2f-116">Az Azure site Recovery Protection Container objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dee2f-116">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dee2f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee2f-117">CommonParameters</span></span>
<span data-ttu-id="dee2f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dee2f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee2f-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee2f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee2f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dee2f-120">INPUTS</span></span>

### <span data-ttu-id="dee2f-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dee2f-121">ASRProtectionContainer</span></span>
<span data-ttu-id="dee2f-122">A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dee2f-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="dee2f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dee2f-123">OUTPUTS</span></span>

### <span data-ttu-id="dee2f-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dee2f-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dee2f-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dee2f-125">NOTES</span></span>

## <span data-ttu-id="dee2f-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dee2f-126">RELATED LINKS</span></span>

[<span data-ttu-id="dee2f-127">Új – AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dee2f-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="dee2f-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="dee2f-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
