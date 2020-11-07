---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 506009ac15fa1c9eeeb3e0b7ae902e3c42d1d468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679838"
---
# <span data-ttu-id="fc88b-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc88b-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="fc88b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc88b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc88b-103">A helyreállítási szolgáltatások boltozatához regisztrált ASR-helyreállítási szolgáltató adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fc88b-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc88b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc88b-104">SYNTAX</span></span>

### <span data-ttu-id="fc88b-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc88b-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc88b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fc88b-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc88b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fc88b-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc88b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc88b-108">DESCRIPTION</span></span>
<span data-ttu-id="fc88b-109">A **Get-AzureRmRecoveryServicesAsrServicesProvider** parancsmag információt kap az Azure webhely-helyreállítási szolgáltatónál a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="fc88b-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="fc88b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fc88b-110">EXAMPLES</span></span>

### <span data-ttu-id="fc88b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc88b-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="fc88b-112">Felsorolja az összes ASR-replikációs szolgáltatót, amely a megadott anyagnak megfelelő helyreállítási szolgáltatások boltozatához van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="fc88b-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="fc88b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc88b-113">PARAMETERS</span></span>

### <span data-ttu-id="fc88b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc88b-114">-DefaultProfile</span></span>
<span data-ttu-id="fc88b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc88b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fc88b-116">-Szövet</span><span class="sxs-lookup"><span data-stu-id="fc88b-116">-Fabric</span></span>
<span data-ttu-id="fc88b-117">Az ASR-szerkezet objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc88b-117">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc88b-118">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="fc88b-118">-FriendlyName</span></span>
<span data-ttu-id="fc88b-119">Az ASR-helyreállítási szolgáltató rövid nevét adja meg, amelyből részletesen tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="fc88b-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc88b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc88b-120">-Name</span></span>
<span data-ttu-id="fc88b-121">Annak az ASR-helyreállítási szolgáltatónak a nevét adja meg, amelyről részleteket szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="fc88b-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc88b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc88b-122">CommonParameters</span></span>
<span data-ttu-id="fc88b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc88b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc88b-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc88b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc88b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc88b-125">INPUTS</span></span>

### <span data-ttu-id="fc88b-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fc88b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="fc88b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc88b-127">OUTPUTS</span></span>

### <span data-ttu-id="fc88b-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fc88b-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fc88b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc88b-129">NOTES</span></span>

## <span data-ttu-id="fc88b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc88b-130">RELATED LINKS</span></span>

[<span data-ttu-id="fc88b-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc88b-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="fc88b-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc88b-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
