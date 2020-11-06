---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502791"
---
# <span data-ttu-id="fac59-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="fac59-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="fac59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fac59-102">SYNOPSIS</span></span>
<span data-ttu-id="fac59-103">Várakozás a biztonsági mentési feladat befejezésére.</span><span class="sxs-lookup"><span data-stu-id="fac59-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fac59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fac59-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fac59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fac59-105">DESCRIPTION</span></span>
<span data-ttu-id="fac59-106">A **WAIT-AzureRmBackupJob** parancsmag megvárja az Azure biztonsági mentési feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="fac59-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="fac59-107">A biztonságimásolat-feladatok hosszú időt vehetnek igénybe.</span><span class="sxs-lookup"><span data-stu-id="fac59-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="fac59-108">Ha egy parancsfájl részeként biztonsági mentési feladatot futtat, előfordulhat, hogy a parancsfájlt úgy kell megvárnia, hogy a feladat befejezését követően továbbra is megmaradjon az egyéb tevékenységekre.</span><span class="sxs-lookup"><span data-stu-id="fac59-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="fac59-109">Az e parancsmagot tartalmazó parancsfájlok egyszerűbbek, mint a biztonsági mentési szolgáltatás a munkahelyi állapothoz.</span><span class="sxs-lookup"><span data-stu-id="fac59-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="fac59-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fac59-110">EXAMPLES</span></span>

## <span data-ttu-id="fac59-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fac59-111">PARAMETERS</span></span>

### <span data-ttu-id="fac59-112">-Job</span><span class="sxs-lookup"><span data-stu-id="fac59-112">-Job</span></span>
<span data-ttu-id="fac59-113">A parancsmag által lemondott feladatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fac59-113">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="fac59-114">**AzureRmBackupJob** objektum beolvasásához használja az Get-AzureRmBackupJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fac59-114">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fac59-115">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="fac59-115">-TimeOut</span></span>
<span data-ttu-id="fac59-116">Annak a maximális időpontnak a száma, másodpercben kifejezve, hogy ez a parancsmag várja a feladat befejezését.</span><span class="sxs-lookup"><span data-stu-id="fac59-116">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="fac59-117">Azt javasoljuk, hogy adja meg az időtúllépés értékét.</span><span class="sxs-lookup"><span data-stu-id="fac59-117">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fac59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac59-118">-DefaultProfile</span></span>
<span data-ttu-id="fac59-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fac59-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fac59-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac59-120">CommonParameters</span></span>
<span data-ttu-id="fac59-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fac59-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac59-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fac59-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac59-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac59-123">INPUTS</span></span>

### <span data-ttu-id="fac59-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="fac59-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="fac59-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac59-125">OUTPUTS</span></span>

### <span data-ttu-id="fac59-126">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="fac59-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="fac59-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fac59-127">NOTES</span></span>

## <span data-ttu-id="fac59-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fac59-128">RELATED LINKS</span></span>

[<span data-ttu-id="fac59-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="fac59-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="fac59-130">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="fac59-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


