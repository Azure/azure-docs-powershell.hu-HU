---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 14f24f9b9659b6668041b800462eca422fb67c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672098"
---
# <span data-ttu-id="e7f2c-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e7f2c-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="e7f2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f2c-103">Az Azure webhely-helyreállítási feladat leállítása.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7f2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7f2c-104">SYNTAX</span></span>

### <span data-ttu-id="e7f2c-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7f2c-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f2c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e7f2c-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f2c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7f2c-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f2c-108">A **stop-AzureRmRecoveryServicesAsrJob** parancsmag leállítja a megadott Azure-webhely helyreállítási feladatát.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="e7f2c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e7f2c-109">EXAMPLES</span></span>

### <span data-ttu-id="e7f2c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7f2c-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="e7f2c-111">Megkísérli leállítani a megadott feladatot, és egy frissített ASR-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="e7f2c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7f2c-112">PARAMETERS</span></span>

### <span data-ttu-id="e7f2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f2c-113">-DefaultProfile</span></span>
<span data-ttu-id="e7f2c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e7f2c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f2c-115">-InputObject</span></span>
<span data-ttu-id="e7f2c-116">Beviteli objektum: Itt adhatja meg az ASR-feladat leállításának megfelelő ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7f2c-117">-Name</span></span>
<span data-ttu-id="e7f2c-118">Adja meg azt az ASR-feladatot, amelyet az ASR-feladat nevében le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="e7f2c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7f2c-119">-Confirm</span></span>
<span data-ttu-id="e7f2c-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f2c-121">-WhatIf</span></span>
<span data-ttu-id="e7f2c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7f2c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7f2c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f2c-124">CommonParameters</span></span>
<span data-ttu-id="e7f2c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7f2c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f2c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f2c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f2c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f2c-127">INPUTS</span></span>

### <span data-ttu-id="e7f2c-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e7f2c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e7f2c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7f2c-129">OUTPUTS</span></span>

### <span data-ttu-id="e7f2c-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e7f2c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e7f2c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7f2c-131">NOTES</span></span>

## <span data-ttu-id="e7f2c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7f2c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e7f2c-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e7f2c-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="e7f2c-134">Újraindítás – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e7f2c-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="e7f2c-135">Önéletrajz – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e7f2c-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
