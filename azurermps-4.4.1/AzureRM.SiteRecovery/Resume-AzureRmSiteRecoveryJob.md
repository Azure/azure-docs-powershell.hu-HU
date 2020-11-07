---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679020"
---
# <span data-ttu-id="a0ca2-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a0ca2-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="a0ca2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ca2-103">Folytatja a felfüggesztett webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0ca2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0ca2-104">SYNTAX</span></span>

### <span data-ttu-id="a0ca2-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a0ca2-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0ca2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a0ca2-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0ca2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0ca2-107">DESCRIPTION</span></span>
<span data-ttu-id="a0ca2-108">A **resume-AzureRmSiteRecoveryJob** parancsmag folytatja a felfüggesztett Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="a0ca2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a0ca2-109">EXAMPLES</span></span>

## <span data-ttu-id="a0ca2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0ca2-110">PARAMETERS</span></span>

### <span data-ttu-id="a0ca2-111">-Megjegyzések</span><span class="sxs-lookup"><span data-stu-id="a0ca2-111">-Comments</span></span>
<span data-ttu-id="a0ca2-112">A Projektnapló megjegyzéseit adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-112">Specifies the comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ca2-113">-Job</span><span class="sxs-lookup"><span data-stu-id="a0ca2-113">-Job</span></span>
<span data-ttu-id="a0ca2-114">A webhely-helyreállítási feladat objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="a0ca2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0ca2-115">-Name</span></span>
<span data-ttu-id="a0ca2-116">A feladat egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="a0ca2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ca2-117">-DefaultProfile</span></span>
<span data-ttu-id="a0ca2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0ca2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ca2-119">CommonParameters</span></span>
<span data-ttu-id="a0ca2-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0ca2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ca2-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0ca2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ca2-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0ca2-122">INPUTS</span></span>

### <span data-ttu-id="a0ca2-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="a0ca2-123">ASRJob</span></span>
<span data-ttu-id="a0ca2-124">A ' Job ' paraméter elfogadja a "ASRJob" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a0ca2-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="a0ca2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0ca2-125">OUTPUTS</span></span>

### <span data-ttu-id="a0ca2-126">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a0ca2-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a0ca2-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0ca2-127">NOTES</span></span>

## <span data-ttu-id="a0ca2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0ca2-128">RELATED LINKS</span></span>

[<span data-ttu-id="a0ca2-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a0ca2-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="a0ca2-130">Újraindítás – AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a0ca2-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="a0ca2-131">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="a0ca2-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
