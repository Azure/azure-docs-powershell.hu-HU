---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 1b17284a5b0dfbdc8ee031df714c9f9f03533697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500683"
---
# <span data-ttu-id="9d63d-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9d63d-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="9d63d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d63d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d63d-103">Az Azure webhely-helyreállítási feladat újraindítása.</span><span class="sxs-lookup"><span data-stu-id="9d63d-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d63d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d63d-104">SYNTAX</span></span>

### <span data-ttu-id="9d63d-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d63d-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d63d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9d63d-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d63d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d63d-107">DESCRIPTION</span></span>
<span data-ttu-id="9d63d-108">Az **Újraindítás – AzureRmSiteRecoveryJob** parancsmag újraindítja az Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="9d63d-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="9d63d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9d63d-109">EXAMPLES</span></span>

## <span data-ttu-id="9d63d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d63d-110">PARAMETERS</span></span>

### <span data-ttu-id="9d63d-111">-Job</span><span class="sxs-lookup"><span data-stu-id="9d63d-111">-Job</span></span>
<span data-ttu-id="9d63d-112">A webhely-helyreállítási feladat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d63d-112">Specifies the Site Recovery job object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d63d-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d63d-113">-Name</span></span>
<span data-ttu-id="9d63d-114">A feladat egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d63d-114">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="9d63d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d63d-115">-DefaultProfile</span></span>
<span data-ttu-id="9d63d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d63d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d63d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d63d-117">CommonParameters</span></span>
<span data-ttu-id="9d63d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d63d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d63d-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d63d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d63d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d63d-120">INPUTS</span></span>

### <span data-ttu-id="9d63d-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="9d63d-121">ASRJob</span></span>
<span data-ttu-id="9d63d-122">A ' Job ' paraméter elfogadja a "ASRJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9d63d-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="9d63d-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d63d-123">OUTPUTS</span></span>

### <span data-ttu-id="9d63d-124">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9d63d-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9d63d-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d63d-125">NOTES</span></span>

## <span data-ttu-id="9d63d-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d63d-126">RELATED LINKS</span></span>

[<span data-ttu-id="9d63d-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9d63d-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="9d63d-128">Önéletrajz – AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9d63d-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="9d63d-129">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9d63d-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
