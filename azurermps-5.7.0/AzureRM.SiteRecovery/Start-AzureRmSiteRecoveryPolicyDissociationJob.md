---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicydissociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: eb12462b85c4a12416f41f899ebc9b2c46cca465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501380"
---
# <span data-ttu-id="6afaa-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="6afaa-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="6afaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6afaa-102">SYNOPSIS</span></span>
<span data-ttu-id="6afaa-103">Disszociációs feladatot indít egy webhely-helyreállítási védelemmel ellátni kívánt replikációs házirendben.</span><span class="sxs-lookup"><span data-stu-id="6afaa-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6afaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6afaa-104">SYNTAX</span></span>

### <span data-ttu-id="6afaa-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6afaa-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6afaa-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="6afaa-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6afaa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6afaa-107">DESCRIPTION</span></span>
<span data-ttu-id="6afaa-108">A **Start-AzureRmSiteRecoveryPolicyDissociationJob** parancsmag disszociációs feladatot kezdeményez az Azure-webhely helyreállítási védelmi tárolója által társított replikációs házirendben.</span><span class="sxs-lookup"><span data-stu-id="6afaa-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="6afaa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6afaa-109">EXAMPLES</span></span>

## <span data-ttu-id="6afaa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6afaa-110">PARAMETERS</span></span>

### <span data-ttu-id="6afaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afaa-111">-DefaultProfile</span></span>
<span data-ttu-id="6afaa-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6afaa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6afaa-113">-Házirend</span><span class="sxs-lookup"><span data-stu-id="6afaa-113">-Policy</span></span>
<span data-ttu-id="6afaa-114">Egy Azure-webhely helyreállítási házirend-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6afaa-114">Specifies an Azure Site Recovery policy object.</span></span>

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

### <span data-ttu-id="6afaa-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6afaa-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="6afaa-116">Az elsődleges védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="6afaa-116">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="6afaa-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6afaa-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="6afaa-118">A helyreállítási védelmi tárolót adja meg.</span><span class="sxs-lookup"><span data-stu-id="6afaa-118">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="6afaa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afaa-119">CommonParameters</span></span>
<span data-ttu-id="6afaa-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6afaa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afaa-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6afaa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afaa-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6afaa-122">INPUTS</span></span>

### <span data-ttu-id="6afaa-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="6afaa-123">ASRPolicy</span></span>
<span data-ttu-id="6afaa-124">A ' Policy ' paraméter az "ASRPolicy" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6afaa-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="6afaa-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6afaa-125">OUTPUTS</span></span>

### <span data-ttu-id="6afaa-126">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6afaa-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6afaa-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6afaa-127">NOTES</span></span>

## <span data-ttu-id="6afaa-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6afaa-128">RELATED LINKS</span></span>

