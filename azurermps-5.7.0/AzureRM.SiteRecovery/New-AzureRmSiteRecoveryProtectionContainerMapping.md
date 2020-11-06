---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 950c5c8e2007568add1aba1122356de670884c07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502376"
---
# <span data-ttu-id="d08e7-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d08e7-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="d08e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d08e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d08e7-103">Az Azure webhely-helyreállítási védelmi tárolók megfeleltetését egy házirend védett tárolóhoz társításával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d08e7-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d08e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d08e7-104">SYNTAX</span></span>

### <span data-ttu-id="d08e7-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d08e7-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d08e7-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d08e7-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d08e7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d08e7-107">DESCRIPTION</span></span>
<span data-ttu-id="d08e7-108">A **New-AzureRmSiteRecoveryProtectionContainerMapping** parancsmag létrehoz egy Azure site Recovery Protection Container-megfeleltetést, ha egy házirendet egy védelmi tárolóhoz társít.</span><span class="sxs-lookup"><span data-stu-id="d08e7-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="d08e7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d08e7-109">EXAMPLES</span></span>

## <span data-ttu-id="d08e7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d08e7-110">PARAMETERS</span></span>

### <span data-ttu-id="d08e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08e7-111">-DefaultProfile</span></span>
<span data-ttu-id="d08e7-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d08e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d08e7-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d08e7-113">-Name</span></span>
<span data-ttu-id="d08e7-114">A védelmi tároló megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d08e7-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="d08e7-115">-Házirend</span><span class="sxs-lookup"><span data-stu-id="d08e7-115">-Policy</span></span>
<span data-ttu-id="d08e7-116">Az Azure-webhely helyreállítási házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d08e7-116">Specifies the Azure Site Recovery Policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d08e7-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d08e7-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="d08e7-118">Az elsődleges védelmi tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="d08e7-118">Specifies the primary Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08e7-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d08e7-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="d08e7-120">A helyreállítási védelem tárolójának objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d08e7-120">Specifies the Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08e7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08e7-121">CommonParameters</span></span>
<span data-ttu-id="d08e7-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d08e7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08e7-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d08e7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08e7-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d08e7-124">INPUTS</span></span>

### <span data-ttu-id="d08e7-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d08e7-125">ASRPolicy</span></span>
<span data-ttu-id="d08e7-126">A ' Policy ' paraméter az "ASRPolicy" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d08e7-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="d08e7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d08e7-127">OUTPUTS</span></span>

### <span data-ttu-id="d08e7-128">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d08e7-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d08e7-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d08e7-129">NOTES</span></span>

## <span data-ttu-id="d08e7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d08e7-130">RELATED LINKS</span></span>

[<span data-ttu-id="d08e7-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d08e7-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="d08e7-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d08e7-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
