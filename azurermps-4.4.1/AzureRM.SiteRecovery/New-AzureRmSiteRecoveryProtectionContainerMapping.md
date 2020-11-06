---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500691"
---
# <span data-ttu-id="f1647-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f1647-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="f1647-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1647-102">SYNOPSIS</span></span>
<span data-ttu-id="f1647-103">Az Azure webhely-helyreállítási védelmi tárolók megfeleltetését egy házirend védett tárolóhoz társításával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f1647-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1647-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1647-104">SYNTAX</span></span>

### <span data-ttu-id="f1647-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1647-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1647-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="f1647-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1647-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1647-107">DESCRIPTION</span></span>
<span data-ttu-id="f1647-108">A **New-AzureRmSiteRecoveryProtectionContainerMapping** parancsmag létrehoz egy Azure site Recovery Protection Container-megfeleltetést, ha egy házirendet egy védelmi tárolóhoz társít.</span><span class="sxs-lookup"><span data-stu-id="f1647-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="f1647-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f1647-109">EXAMPLES</span></span>

## <span data-ttu-id="f1647-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1647-110">PARAMETERS</span></span>

### <span data-ttu-id="f1647-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1647-111">-Name</span></span>
<span data-ttu-id="f1647-112">A védelmi tároló megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1647-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1647-113">-Házirend</span><span class="sxs-lookup"><span data-stu-id="f1647-113">-Policy</span></span>
<span data-ttu-id="f1647-114">Az Azure-webhely helyreállítási házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1647-114">Specifies the Azure Site Recovery Policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1647-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f1647-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="f1647-116">Az elsődleges védelmi tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="f1647-116">Specifies the primary Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1647-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f1647-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="f1647-118">A helyreállítási védelem tárolójának objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1647-118">Specifies the Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1647-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1647-119">-DefaultProfile</span></span>
<span data-ttu-id="f1647-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1647-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1647-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1647-121">CommonParameters</span></span>
<span data-ttu-id="f1647-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1647-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1647-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1647-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1647-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1647-124">INPUTS</span></span>

### <span data-ttu-id="f1647-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f1647-125">ASRPolicy</span></span>
<span data-ttu-id="f1647-126">A ' Policy ' paraméter az "ASRPolicy" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f1647-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="f1647-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1647-127">OUTPUTS</span></span>

### <span data-ttu-id="f1647-128">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f1647-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f1647-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1647-129">NOTES</span></span>

## <span data-ttu-id="f1647-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1647-130">RELATED LINKS</span></span>

[<span data-ttu-id="f1647-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f1647-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="f1647-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f1647-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
