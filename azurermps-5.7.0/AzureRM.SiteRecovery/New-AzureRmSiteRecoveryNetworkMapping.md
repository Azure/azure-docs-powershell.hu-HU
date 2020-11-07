---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 36f5c6e535cc67029fac7c951cbc6dbbe3c73091
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679679"
---
# <span data-ttu-id="d6c08-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d6c08-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="d6c08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6c08-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c08-103">Társítást hoz létre a virtuális hálózatok között.</span><span class="sxs-lookup"><span data-stu-id="d6c08-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6c08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6c08-104">SYNTAX</span></span>

### <span data-ttu-id="d6c08-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d6c08-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6c08-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d6c08-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6c08-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6c08-107">DESCRIPTION</span></span>
<span data-ttu-id="d6c08-108">A **New-AzureRMSiteRecoveryNetworkMapping** parancsmag létrehoz egy megfeleltetést két virtuális hálózat között, és egy Azure webhely-helyreállítási feladatot ad eredményül a követéshez.</span><span class="sxs-lookup"><span data-stu-id="d6c08-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="d6c08-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6c08-109">EXAMPLES</span></span>

## <span data-ttu-id="d6c08-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6c08-110">PARAMETERS</span></span>

### <span data-ttu-id="d6c08-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d6c08-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="d6c08-112">Az Azure virtuális hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6c08-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c08-113">-DefaultProfile</span></span>
<span data-ttu-id="d6c08-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6c08-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6c08-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6c08-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-116">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="d6c08-116">-PrimaryNetwork</span></span>
<span data-ttu-id="d6c08-117">Az elsődleges hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6c08-117">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-118">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="d6c08-118">-RecoveryNetwork</span></span>
<span data-ttu-id="d6c08-119">A helyreállítási hálózat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6c08-119">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c08-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c08-120">CommonParameters</span></span>
<span data-ttu-id="d6c08-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6c08-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c08-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6c08-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c08-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6c08-123">INPUTS</span></span>

### <span data-ttu-id="d6c08-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="d6c08-124">ASRNetwork</span></span>
<span data-ttu-id="d6c08-125">A ' PrimaryNetwork ' paraméter az "ASRNetwork" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d6c08-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="d6c08-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6c08-126">OUTPUTS</span></span>

### <span data-ttu-id="d6c08-127">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d6c08-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d6c08-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6c08-128">NOTES</span></span>

## <span data-ttu-id="d6c08-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6c08-129">RELATED LINKS</span></span>

[<span data-ttu-id="d6c08-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d6c08-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="d6c08-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d6c08-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
