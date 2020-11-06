---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492168"
---
# <span data-ttu-id="e42a3-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e42a3-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="e42a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e42a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e42a3-103">Az Azure webhely-helyreállítási feladat újraindítása.</span><span class="sxs-lookup"><span data-stu-id="e42a3-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e42a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e42a3-104">SYNTAX</span></span>

### <span data-ttu-id="e42a3-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e42a3-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e42a3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e42a3-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e42a3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e42a3-107">DESCRIPTION</span></span>
<span data-ttu-id="e42a3-108">Az **Újraindítás – AzureRmSiteRecoveryJob** parancsmag újraindítja az Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="e42a3-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="e42a3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e42a3-109">EXAMPLES</span></span>

## <span data-ttu-id="e42a3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e42a3-110">PARAMETERS</span></span>

### <span data-ttu-id="e42a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42a3-111">-DefaultProfile</span></span>
<span data-ttu-id="e42a3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e42a3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e42a3-113">-Job</span><span class="sxs-lookup"><span data-stu-id="e42a3-113">-Job</span></span>
<span data-ttu-id="e42a3-114">A webhely-helyreállítási feladat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e42a3-114">Specifies the Site Recovery job object.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e42a3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e42a3-115">-Name</span></span>
<span data-ttu-id="e42a3-116">A feladat egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e42a3-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="e42a3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42a3-117">CommonParameters</span></span>
<span data-ttu-id="e42a3-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e42a3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42a3-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e42a3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42a3-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e42a3-120">INPUTS</span></span>

### <span data-ttu-id="e42a3-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="e42a3-121">ASRJob</span></span>
<span data-ttu-id="e42a3-122">A ' Job ' paraméter elfogadja a "ASRJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e42a3-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="e42a3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e42a3-123">OUTPUTS</span></span>

### <span data-ttu-id="e42a3-124">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e42a3-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e42a3-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e42a3-125">NOTES</span></span>

## <span data-ttu-id="e42a3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e42a3-126">RELATED LINKS</span></span>

[<span data-ttu-id="e42a3-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e42a3-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="e42a3-128">Önéletrajz – AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e42a3-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="e42a3-129">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e42a3-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
