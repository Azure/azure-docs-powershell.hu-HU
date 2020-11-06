---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500388"
---
# <span data-ttu-id="0d3dd-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0d3dd-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="0d3dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0d3dd-103">Frissíti az Azure webhely-helyreállítási szolgáltatás szolgáltatójától kapott információkat.</span><span class="sxs-lookup"><span data-stu-id="0d3dd-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d3dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d3dd-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d3dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d3dd-105">DESCRIPTION</span></span>
<span data-ttu-id="0d3dd-106">Az **Update-AzureRmSiteRecoveryServicesProvider** parancsmag frissíti az Azure webhely-helyreállítási szolgáltatás szolgáltatójától kapott információkat.</span><span class="sxs-lookup"><span data-stu-id="0d3dd-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="0d3dd-107">Ezzel a parancsmaggal megadhatja a helyreállítási szolgáltatótól kapott információk frissítését.</span><span class="sxs-lookup"><span data-stu-id="0d3dd-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="0d3dd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0d3dd-108">EXAMPLES</span></span>

## <span data-ttu-id="0d3dd-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d3dd-109">PARAMETERS</span></span>

### <span data-ttu-id="0d3dd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d3dd-110">-DefaultProfile</span></span>
<span data-ttu-id="0d3dd-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d3dd-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d3dd-112">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0d3dd-112">-ServicesProvider</span></span>
<span data-ttu-id="0d3dd-113">Az Azure webhely-helyreállítási szolgáltató objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d3dd-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d3dd-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d3dd-114">CommonParameters</span></span>
<span data-ttu-id="0d3dd-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d3dd-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d3dd-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d3dd-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d3dd-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d3dd-117">INPUTS</span></span>

### <span data-ttu-id="0d3dd-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0d3dd-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="0d3dd-119">A ' ServicesProvider ' paraméter az "ASRRecoveryServicesProvider" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0d3dd-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="0d3dd-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d3dd-120">OUTPUTS</span></span>

## <span data-ttu-id="0d3dd-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d3dd-121">NOTES</span></span>

## <span data-ttu-id="0d3dd-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d3dd-122">RELATED LINKS</span></span>

[<span data-ttu-id="0d3dd-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0d3dd-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="0d3dd-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="0d3dd-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
