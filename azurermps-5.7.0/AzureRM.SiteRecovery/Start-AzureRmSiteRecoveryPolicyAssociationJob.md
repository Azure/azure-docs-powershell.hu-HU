---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicyassociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 140bec7738d107574db5d0d157cc3f8cfac46583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679663"
---
# <span data-ttu-id="477b5-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="477b5-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="477b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="477b5-102">SYNOPSIS</span></span>
<span data-ttu-id="477b5-103">A webhely-helyreállítási házirend társítási feladatát indítja el.</span><span class="sxs-lookup"><span data-stu-id="477b5-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="477b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="477b5-104">SYNTAX</span></span>

### <span data-ttu-id="477b5-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="477b5-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="477b5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="477b5-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="477b5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="477b5-107">DESCRIPTION</span></span>
<span data-ttu-id="477b5-108">A **Start-AzureRmSiteRecoveryPolicyAssociationJob** parancsmag társítási feladatot kezdeményez a replikációs házirend társításához az Azure webhely-helyreállítási védelmi tárolóval.</span><span class="sxs-lookup"><span data-stu-id="477b5-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="477b5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="477b5-109">EXAMPLES</span></span>

## <span data-ttu-id="477b5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="477b5-110">PARAMETERS</span></span>

### <span data-ttu-id="477b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477b5-111">-DefaultProfile</span></span>
<span data-ttu-id="477b5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="477b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="477b5-113">-Házirend</span><span class="sxs-lookup"><span data-stu-id="477b5-113">-Policy</span></span>
<span data-ttu-id="477b5-114">A webhely-helyreállítási házirend objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="477b5-114">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="477b5-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="477b5-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="477b5-116">Azt az elsődleges védelmi tárolót adja meg, amelyre a védelmi profil beállításait alkalmazni szeretné.</span><span class="sxs-lookup"><span data-stu-id="477b5-116">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="477b5-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="477b5-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="477b5-118">Annak a helyreállítási védelemnek a tárolóját adja meg, amelyre a védelmi profil beállításait alkalmazni szeretné.</span><span class="sxs-lookup"><span data-stu-id="477b5-118">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="477b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477b5-119">CommonParameters</span></span>
<span data-ttu-id="477b5-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="477b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477b5-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477b5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477b5-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="477b5-122">INPUTS</span></span>

### <span data-ttu-id="477b5-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="477b5-123">ASRPolicy</span></span>
<span data-ttu-id="477b5-124">A ' Policy ' paraméter az "ASRPolicy" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="477b5-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="477b5-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="477b5-125">OUTPUTS</span></span>

### <span data-ttu-id="477b5-126">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="477b5-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="477b5-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="477b5-127">NOTES</span></span>

## <span data-ttu-id="477b5-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="477b5-128">RELATED LINKS</span></span>

