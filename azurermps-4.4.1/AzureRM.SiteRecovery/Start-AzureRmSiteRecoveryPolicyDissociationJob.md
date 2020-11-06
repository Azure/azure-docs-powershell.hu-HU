---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494636"
---
# <span data-ttu-id="b2cb1-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="b2cb1-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="b2cb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="b2cb1-103">Disszociációs feladatot indít egy webhely-helyreállítási védelemmel ellátni kívánt replikációs házirendben.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2cb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2cb1-104">SYNTAX</span></span>

### <span data-ttu-id="b2cb1-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2cb1-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2cb1-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b2cb1-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2cb1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2cb1-107">DESCRIPTION</span></span>
<span data-ttu-id="b2cb1-108">A **Start-AzureRmSiteRecoveryPolicyDissociationJob** parancsmag disszociációs feladatot kezdeményez az Azure-webhely helyreállítási védelmi tárolója által társított replikációs házirendben.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="b2cb1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b2cb1-109">EXAMPLES</span></span>

## <span data-ttu-id="b2cb1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2cb1-110">PARAMETERS</span></span>

### <span data-ttu-id="b2cb1-111">-Házirend</span><span class="sxs-lookup"><span data-stu-id="b2cb1-111">-Policy</span></span>
<span data-ttu-id="b2cb1-112">Egy Azure-webhely helyreállítási házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-112">Specifies an Azure Site Recovery policy object.</span></span>

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

### <span data-ttu-id="b2cb1-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b2cb1-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="b2cb1-114">Az elsődleges védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-114">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="b2cb1-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b2cb1-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="b2cb1-116">A helyreállítási védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-116">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="b2cb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2cb1-117">-DefaultProfile</span></span>
<span data-ttu-id="b2cb1-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2cb1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2cb1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2cb1-119">CommonParameters</span></span>
<span data-ttu-id="b2cb1-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2cb1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2cb1-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2cb1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2cb1-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2cb1-122">INPUTS</span></span>

### <span data-ttu-id="b2cb1-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b2cb1-123">ASRPolicy</span></span>
<span data-ttu-id="b2cb1-124">A ' Policy ' paraméter az "ASRPolicy" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b2cb1-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="b2cb1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2cb1-125">OUTPUTS</span></span>

### <span data-ttu-id="b2cb1-126">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b2cb1-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b2cb1-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2cb1-127">NOTES</span></span>

## <span data-ttu-id="b2cb1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2cb1-128">RELATED LINKS</span></span>

