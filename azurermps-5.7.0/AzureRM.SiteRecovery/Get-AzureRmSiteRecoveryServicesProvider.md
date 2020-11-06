---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 4e65636c732ede20487df0b80973172977c6c832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502400"
---
# <span data-ttu-id="c0ccb-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c0ccb-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="c0ccb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ccb-103">Információt kap az Azure webhely-helyreállítási szolgáltatónál a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0ccb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0ccb-104">SYNTAX</span></span>

### <span data-ttu-id="c0ccb-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0ccb-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0ccb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c0ccb-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ccb-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c0ccb-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0ccb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0ccb-108">DESCRIPTION</span></span>
<span data-ttu-id="c0ccb-109">A **Get-AzureRmSiteRecoveryServicesProvider** parancsmag információt kap az Azure webhely-helyreállítási szolgáltatónál a boltozatban.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="c0ccb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c0ccb-110">EXAMPLES</span></span>

## <span data-ttu-id="c0ccb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0ccb-111">PARAMETERS</span></span>

### <span data-ttu-id="c0ccb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ccb-112">-DefaultProfile</span></span>
<span data-ttu-id="c0ccb-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0ccb-114">-Szövet</span><span class="sxs-lookup"><span data-stu-id="c0ccb-114">-Fabric</span></span>
<span data-ttu-id="c0ccb-115">Az Azure site Recovery Fabric objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-115">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ccb-116">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="c0ccb-116">-FriendlyName</span></span>
<span data-ttu-id="c0ccb-117">Annak az Azure-webhely-helyreállítási szolgáltatónak a felhasználóbarát nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-117">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ccb-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0ccb-118">-Name</span></span>
<span data-ttu-id="c0ccb-119">Annak az Azure-webhely-helyreállítási szolgáltatónak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="c0ccb-119">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ccb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ccb-120">CommonParameters</span></span>
<span data-ttu-id="c0ccb-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0ccb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ccb-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ccb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ccb-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0ccb-123">INPUTS</span></span>

### <span data-ttu-id="c0ccb-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c0ccb-124">ASRFabric</span></span>
<span data-ttu-id="c0ccb-125">A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c0ccb-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="c0ccb-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0ccb-126">OUTPUTS</span></span>

### <span data-ttu-id="c0ccb-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. commands. SiteRecovery, Version = 2.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c0ccb-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c0ccb-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0ccb-128">NOTES</span></span>

## <span data-ttu-id="c0ccb-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0ccb-129">RELATED LINKS</span></span>

[<span data-ttu-id="c0ccb-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c0ccb-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="c0ccb-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c0ccb-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
