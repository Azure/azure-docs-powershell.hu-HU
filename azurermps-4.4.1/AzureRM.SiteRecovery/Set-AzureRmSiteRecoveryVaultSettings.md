---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: 9c252649ea668e666c98719ab2045e99e729a836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500675"
---
# <span data-ttu-id="c5e1e-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c5e1e-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="c5e1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e1e-103">A webhely-helyreállítási boltozat környezetének beállítása további műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="c5e1e-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5e1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5e1e-104">SYNTAX</span></span>

### <span data-ttu-id="c5e1e-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c5e1e-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5e1e-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c5e1e-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5e1e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5e1e-107">DESCRIPTION</span></span>
<span data-ttu-id="c5e1e-108">A **set-AzureRmSiteRecoveryVaultSettings** parancsmag az Azure webhely-helyreállítási boltozat környezetének beállításával további műveleteket végezhet.</span><span class="sxs-lookup"><span data-stu-id="c5e1e-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="c5e1e-109">Ez a funkció nem vonatkozik a helyreállítási szolgáltatások boltívekre.</span><span class="sxs-lookup"><span data-stu-id="c5e1e-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="c5e1e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c5e1e-110">EXAMPLES</span></span>

## <span data-ttu-id="c5e1e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5e1e-111">PARAMETERS</span></span>

### <span data-ttu-id="c5e1e-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="c5e1e-112">-ARSVault</span></span>
<span data-ttu-id="c5e1e-113">Egy **ARSVault** objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c5e1e-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e1e-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="c5e1e-114">-ASRVault</span></span>
<span data-ttu-id="c5e1e-115">Egy **ASRVault** objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="c5e1e-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e1e-116">-DefaultProfile</span></span>
<span data-ttu-id="c5e1e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5e1e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5e1e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e1e-118">CommonParameters</span></span>
<span data-ttu-id="c5e1e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5e1e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e1e-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e1e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e1e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5e1e-121">INPUTS</span></span>

### <span data-ttu-id="c5e1e-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="c5e1e-122">ARSVault</span></span>
<span data-ttu-id="c5e1e-123">A ' ARSVault ' paraméter az "ARSVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c5e1e-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="c5e1e-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="c5e1e-124">ASRVault</span></span>
<span data-ttu-id="c5e1e-125">A ' ASRVault ' paraméter az "ASRVault" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c5e1e-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="c5e1e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5e1e-126">OUTPUTS</span></span>

### <span data-ttu-id="c5e1e-127">Microsoft. Azure. Command. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c5e1e-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c5e1e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5e1e-128">NOTES</span></span>

## <span data-ttu-id="c5e1e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5e1e-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5e1e-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c5e1e-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
